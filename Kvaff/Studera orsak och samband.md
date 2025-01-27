#KvaffKap6
Analytiker uppgift utoforska möjliga framtider, måste etablera ide om kausala samband orsak och verkan
--> Hur undersöka orssakssammanbad mellan två storheter?

## Hypotetisk-deduktiv vetenskap
klokt när studera orsak verkan amtt anväda *the scientific method*
- analys formas kring hypoteser som ankras i bästa möjliga befintliga uppfattning av fenomenet
- Interessant hypotes kan tydligt falsifieras, bestäm innan vilka observationer som leder t förkastning
- hypotes testas genom empirisk undersökning - analys, som ger underlag för slutsatser
	- för att komma ifrån ex confirmation bias
	- strukturerat arbete -> kan tydliggöra antaganden och slutsatsers validitet för sig själv/andra
	- hypotesprövande arbetssätt -> uppfattning endast kombination teoretiska idéer och empirisk undersökning som ger använbar kunskap
- arbete genom *scientific method* vanligt i naturvetenskap, lite mindre vanligt i samhällsvetenskap

- Om man tror på scientific method påverkar vilka analysmetoder man väljer
	- Ex om tror på det kan betrakta kvalitativa data som mindre tillförlitliga kvantitativa data
	- Andra menar enda kunskap är den man får genom djupt reflektera över process utan göra anspråk på orsakssamband
	- #clarifyKvaff allt detta var lite otydligt, s . 56
- svenska "vetenskapligt arbete" är bredare, "scientific method" = "hypotetisk-deduktiv ansats"
	- deduktiv - deduktiv logik grundad i teoretisk förståelse (eftersom x och y följer att...)**
		- Hypoteser följer från detta, **som sedan testas** 
	- skillnad fr induktiv logik, som bygger på empiriska observationer (pga mina observationer av x, y, ser vi...)
- Utan hypoteser grundad i teoretisk hypoteser blir sannolikheten för bias och feltolkningar under undersökningar av orsakssamband, ex att man tolkar slumpvisa mönster som res av kausala samband, och confirmation bias

## Ny teknik och gamla principer
- ai teknologi kan göra många analyser/slutsatser människor kan och kan göra 
- Dessa bygger ofta på väldigt stora datamängder --> induktiv logik tar större plats
	- detta ersätter inte scientific method/hypotetisk-deduktiv kunskap, eftersom vi inte kan säga att de upptäcka mönstrena ger ny *vetenskaplig* kunskap innan man har en (teoretisk) förklaring till varför mönstrena uppstår

## Kontrafaktisk analys
- etablerat att analytiker som vill testa orsakssamband bör ställa upp och testa hypoteser, men inte sagt vilken data som behövs
	- Grundprincip = slutsatser om detta kräver *kontrafaktisk analys*: Att vår data så långt som möjligt ska möjligöra analys om hur ett visst utfall hade blivit med en annan historik
- ### Krav på data för att möjliggöra analys om orsaksamband:
	- ***Data med variation***
		- ex om undersöker pris - efterfrågan
			- Omöjligt dra slutsatser om pris varit konstant
			- högre variation -> lättare att fånga upp effekter av pris på efterfrågan
			- extra stor variation om finns brus eller felkällor i mätning
				- om lite variation kan brus störa ut mönster
				- vill ha så mycket användbar variation som möjligt, högt signal-brusförhållande
				- mätfel och brus under kontroll -> mindre variation ok
				- Ex kommer osäkerhet i linjär regression genom att man vill dra slutsatser om underliggande population genom ett stickprov 
				- standardfel #clarifyKvaff fatatde inte riktigt vad det var
			- kan ex inte dra slutsatser om värden utanför range av variation
	- ***Data som möjliggör rekonstruktion av orsakssamband***
		- Detta innebär två tumregler:
			- Experimentella data är bättre än kvasi-experimentella data
				- experiementella data samlas in genom experiment
				- Idealfall: randomiserad kontrollstudie
					- = full tillgång till försöksobjekt. Väljer slumpmässigt ut ett stickprov, behandlar det, får data, och får resultat. Sen jämför resultat med kontrollgruppen (obehandlade gruppen), representerar kontrafaktiska utfallet
				- detta ideal ganska långt i från verkligheten utanför vetenskapliga studier, kan inte få den kontrollen
					- i detta fall får göra kvasi-experimentell ansats: samla in data från verklighet vi inte själva manipulerat och analysera den som att den vore experimentell
						- Kan inte isolera faktorer som är interesserad av, måste också samla data på alla faktorer som påverkar vår beroende variabel
						- kan då rensa bort trendar som irellevanta för studier (ex om pris ökar över tid och det inte är relevant för studien)
							- Om inte gör detta drar man felaktiga slutsatser om orsakssamband
				- mellanting mellan kvasi-experimentell och experimentell: studie som kan uttytja naturligt experiment
					- om system av intresse haft exogen (yttre) påverkan, som ändrat ex variabler vi intresserade av, kommer närmare "allt annat lika" analys man kan få i labb
					- Ex om studerar pris-efterfrågan elpriser: EU-lagändring som höjer elpriser är exogen påverkan, låter oss studera allt annat lika
						- Annan variation som ändrar priset kan eventuellt vara sammankopplad med priset också, mindre [[reliabilitet och validitet|validitet]]
			- Paneldata är bättre än tvärsnittsdata
				- Tvärsnittsdata: Data från många observationsenheter, men bara vid ett tillfälle (tvärsektionellt)
				- Paneldata: Data från många observationsenheter, vid flera tillfällen (i tiden)
				- Paneldata bättre för att
					- Data över tid kan användas för skatta samband
					- Mer variation ger mer precisa skattningar
					- kan fokusera på skillnader över tid hos enskilda observationsenheter, hitta saker/eleminera vissa faktorer som är tidsinvarianta

## Triangulering och komplementerande analyser
- Komplementerande delanalyser för en närmare målet att formulera pålitliga orsak-verkan-samband
- Kan göra placeboförsök:
	- Ge randomiserad kontrollgrupp en behandling som antas inte ha någon verkan, se vilka resultat det får (se så att det faktiskt inte har någon verkan)
	- bra exempel lottvinnare s. 62

## [[reliabilitet och validitet]] för samvariation och kausalitet
- reliabilitet = spridningsmått (varians, standardavvikelse) på punktskattning av beroendemått (kovarians, korrelationskoeffecient, regressionskoeffecient) kan användas
- Validitetet behandlas som två separata frågor: Intern och Extern validitet:
	- Intern validitet
		- finna giltiga samband för den egenskap vi vill studera hos populationen vi studerar
	- Extern validitet
		- Hur representativ av målpopulationen är den populationen (stickprovet) vi har valt?
		- Blir ofta fråga om hur långt resultat kan generaliseras
			- ex kan inte generalisera resultat om sömns vikt för studier till sömns vikt generellt
		- Många studier har problem med detta, samband i testmiljö men inte utanför den (ex i samhällsvetenskap, etc etc)