#KvaffKap7#KvaffKap7
Om skattar sambandandet X -> Y med linjär regressionsmodell blir sambandet bara väntervärdesriktigt om påverkan är exogen i sammanhanget (att det skett variation utifrån som bara påverkar X?)
- om finns confounding factors, förväxlingsfaktorer, som modellen ej fångar upp blir skattning skev
	- => modellen lider av endogenitetsproblem ouppfångad kontrollvariabel
		- (Kan ockås kanske säga att endogenitetsproblem = ej uppfattad intern påverkan av olika variabler?)
		- svårt avgöra vilka variabler som påverkar varandra, vår modell inte lagom komplicerad för fånga upp det
	- God teoretisk förståelse -> kan åtgärda detta, samla in data om förstådda kontrollvariabler/förväxlingsfaktorer
		- Kan dock vara svårt add åtgärd engogenitetsproblem eftersom:
			- Kanske bristfällig förståelse för problemet eller osäker om fångat alla förväxlingsfaktorer
			- kan finnas omätbara förväxlingsfaktorer
			- X kan påverka Y, ömsesidigt snarare än ensidigt orsakssamband
				- Dessa endogenitetsproblem kallas simultanitet, ex studier tillgång efterfrågan
	- För att åtgärda endogenitetsproblem som inte kan lösas med mer/bättre datauppsamling:
		- Experimentell anstats
		- Använda naturligt experiment
		- Om anser de faktorer som orsakar endogenitetsproblem är tidsinvarianta kan man använda paneldata, många olika mätpunkter över tiden och använd endast tidsvariation för skatta koeficienter
			- vanligt i ex epidimeologi eller statsvetenskap där experimentella ansatser svåra att ådstakomma
			- #clarifyKvaff vad är experimentella anstatser nu igen?
		- Ett viktigt verktyg här är skattningsestimator med fasta effekter (fixed effects estimator)
			- $Y_{it} = \alpha_{i} + \beta x_{it}$
				- $\alpha$ tidsinvariant från t och unik till varje individ i
					- På så vis fångar den upp/absorberar alla faktorer som är unika till individen (och som inte ingår i x (!?), x fångar istället det vi interesserade av)
				- endast $\beta$ skattas för hela stickprovet/målpopulationen
				- På detta vis undviker vi endogenitetsproblem som härstammar från tidsinvarianta faktorer som påverkar utfallet vi studerar
					- !!! Men inte andra källor t endogenitet
	- Om vill hantera ömsesidigt beroende variabler eller båda faktorer (X och Y?) påverkas av tidsinvariant oobserverad faktor, måste man ha mer avancerade regressionsmodeller för att undvika endogenitetsproblem i kvasi-experimentella data
		- ex instrumentalvariabelmodeller


Endogenitetsproblem är när någon förklaringsvariabel är korrelerad med felterm, dvs all påverkan av det som vår modell inte har fångat upp
![[Pasted image 20250303203847.png]]