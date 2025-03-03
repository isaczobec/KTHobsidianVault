#KvaffKap8
Analytikers uppgift ofta att göra förutsägningar om framtid snarare än endast blottlägga underliggande orsak-verkan samband
- risk göra felaktiga prognoser om bristfällig kunskap om kausala samband

## Validering
- För god prediktion behöver en modell som ligger nära verkliga datagenererande processen
	- I process skapa denna modell hjälper förståelse för den processen
	- Kan också ta an prediktionsproblem genom helt enkelt träna ML algoritm
		- Under antagande att systemet inte förändras för mycket över tid, att träningsdatan är representativ för framtiden, kan man uttnyttja modell utan djupare insikt i hur den fungerar eller vad den säger om underliggande process
			- processen blir då "Svart låda", vi bryr oss bara om indata utdata
			- Om har ett ickeförändrande system finns här fördel att man tydligt kan mäta precision hos maskininlärningsalgoritm: Hur bra kan den göra precisa prediktioner på dataset det inte tränats på? = out of sample prediction 
				- kan dela upp dataset i ex 70-30 procent, 70% för träna 30% för utvärdera
				- Validering enligt samma principer kan göra för optimera modellval genom att kolla deras presicion på samma sätt
					- kan undvika dataförlust kan man använda korsvalidering: dela upp dataset i olika delar som sätts ihop t flera träninigsset ch testset

## Skillnader mellan [[analystyper|deskriptiv, prediktiv och preskriptiv analys]]
- säger ofta komplexitet ökar fr deskriptiv prediktiv preskriptiv
- Ofta analytikers mål att säga något om framtiden
	- inte omöjligt att göra detta med deskriptiv analys: Kan hitta/beskriva mönster och argumentera varför de kommer upprepa sig i framtiden
- I andra frågeställningar krävs kartläggning av kausala samband för koppla handlingsalternativ till utfall
	- Detta kallas ibland (något slarvigt) preskriptiv analys
	- Kan dock också vara grund för prediktion, om modell har extern validitet och fångar upp ansenlig del av datagenererande processen
	- En skillnad när man försöker göra en enskild förutsägelse/prognos är att man kan göra starkare antaganden om stabilitet i datagenererande processen och ist för validitet maximera reliabilitet
		- Detta fokus reliabilitet kan ofta leda till enkla modeller, men de kan ofta ha högre precision av prediktion av framtiden jämfört med komplexa modeller som representerar underliggande kausala samband
	- Prognosmodeller är dock ofta väldigt komplicerade, kan söka efter optimal metod med algoritmer

## Prediktionsförmåga
- Kan mätas i MSE, eller standardavvikelse (lätttolkad eftersom har samma enhet som storheten man undersöker)
- R2-måttet säger hur stor andel av den totala variationen i beroende variabeln som förklaras av modellen
	- Är bra för jämförelse/utvärdering mellan prediktionsmodeller
- Om dikotoma eller kategoriska klasificieringar (utifrån andra mätvärden från en datapunkt) är det man söker kan man mäta prediktionsförmåga som andel korrekta klassificieringar
- bör göra avvägningar mellan positiva och negativa klassificieringar: Om värre med falsk negativ/positiv bör man favoura den andra
- Kan använda ROC-kurva för att visa dessa klassificieringar, y axeln visar andel positiva fall som klassas som positiva, x-axeln andel negativa fall som klassas som positiva
- Kan istället ha presicion-recall-kurva: Horisontell axel har mått för hur stor andel av alla observationer som klassas som positiva som är korrekt klassificierade #clarifyKvaff 
- Dessa kurvor kan simplifieras som AUC (area under the curve) fr 0 t 1, värde nära 1 visar att nästan alla mätpunkter som klassas som positiva verkligen är positiva

## Prognosmodeller
- Kan använda många olika verktyg när man ska göra prognoser av framtiden
- regressionsmodeller m mkm ofta dåliga för tidsserier eftersom framtida utfall ofta beror på tidigare utfall
	- Dessa har så kallad autokorrelation, de beroendena bryter mot "antagandet om oberoende feltermer i gauss-markov-villkoren"
	- autokorrelation – utfall påverkas av ett eller flera tidigare utfall
	- riskerar underskatta standardfelen
	- måste modellera autokorrelation med prognosmodeller som ARCH och GARCH
		- Kan också använda enklare modeller
			- Ex exponential smoothing: Nästa värde i tidsserie är linjärinterpolation mellan prognosvärdet $L_{t-1}$ och senast uppmätt värde $Y_t$:
				- $L_t = \alpha Y_t + (1 - \alpha) L_{t-1}$
				- eftersom $L_{t-1}$ beräknas från tidigare värden är vår modell ett viktat medelvärde av mätserien, mer vikt senare delar i mätserien om $\alpha$ är högt
	- Holt-winters metod är mer komplicerat ekv-syst som bygger på att säsongsvariationer (eller trender) har återkommande påverkan (se s. 87 i boken)

- Dessa modeller är mellanting mellan rent prediktiva modeller och statiska modeller för testa hypoteser om kausala samband
- Utgår dock ofta från teoretisk förståelse för processen: fördel kan göra ändringar i funktionen/modellen 
	- Kan ex justera ner styrkan för parametrar som anger hur mycket försäljning som kommer ske om vi vet att det är lågkonjunktur
	- 