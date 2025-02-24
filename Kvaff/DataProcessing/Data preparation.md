#DataProcessing
Mycket tid läggs på detta

- essentiellt för få high quality results från data analysis and modelling

### Varför data preparation?
- Förbättrar resultat, ta bort errors/inconsitencies, ökar [[reliabilitet och validitet|reliabilitet]]
- Ökar effketivitet: minskar tid/computational resources det tar för data anlaysis/modelling
- Lättare organisera cleaned och organiserad data
- Minskar risk m använda felaktig data

### Vad är data preparation?
- transformera data till något format suitable för analy/rapporter
- Steg:
	- 1. ***Data cleaning***
		- Ta bort inacuracies, inconsitencies, irrelevant information, öka usability/[[reliabilitet och validitet|reliabilitet]]
		- ![[Pasted image 20250224111500.png]]
			- Dessa saker försämrar datans o analysens kvalite
			- *Vanliga fel:*
				- kan ha missing data om folk inte vill uppge saker/ fältet appliar inte till dem/errors i insamlingen
					- Kan hantera genom droppa missing values, keep missing values, inputta vanliga/rimliga values där de saknas
				- dupllicate data
					- om flera kopior/när kopior av samma objekt finns
					- delete/merge records
				- Inconsistent/invalid data
					- Om omöjliga värden under någon kolumn
					- replace med rimlig value eller använd extern data source för få correct value
				- Noise
					- Allt som kan förstöra data
					- filtrera eller ta bort frequent noise components
					- ta bort del av data
				- Outliers
					- Mycket annorlunda värden från resten av datasettet
					- Kan vara failure/real anomaly
					- Undersök ytterligare innan tar bort, men endast om de är fokus av analysen
	- 2. ***Data formatting***
		- Ändra struktur för göra mer suitablre för analys, reporting, eller andra applications
		- ***Feature selection***
			- Välja set av features som är lämpliga för analys
			- Metoder:
				- adding features - data enrichment
					- derived/extern data source
				- removing features - reduction
					- Väldigt korrelerad, saknade värden, irrelevanta värden
				- combining features
					- Om två features inte ger information ensamma kombinerar man de, ex BMI
				- Recoding features
					- Kan göra continous till kategorisk eller liknande
				- breaking up features
					- Göra om ex address till gata, län
			- Välj så få features som möjligt som relevanta för problemet, simplare analys
		- ***Feature transformation***
			- Ändra format av data på något sätt för att minska noise/variabilitet eller göra data enklare att analysera
			- Mappa om set av värden till nytt set för att göra representation av data enklare/mer suitable
			- ***Scaling***
				- Normalisera/standardisera värden som varierar väldigt mycket
				- kan göra ML enklare
				- Normalisering
					- shifta/scala så hamnar i rangen $[0,1]$
				- Standardisering
					- Ändra data så att mean $\mu = 0$ och std $\sigma = 1$
				- Använd stanadrinseng om vet normalfördelning råder (men ingen set in stone regel)
			- ***Aggregation***
				- Summera/averega flera av samma features
					- Kan minska noise och ge tydligare representation
					- 