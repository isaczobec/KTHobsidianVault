
ta en input x och assigna den till en predicted klass $\hat{y} \in Y$
har en labeled trainig set: ![[Pasted image 20251102165904.png]]

- finns också probabalistic classifiers som assignar probability till varje klass

- logistic regression
- använder ex sigmoid function
	- Z calculated med vikter sen normalized till (0,1) med sigmoid function
	- ![[Pasted image 20251102170831.png]]
	- ![[Pasted image 20251102170837.png]]
	- för att göra outputten till en probability (med sums = 1)
		- ![[Pasted image 20251102171058.png]]
- logit är annan term för z 
	- ![[Pasted image 20251102171314.png]]
- för att göra desiscion: yes om sigmoid(z) > 0.5 noll annars
- kan ha feature templetas, blir parsade(?) till features som kan beräknas automatiskt
- brukar standardiza features så att de får mean 0 och std 1
	- ![[Pasted image 20251102172434.png]]
	- kan speeda up learning, comparing values across features
- i matrix form: ![[Pasted image 20251102173039.png]]

**multinomial logistic regression**
- ger istället en output vector Y med $P(y_k=1|x)$ som komponenter. I träningsdatan är alla komponnenter 0 förutom den klassen som är rätt, är 1
- ![[Pasted image 20251102173712.png]]
	- z fortfarande kallat logits
	- för beräkna z behöver vi ny separata viktvektorer för varje output class
		- ![[Pasted image 20251102173913.png]]
		- ha en $K \times f$ weight matrix $W$ 
			- ger ![[Pasted image 20251102174135.png]]
- Weoght vectorn blir som en prototype för en klass, kan ta dot product mellan två stycken för att se lika de är
- feature kan vara evidence för eller emot varje klass i multinomial, men är antingen eller baserat på vikterna i binary classification

**learning in logistic regression**
- distance mellan $\hat{y}$ och $y$ är cost function, ska minimeras
- vi har fått estimeringen:
	- ![[Pasted image 20251102180539.png]]
	- log ![[Pasted image 20251102180558.png]]
	- ta \*-1 för att minimera istället för maximera 
	- ![[Pasted image 20251102180713.png]]
- mål med lärandet:
	- ![[Pasted image 20251102181109.png]]
	- vi använder gradient descent, beräkna derivatan med avseende på alla parametrar och gå dit den lutar mest
	- cost funktionen i logistic regression är convex ^^^
	- har en leaarning rate, multiplicera med derivatan
	- ![[Pasted image 20251102181711.png]]
	- använd gradienten när har många parametrar
	- ![[Pasted image 20251102181918.png]]
	- ![[Pasted image 20251102182000.png]]
	- derivatorna för cross entropy loss fumction:
		- ![[Pasted image 20251102182154.png]]
- Stochastic gradient descent
	- räknar ut gradienten och nudgar $\theta$ efter varje randomly selected training example
- bartch training
	- Räknar ut gradient för hela training settet
	- mycket computation
- mini batch
	- ta m exempel, sen gå
	- för beräkna loss function, anta training examples är independent
		- ![[Pasted image 20251102183021.png]]
		- så blir samma som summan av loss för varje exempel
		- ![[Pasted image 20251102183147.png]]

**för multinomial distribution**
![[Pasted image 20251102192108.png]]
![[Pasted image 20251102192431.png]]

### Evaluation: Precision, Recall, F-measure
- har true/false negatives/positives
- att beräkna accuracy som andel korrekt klassifierade fall är missvisande om försöker klassificiera rare cases
	- använder istället preciscion och recall
		- ![[Pasted image 20251103120553.png]]
		- ![[Pasted image 20251103120639.png]]
	- för väga båda har vi F-measure
		- beta > 1 favors recall, beta < 1 favor precision
		- ![[Pasted image 20251103120829.png]]
		- kommer från harmonic mean
			- ![[Pasted image 20251103120952.png]]
- För flera klasser:
	- ![[Pasted image 20251103121227.png]]
	- kan ha macroavaraging: Beräkna en true/false positive/negative matrix för varje klass och sen average ihop metrics
	- Microavaraging: skapa en ända matrix med true/false positives/negatives
		- I denna blir more frequent class facoured

## Cross validation
- för att få använda all data för test och training
- cross validation: dela in all data i k folds, välj sedan k-1 av de för träna på, testa på den sista och beräkna sedan average erorr rate
- måste vara blind corpus man tränar på: blir fusk att kolla på testdatan
	- för denna anledning brukar man ända ha ett avsett test set, men skippa dev sets

## Overfitting/reguralization
- Om vissa features bara accidentaly associearde med en viss klass i training data har vi overfitting, vill att modelen ska vara general istället
- lägg till en regularization term till loss function
- ![[Pasted image 20251103123214.png]]
- R-termen penalizar stora vikter, ska bli mer generell
- kan ex vara
	- ![[Pasted image 20251103123302.png]]
	- ![[Pasted image 20251103123308.png]]
- L2 preferar många small weights, L1 många 0 och några högre