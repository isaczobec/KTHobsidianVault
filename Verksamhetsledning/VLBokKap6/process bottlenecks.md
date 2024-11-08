#VLBokKap6
Är en aktivitet/stage i en [[process]] där innefektivitet skapas eftersom att workloaden är större än kapaciteten
- eller mest overloaded del av aktivitet

Bra bild med exempel S 201

balancing är att allocata work equally mellan stages

### Balancing work time allocation
måste respektera precedence av work tasks när allokerar arbete till process stages
- kan räkna ut required cycle time
- sedan räkna ut total work content, dela med required cycle time och ta ceil för att få required stages, och sortera in activities i stages vars tid inte överstiger cycle time

### Arranging the stages
för att få samma cycle time kan man arrangera en lång lina stages i en [[process]] i flera kortare flöden
- = Long-thin (respektive short-fat)
- Fördelar Long-Thin:
	- kontrollerat flöde, easy to manage
	- simple handling, speciellt om föremål svåra att flytta
	- mindre kapitalintensivt jämfört med om dyra maskiner hade krävts i flera linjer
	- högre proportion av produktivt-inte produktivt arbete
- Fördelar Short-Fat:
	- högre flexibilitet att arbeta på olika typer av produkter/speciallisera sig
	- högre flexibilitet med volym - kan lägga till/ta bort ist för ombalansera
	- Mer robust - om en stage går sönder kan fof producera, long thin hade kollapsat helt
	- Mindre monotont arbete

