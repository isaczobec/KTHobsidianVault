#DataProcessing
en del av the [[data science]] process

två typer data:
- company data
	- collected och använd av företag för göra så de kan ta data-driven desicions
- open data
	- Alla har tillgång

vi genererar massa data genom att använda services
- företag som ger service samlar denna data i ovannämnda syfte

### Company data
- kan vara 
	- web events
	- survey data
	- customer data
	- logistics data
	- financial desicions


### Open data
- kan vara
	- APIs
	- Public records
		- från olika institut, ex universitet
	- Finns internationella / nationella organisationer som ger data


### DATA TYPES
- ***Två genrerella typer av data:***
	- Numerisk (quantitative)
		- Sånt som kan bli mätt, expressed using numbers
		- Kan vara diskret eller kontinuerlig
			- bara integer values om diskret?
	- Categorical (qualitative)
		- deskriptiv, conceptuell
		- Inte alltid en underliggande storhet som existerar?
		- Kan vara nominal eller ordinal
			- Nominal har ingen ordning eller numerisk värde
				- Hårfärg, religion
			- Ordinal kan ordnas
				- Ex betyg, education level
- ![[Pasted image 20250224110238.png]]
	- Dessa är essentiellt blandningar av kvalitativ/kvantitativ data


### Data storing and retreiving
- hur ska man lagra och ta ut insamlade datan?
	- **Location**
		- Kan använda single/cluster av datorer/servers beroende på mängden data
		- Cloud storage
			- azure, AWS, google cloud
	- **Data type**
		- Olika data types lagras på olika sätt
			- *Ostrukturerad data* =  email text image etc
				- Non relational databases, NoSQL
				- Länkade tables, joins, queries
			- *Strukturerad data* = Information som kan lagras i tabeller, ex xlsx eller csv-format
				- Relational databases, SQL
				- Mer komplex  flexibel manner av storing, kan accessa snabbt o effektivt
