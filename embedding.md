att mappa varje ord till en vektor som korresponderar mot dess mening

- intuition att liknande ord hamnar i samma contexts, bredvid samma ord
- kan räkna intilligande ord och deras frekvens

## Simple count-based embeddings
- räkna hur många gånger ord appearar nära varandra i en $|V| \times |V|$ matrix
- ![[Pasted image 20251107174856.png]]
- för att mäta similarity: beräkna cosine av vilkeln mellan vektorerna ![[Pasted image 20251107175517.png]]
- eftersom positiva värden i frekvens så kommer värdet $\in [0,1]$

dessa var långa sparse vektorer, kan istället ha kortare mer dense vektorer = **embeddings**
- **word2vec/skip-gram**
	- ger static embeddings = samma för varje ord oavsett context
	- tränar en binary classifier för att svara på “Is word w likely to show up near apricot?”
	- klassifieraren:
		- Ska peräkna $P(+|w,c)$, sannolikheten att c är ett context word till w
		- använd dot produkt av ordens vikter och sigmoid function för estimera: ![[Pasted image 20251107180742.png]]
		- för flera context words, anta att deras appearance är independent: ![[Pasted image 20251107180902.png]]
		- ![[Pasted image 20251107180909.png]]
		- för lärande:
		- har två embeddings per ord: som target word $w$ och context word $c$
		- ger två matriser $W$ och $C$ med embeddings för varje ord vi måste lära oss
		- generera positiva och negativa exempel från träningsdatan
		- ![[Pasted image 20251107181626.png]]
		- samplar negativa exempel med viktad unigram probability (lägre $\alpha$ => högre sannolikhet för ovanliga ord)
		- ![[Pasted image 20251107181709.png]]
		- ge random initial weights till alla ord
		- man vill maximera similarity $P(+|w,c_{pos})$ och maximera dissimilarity $P(-|w,c_{neg})$
		- loss function blir då
			- ![[Pasted image 20251107182126.png]]
		- använd stochastic gradient descent för att minimera
		- derivatives blir: ![[Pasted image 20251107182844.png]]
- embeddings captures relation, ex $\vec{King} - \vec{Man} + \vec{Woman} \approx \vec{Queen}$

![[Pasted image 20251107200736.png]]

kan bli evaluatade genom human made simliarity ratings, hitta bästa synonymen, parallelogramproblem, osv