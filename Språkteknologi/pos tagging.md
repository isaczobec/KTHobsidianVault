
om words ambiguos: välj mest common POS

named entity tagging = sätta vad en grupp tokens refererar till (person, ställe, datum, osv)
kan ha BIO tagging för NER:
- blir som siple sequence modelling eftersom assignar `Begin` `Inside` eller `Outside` för varje token

HHM POS tagging
- hidden markov model
- för mappa varje element i en sequence till ett anant element
- HMM based on augmenting markov chain:
	- hidden eftersom vi inte direkt observar alla tags
	- ![[Pasted image 20251102134532.png]]
	- output beror bara på current state (?)
	- statesen är tagsen, observationerna är orden/tokensen
		- beräknar alla probabilities med MLE
		- ![[Pasted image 20251102142117.png]]
		- ![[Pasted image 20251102142123.png]]
		- behöver också initial probabilities för tags
	- FÖr att bestämma sequence of alla tags, hitta den som maximerar likelyhooden given the observed words:
		- För POS tagging ![[Pasted image 20251102135404.png]]
		- Kan istället använda bayes formula och droppa denominatorn: ![[Pasted image 20251102135508.png]]
		- vi använder independence of outputs assumption och markov assumption
		- ![[Pasted image 20251103114420.png]], ![[Pasted image 20251103114427.png]]
- **Viterbi algo**
	- Beräknar $V_t(j)$, sannolikheten att ord t är av typ j givet att vi tagit den mest probable vägen av tags hit
	- ![[Pasted image 20251102141559.png]]
	- lite som stränglänkning

- Forward algorithm
	- för att beräkna sannolikheten att en viss sequence av tags uppkommer, O(N^2 * T)
	- ![[Pasted image 20251102143418.png]]
	- ![[Pasted image 20251102143425.png]]
	- ![[Pasted image 20251102143517.png]]