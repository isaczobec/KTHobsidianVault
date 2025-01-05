#VLBokKap11
= aktiviteten att förstå naturen av supply and demand och copa med deras missmatches i [[operations]]

ska minska competing demands av custoomer satisfaction och resource efficiency

capacity desiscions görs med constraints på operations och supply in min

medium term capacity management ex att variera mängd output genom hur mycket alla arbetar
short term capacity management är att copa med kortsiktiga avvikelser
![[Pasted image 20241223181551.png]]

## capacity management affects performance objectives
- cost: ex högre capacity än demand ger höga unit costs
- revenue: motsatt korrelation: lagom hög kapacitet gör att ingen produktion går förlorad
- working capital: kan bygga upp stort lager om producerar innan demand, måste kunna funda detta lager
- Quality: om gör stora ändringar för copa med stora flucuations kan kvalitee ändras, ex hiring temp staff ökar risk errors
- Speed: kan ökas genom surplus capacity eller buildup av inventory
- Dependability: om demand nära capacity ceiling blir ability copa med disruptions mindre
- Flexibility: ökar med surplus capacity, minskar om demand och kapacitet exakt matched

## Framework for capacity management
- första steg predicta future demand i olika tidsperioder
	- välj rätt kvalitativa och kvantitativa redskap
- andra steg förutspå hur stor kapaciteten/möjlighet skapa supply kommer vara
- tredje steg kolla om kan använda demand management
- fjärde steg är bestämma appropriate capacity och om den ska hållas konstant eller varieras med demand
![[Pasted image 20241223183139.png]]

### How is demand measured?
- bör veta demand över olika timeframes och rate of change av demand, så vet när man ska ta action

#### Qualitative approaches to forecasting
- **Panel approach**
	- många personer som är kunniga i ämnet kommer tillsammans och diskuterar
	- många personers åsikt bättre än en, men kan bli mest högljudda eller hög status åsikt som vinner
	- alla kan ha fel
- **Delphi approach**
	- istället har man en grupp experts som själva kommer på lösningar, skickar en survey till de
	- sen får de anonymt läsa varandras svar och omvärdera, iterativt många gånger
	- ska narrowa ner möjligheterna
	- problem är skapa rätt questionnaire och välja rätt panel of experts
- **Scenario planning**
	- för long range planning och stor uncertainty
	- en panel skapas, de diskuterar möjlgia scenarion
	- inte concerned necesairly med hitta consencus, men att sätta bra planer i ljus för att minska sannolikheten att välja dåliga

#### Quantitative approaches to forecasting
- **Time-series analysis**
	- kolla tidigare data, ta bort variationer pga känd variabler, och använd det för att extrapolera future behaviour
- Skippade de andra, de var inte med på läshänvisningarna #skipped



---

### How is capacity measured?
- capacitet är max nivå av value added activity över en tidsperiod som normalt kan ådstakommas
- när gör ny investering är man intereserad i hur många fler produkter som actually kan bli processade, men väntetider och olika variationer i åtanke
- -
- kan vara svårt att definiera kapacitet om inte standardiserad och repetetiv process
	- när det går och outputs natur inte varierar kan man ha *output capacity measures*: ex units/hour
	- om har hög vareity och krav på varierbara [[process]]er kan *input capacity measures* vara bättre: ex antal sängar tillgängliga i hotel

- Vad [[operations]] gör påverkar om kapacitet kan mätas
	- output beror ex på mix av aktiviteter, om de är varierade blir svårt mäta output exakt
	- Kan använda aggregated capacity measures för att minska detta

- Viktigt att mäta kapacitet över olika time frames
	- max kapacitet möjligt är inte alltid en sustainable kapacitet: ex overworking
	- kan ha tre mått när mäter kapacitet:
		- Design capacity: det man teoriskt sätt kan uppnå utan losses
		- Effective capacite: med planned losses i åtanke
		- Actual output: Vad man har i verkligheten, efter unplanned losses
	- utulisation = actual output / design capacity
	- Efficiency = actual output / effective capacity
