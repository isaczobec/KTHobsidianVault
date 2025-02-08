#KvaffKap3
## Reliabilitet:
- Att mätning av samma underliggande storhet ger samma utfall till stor grad oberoende av när, hur, var mätningar görs
- Mätningar konsistenta?

## Validitet:
- Hur väl våra mätvärden faktiskt mäter den underliggande storheten; 
- Ex våg med för tunga motvikter, låg validitet
- ofta svårare att utgöra än reliabilitet

Om den underliggande storheten kanske inte är förknippat med ett mått och en mätmetod (ex som mätning av vikt med våg är), ex pris kund villig att betala, kan mycket mätdata, många mätserier krävas för att få god validitet

Reliabilitet och validitet avgör tillsammans förutsättningar för att data ska kunna vara användbar i analys
- validitet - väntesvärdesriktigt?
- Måste ha hög reliabilitet för att ha hög validitet - för stort konfidensintervall gör att vi inte mäter rätt underliggande storhet lagom väl (?)
- kan vara filosofisk fråga att säga om dålig data beror på dålig reliabilitet/validitet

----
- väldigt vag skattning kan inte sägas ha hög validitet
	- ex om gjort för få observationer för skattning
	- stora talens lag
----
För bedömma om problem med [[reliabilitet och validitet]] måste bedömma hur data förhåller sig till den verklighet man undersöker
- = "*Att förstå den datagenererande processen*"
	- Denna ofta komplicerad och omöjlig att helt förstå, behöver modellera matematikst genom ex normalfördelning
- **förstå den datagerenerande processen kräver två typer förståelse:**
	- *god insikt i verkligheten interesserade av*
	- *insikt i metoder som används för att samla data*
	- exempel:
		- Mäta trafiken utanför skola morgonar under 30 min
			- dessa måste vara representativa av morgonar i framtiden
			- hög spridning; högre trafik fredagar
				- om inte inser detta skattar man för högt, måste ha insikt i verkligheten
				- Betingat väntevärde kan ofta mätas med högre validitet / reliabilitet
			- mer insikt gör att man kan välja bättre mått, bätre mätmetod
				- <-- man kan förbättra sätt att mäta, eller mäta faktorer som påverkar utfallen man är interesserad av


