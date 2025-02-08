#KvaffKap4
Modeller förändrar komplex verklighet/värld till någott greppbart / översiktligt

## modeller som representation
- modell = representation komplexa/mångtydliga verkligheter
- Människans vardagilga tänkande bygger på tumregler/heurestiker, slags modeller
- modeller samlar erfarenheter som tolkas som generellt mönster
	- ex antiker som värderar möbel
		- är en informell modell, ofta bättre i analys med kvantitativa data med formell modell
### Vad är en bra modell??
- teori = systematisk förståelse av fenomen
- Modell = konkret manifestation av teori
	- Behöver förhålla sig till teori för göra bra modell, för få hög [[reliabilitet och validitet]] i föreänderlig värld
- Bra model != modell som beskriver världen så exakt som möjligt
	- Istället en som lätt hjälper en få syn på några interessanta aspekter av fenomenet
	- modellera bara det avgränsade problemet!
- Hur en modell värderas beror på hur den ska användas
	- Finns skillnad mellan att modellera systemet man hämtar data från vs ett mer allmän princip
	- val av analysmetod beror på förhållandet mellan det man vill förutsäga och historiken man använder för leta efter mönster
	- ***Finns tre viktiga typfall:***
	- 1. **Modellen som Prediktionsmaskin**
			- om stabilt system kan använda algoritmiska metoder för finna bästa beskrivning (både i struktur och parameterval)
			- stabilt = systemet fungerar på samma sätt i framtiden som under tiden data genererades
			- Bra modell = en som skapar riktig output med indata som inte använts under träning (*out of sample prediction*)
				- denna förmåga beskrivs av roc-kurva elr precision recall-kurva #läsmerkvaff
			- Maskininlärning vanligt för dessa tillämpningar
				- Ex stödvektormaskin (support vector machine), klassificeierar/skiljer datapunkter #läsmerkvaff
				- Random forest: aggregera flera beslutsträd t genomsnittsmodell
					- #clarifyKvaff s 41 hur random forest funkar, fatta inte riktigt #läsmerkvaff 
	- 2. **Modellen som systemrepresentation/beskrivning av systemdynamik**
			- om modellerar system som är förändligt måste förändringen modelleras utifrån teoretisk förståelse
			- =>Måste ha minne, bero på *tillståndsvariabler* som ändras över tid och som har påverkanssamband med andra tillståndsvariabler. Påverkanssamband kan beskrivas med parametrar/kunskap från tidigare undersökningar eller skattas
			- system är ofta system av differentialekvationer eller differensekvationer. matematiskt Komplexa, modellera ist med simuleringar => möjligt utforska utfall som går bortom observerade data
			- Dessa typer av modeller används ex för logistik, naturliga ekosystem
			- Bra modell i denna klass leder till insikt om hur underliggande system kommer bete sig i framtiden 
			- kan kanske göra [[analystyper|presktiptiv analys]] baserat på utfallen'
			- Enklaste form av denna typ av modell: länkade variabler med återkopplingsstruktur
	- 3. **Modellen som inferensverktyg**
			- Ibland inte datagenererande systemet som interessant utan underliggande principer som tar uttryck i systemet
			- ofta interesserad orsakssamaband/samvariation mellan två/flera faktorer
			- naturligt utgå från teoiretisk förståelse för modellera strukturen på system, skatta parametrar
				- I detta fall är det istället *parameterskattningarna* själva som är interessanta istället för prediktioner / dynamiken från modellen
				- ex skattning av koeffecienter i linjär regression  (?) för att påvisa sambandsstyrka