- **Capacity leakage**
	- denna loss i kapacity som orsakas av predictable/unpredictable kallas capacity leakage och kan mätas genom Overall equipment effectiveness (OEE): a x p x q
		- a = availability of the process
		- p = performance or speed of process
		- q = quality it creates
	- avaliability kan minska m ställtider, absence, eller breakdowns
	- speed kan minska med idling eller inte optimum speed
	- quality minskar capacity eftersom måste ha kvalitetskontroller etc
	- för process att vara effektiv måste ha alla dessa, tillsammans ger de bra översikt över kapaciteten
	- ![[Pasted image 20241223210123.png]]
- **Understanding changes in capacity**
	- vissa businesses har inte stabil capacity, möjlighet att skapa supply
	- ex om en crop inte harvestas hela året runt
	- deala med gaps mellan demand och supply är capacity managements uppgift

### How is the demand side managed?
- måste försöka få demand att mer closely matcha kapacitet
	- kan göra detta genom stimulera off-peak demand eller constraina peak demand
	- några metoder för detta:
		- Price differentials
			- ändra priset över tid: högt när hög demand, låg när låg
		- Scheduling promotion
			- promota när inte är säsong
		- Constraining customer access
			- tillåt bara access ibland, ex genom reservation/appointment systems
		- Service differentials
			- ge bättre service i låd demand period, sämre i högre demand period (?) 
		- Creating alternate products or services
			- nya produkter som fyller demand i quiet periods



## How can operations understand the consequences of their capacity management desiscions?
- capacity management innebär balansera förmåga tillgodose kundbehov och minimera kostnader
	- ex använder man demand management för göra detta
- måste assesa konsekvenser av beslut om capacity management plans, **fyra (4) vanliga sätt**:
	1. **factoring in predictable vs unpredictable demand variation**
		- om predictable change i demand, justera kapacitet accordingly
		- om unpredictable change i demand, måste reagera snabbt för ska få någon verkan
		- ![[Pasted image 20241223210402.png]]
	2.  **using cumulative representations of demand and capacity**
		- måste se till att cumulative production alltid ska ligga över cumulative demand
		- tänk på att det kostar att ha inventory
		- skippade det om chase capacity plans s. 384 #skipped 
		- ![[Pasted image 20241225122247.png|300]]
	1. **using queueing principles to make capacity management desiscions**
		1. bra om man inte kan stora sina outputs, ex service organisations
		2. använd queueing theory
			1. ibland får kunder service direkt, ibland måste vänta
			2. kunder kommer t servers som processar de under en viss tid, allt enligt olika probability distributions
			3. *några element som definierar queueing behaviour:*
				1. The sources of customers
					1. om de är infinite eller finite
					2. om finite påverkar sannolikheten av nya customers av de som redan servicas
				2. servers
					1. kan vara i parallel eller series, eller en komplex web
					2. kan vara maskiner/stationer/personer
					3. service time varierar
				3. the arrival rate
					1. varierar
				4. the queue
					1. kan vara infinite
					2. måste inte vara fysisk, kan vara vänta på fysisk produkt
				5. queue discipline
					1. vilka [[sequencing]] rules som används
				6. rejecting
					1. om man nekar någon access, ex under hög demand
				7. balking
					1. att inte gå in i queue för att det tar för lång tid
				8. reneging
					1. Att exita queue av samma anledning
		3. Variability effects on queues
			1. måste matcha kapacitet och demand här också
			2. även om samma average kapacitet och demand kommer underutulization/överbelastning inträffa tack vare variabilitet
		4. Customer perceptions on queuing
			1. kan försöka bättra experiencen av att vara i en queue
	2. **taking a longitudinal perspective that considers short and long term outlooks**
		1. capacity management är inte bara att planera capacity utan också att kortsiktigt reagera på changes
		2. lär sig från tidigare perioder av capacity management
		3. ta beslut baserat på kombinationen av short term och long term outlook for volume
		4. ![[Pasted image 20241223210653.png]]

#skipped  supplement till ch11, analytical queing models s.399 #frågaomtentan kommer på tentan?

