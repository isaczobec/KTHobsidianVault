
ngram = sequece av n ord.
eller ngram-model = model som kan predicta nästa ord givet n-1 ord

### computing the probabilities
beräkna $P(\text{nästa ord}|\text{history})$
- kan ta alla förekomster i corpus och kolla relativa förekomster av nästa ord

**Markovian assumption**
estimate $P(w_n | w_{1:n-1}) \approx P(w_n | w_{n-1})$
- bigram, eller kan göra om till n-gram
	- $P(w_n | w_{1:n-1}) \approx P(w_n | w_{n-N+1:n-1})$

![[Pasted image 20251102114330.png]]

Eftersom probabilities går mot noll när man multiplyar ihop många tar man log av alla, gör om till addition

för att jämföra flera models:
- den som assignar högst probability till test setet är bäst
- ha en development set som liknar training set, som man testar på under development
- training data ska vara så stor som möjligt

sampling sentences
- välj randomly, viktat av probability distributionen. Ser om det är rimligt eller ej

Om vissa n-grams eller ord inte förekommer i corpusen men ändå är ok kommer de ha zero probabiliy
- då får också hela test settet zero probability
- för att lösa: smoothing
	- laplace smoothing: lägg till 1 alla ngram counts innan normalization
	- ![[Pasted image 20251102122542.png]]
	- eller add-k smoothing: lägg till mindre probability madd till varje count
		- ![[Pasted image 20251102122824.png]]

### Interpolation
- för att lösa zero probability problemet
- blir att man viktar porbabilityn för nästa ord med alla längder på grams
- ![[Pasted image 20251102123056.png]]
- beräknar alla lambdas med en held-out corpus, använder MLE för att maximera probabilities holding the N-gram probabilities fixed
- kan istället använda *stupid backoff*
	- Att man istället för vikta bara går till N-1 gram om inte finns någon occurence av current ngram
	- multiplicerat med någon fixed lambda
	- blir ej en probability distribution
	- ![[Pasted image 20251102123742.png]]