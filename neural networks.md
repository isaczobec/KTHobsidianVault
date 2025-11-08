har många units som alla får en activation:
![[Pasted image 20251108102324.png]]

![[Pasted image 20251108102618.png]]
- en enda unit

activation functions
- ![[Pasted image 20251108102747.png]]
- ![[Pasted image 20251108102754.png]]
- ![[Pasted image 20251108102800.png]]

Nätverk
- haren viss mängd gömda lager
- inga cykler
- alla nodes fully connected
- weight matrix $W$, bias vector $b$

- för att konvertera output till en probability distribution kan vi använda softmax function
- ![[Pasted image 20251108104452.png]]

för flera lager:
![[Pasted image 20251108104845.png]]

kan byta ut bias mot en dummy input node $x_0$ till varje lager
![[Pasted image 20251108105240.png]]

**NLP applications**
![[Pasted image 20251108105610.png]]
kan använda en matris av inputexempel istället för enbart en vektor
![[Pasted image 20251108105840.png]]

kan också använda vector embeddings som input till nätverk

har en stor $|V| \times d$ emedding matrix, välj rätt rader ur den för rätt ord
- kan också tänka att man multiplicerar med en one hot per row matrix
- ![[Pasted image 20251108110417.png]]
- för att sedan passa input till NN kan man concatenate embeddingsen: lägga de efter vartannat i en lång vektor, eller poola de: göra om till en single embedding
- **Pooling**
- ![[Pasted image 20251108110653.png]]
- eller component-wise max pooling

language modelling
- använder concatenation av $N$ embeddings för att gissa framtida
- ska skapa en probability distribution over next possible words
- använder approximationen ![[Pasted image 20251108112836.png]]
- ![[Pasted image 20251108113126.png]]
- använd softmax för att få en output probability för varje möjligt output word i $V$

### Learning
- loss function är ![[Pasted image 20251108114000.png]]
- om har hard classification blir den
- ![[Pasted image 20251108114022.png]]
- med subbad in softmax: ![[Pasted image 20251108114056.png]]
- minskad loss ökar prob right answer och eftersom alla $\hat{y_i}$ summar till 1 så minskar prob för wrong answer

- gradients
- är för sista softmax layer ![[Pasted image 20251108114844.png]]
- backpropogation för att räkna ut tidigare lagers vikters gradienter
- använd computation graphs:
- ![[Pasted image 20251108115652.png]]
- chain rule:
	- ![[Pasted image 20251108115738.png]]![[Pasted image 20251108115741.png]]
- beräkna derivatorna höger till vänster:
	- ![[Pasted image 20251108120047.png]]
- ![[Pasted image 20251108120533.png]]
![[Pasted image 20251108120553.png]]

för minimera overfitting kan ha dropout = randomly droppa nodes under training, eller regularization terms