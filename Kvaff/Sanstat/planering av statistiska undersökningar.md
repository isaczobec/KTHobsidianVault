
## Allmänt om planering
- planering viktig eftersom man i planeringsstadiet kan påverka valet av teoretisk modell för data som kommer fram
- kanvid god planering välja modell som möjiggör klara slutsatser 
- mer än bara storlek som påverkar undersöknings kvalitet
- lägg upp plan som är så bra som möjlig med tillgängliga resurser
	- enkla övervägningar kan lösa sådana frågor
- behöver både statistisker och folk som är insatta i undersökta processen -> lagarbete gör gott
- **List med ungefärliga etapper för planeringsarbete:**
- ![[Pasted image 20250208191338.png]]

- Finns betydande skillnader i planeringsarbete mellan jämförande och icke-jämförande undersökningar


## Icke-jämförande undersökningar
- önskar information om någon okänd storhet inom någon disciplin
- måste ta ett stickprov med n element från målpopulationen
	- om fysiska element kallas det *enkelt urval*
- **För att kunna ställa upp användbar modell måste några krav ställas på stickprovstagningen**:
	- 1. ***måste vara slumpmässig***
		- om ändlig population som går att numrera gör slumptalsteknik
		- annars får göra på något annat sätt
		- ibland kanske inte går att ta slumpmässigt element - går då att använda slumpmodell?
			- avgörande för om kan betraka som slumpmässigt dragna är om experiment är reproducerbart
		- ofta svårt att avgöra vilken population observationerna/stickprovet kommer från (ex medecinstudier på ett enskilt sjukhus). Måste klargöra vad man menar med att datamängd är slumpmässigt stickprov från en population
		- om inte kan garantera slumpmässighet krävs stor erfarenhet för att avgöra vilka slutsatser som är giltiga att göra
	- 2. ***störande faktorer får inte förekomma***
		- inga systematiska fel får finnas
		- ex felkalibrerat instrument ger felaktigt resultat oavsett antal mätningar
			- -> är en *störande faktor*
		- bortfall (elementen i populationen som inte upträder i stickprovet) kan påverka ndersökning
			- Små bortfal % kan ibland vara devestating
		- egentligen ouppnåeligt att inte ha några störande faktorer, snarare ska de inte påverka slutsatserna
- #### Flera stickprov
- Ibland samlar man stickprov från $k$ olika populationer 
- mer omfattade planering eftersom måste välja hur insamlingen ska fördelas över olika stickprov
- Kan göra ***Stratifierad undersökning***
	- = dela in populationer i k delpopulationer efter någon förmåga, ta stickprov från varje
	- om väljer storlek på stickproven lämpligt kan ofta lättare få önskad information om hela popualtionen än om tar ett enda stickprov från hela populationen
- ***matematisk beskrivning av hur göra stratifierade undersökningar och varför de är bra kring sidan 382*** #läsmerkvaff

## Jämförande undersökningar
- undersöka olika "behandlingar"
- två typer: *jämförande experimentell undersökning*: kontroll över hur behandlningarna fördelas på de i undersökningen ingående experimenten, om inte är det *jämförande icke-experimentell undersökning*
	- förstnämnda ger säkrare slutsatser, kan eleminera störande faktorer
- #### Funnständigt randomiserat experiment
	- behandlingarna fördelas slumpmässigt på ingående elementen
	- -> Jämförelsen påverkas inte systematiskt av störande faktorer
	- när planerar för längd på konfidensintervall genom antal observationer kan man ex optimera för kostnad
- #### Randomiserat blockexperiment
- om stora skillnader mellan elementen, kan dela in de parvis efter vilka objekt som liknar varandra, och sedan ge varje par antingen A- eller B-behandlingen
- -> Kan jämföra skillnader inom block utan att skillnader mellan blocken påvekar
	- kan sedan använda stickprov i par (normalfördelningsantagande)
	- 