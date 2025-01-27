#KvaffKap7
## Kontrollvariabler
= *Variabler som vi har med i regressionsanalys för att inte dra felaktiga slutsatser om samvariation, men som vi inte är analytiskt interesserade av (?)*
för studera samvariation mellan X och Y börjar man med fundera över vilka kausala länkar som (teoretiskt) kan sammankoppla de (se [[Studera orsak och samband]])
- ex genom formulera ekvation vars parametrar kan skattas med regression
- Kan vara vanligt misstag att i modellen/ekvationen lägger till alla kända variabler + felterm:
$Y = \alpha + \beta_1 \cdot X_1 + ... + \beta_n \cdot X_n + \epsilon$
- Kan då hålla alla variabler bi inte interesserade av konstanta och ändra den vi är interesserad av

## Val av variabler i regressionsmodell
- många kontrollvariabler != bättre modell
- Ofta är enklaste möjliga modell den bästa
	- Mer pedagogiskt när uppvisa resultat, lättare att replikera tester
- Kan också bli problem med overfitting om man har för många variabler
	- Sådant som egentligen bara är brus (osystematiska fel) "bakas in" i parametrarna för (kontroll)variablerna
	- modellen blir väldigt specefikt anpassad till just de data den skattats med, sämre lämoad att beskriva underliggande processen
	- överanpassning försämrar möjlighet t prediktion
- Vanligt att experimentera med modellen; ex ta bort icke statistiskt signifikanta variabler
	- Kan göra detta om andra X-variablers relation till Y ej ändras, eller om modellens exmpelvis MSE eller R2-värde ej ändras/blir sämre
- grupper av variabler kan behöva testas tillsammans, eftersom en av de kan ha ingen påverkan på Y medan de tillsammans har påverkan
	- exempel med olika typer av test på s. 67
- --
- På senare tid vanligt med algoritmer som väljer ut variabler i en modell och skattar modellen
	- exx lassomodell, säter parametrar som är nära 0 till 0
		- kan på så vis komma frammåt i analys, eleminera icke signifikanta variabler, speciellt om inte har teoretisk förståelse för vilka som är relevanta för att förklara Y
		- Kan bli väldigt olika modeller beroende på vilka variabler som finns till hand, används därför bäst som komplement
	- #clarifyKvaff väldigt svårtolkad paragraf slutet av s. 68


