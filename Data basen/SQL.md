
### Queries
ex motsvarande selection i relational algebra
- `SELECT * FROM Movies WHERE studioName = ’Disney’ AND year = 1990;`
- where följs av condition som måste uppnås
- select säger vad som ska tas
- from specefierar relation
- kan göra projection genom byta ut stjärnan

![[Pasted image 20251109180130.png]] $\iff$ ![[Pasted image 20251109180148.png]]

pattern matching med strings
- `s LIKE p`
- % = any sequence of characters, _ = en  karaktär
- ![[Pasted image 20251109181247.png]]
- `DATE 1948-05-14’

**Null values**
- unknown values
- innaplicable values
- withheld values

null i operations:
- + eller - eller liknande ger NULL
- comparasion ger UNKNOWN

x IS NULL är korrekt, x = NULL incorrect
ger det man kan lista ut när använder logical operators, ex TRUE or UNKOWN = TRUE

Vi kan också ordera output
![[Pasted image 20251109182637.png]]
ascending by default
![[Pasted image 20251109182702.png]]


### flera relations
- kan considera pairs av tuples genom sätta flera namn i FROM clausen ![[Pasted image 20251109183122.png]]
- om ska jämföra samma relation med sig själv, andvänd `AS` keyword (omittat i bilden)
	- ![[Pasted image 20251109183501.png]]

### Subqueries
kan nesta queries inne i andra queries and so on
- kan comparas i where clauses
- kan användas i from clauses
- ![[Pasted image 20251109184859.png]]
	- runtime error om mer än en tuple producas

### Conditions med relations
- relations måste då uttryckas som subqueries (`(SELECT * FROM FOO)`)
- EXISTS R sann om R inte tom
- s IN R om s finns i R (givet R är unary relation)
- s > ALL R sann om och endast om s större än alla element i unary R
- s > ANY R som det låter

om en tuple har lika många element/samma element som en relation kan man använda ovannämnda klauserna:
![[Pasted image 20251109192827.png]]

om en query behövs evalueras flera gånger, ex med input från outside queries har vi en *correlated subquery*

variabelnamn resolvas från det innersta scopet och utåt

kan också använda subqueries i from statement
- ![[Pasted image 20251109193838.png]]

### joins
producerar en egen relation så kan använda som subqueries
- CROSS JOIN är cartesian product
- kan använda ON för specifiera vilka tuples man vill behålla
	- ![[Pasted image 20251109194216.png]]
- natural joins
	- Dessa joinar tuples med samma värden i attributes med samma namn, en av attributera projectas out
		- NATURAL JOIN
	- NATURAL FULL OUTER JOIN tar med dangling tuples men paddar med NULL values där det krävs
		- kan byta ut outer mot left eller right join

## Full-relation operations
- Eliminatign duplicates
	- SQL tables är bags och inte sets, queries kan producera relations med duplicate tuples
	- kan tolka sql statement som först tar cartesian product av allt i FROM, sen testar WHERE condition på allt, sen projicerar i SELECT, vilket kan resultera i identiska tuples
		- SELECT DISTINCT tar bort duplicatesen
- duplicates tas bort by default i UNION, INTERSECT, EXCEPT operations, men ta med ALL efter om vill ha kvar allt
	- ![[Pasted image 20251113165359.png]]
	- ALL blir som bag semantics
- Aggregation
	- opperar ofta på en column av en relation 
	- ![[Pasted image 20251113165808.png]]
	- ![[Pasted image 20251113165823.png]] distinkta värden i kolumn X
- Grouping
	- ![[Pasted image 20251113170234.png]] (räknar utt summan av alla filmers längd för varje studio)
		- de enda termerna som kan komma efter select i aggregation är antingen aggregation terms, eller attribute names som förekommer i GROUP BY statement
	- group by query med flera realtions: ![[Pasted image 20251113170721.png]]
- grouping/aggregation med nulls
	- nulls ignoreras helt
	- average/sum of empty bag är null
	- coutn räknar inte null
- HAVING
	- Lägg till efter group by och med aggregations för att bara få önskade grupper
	- ![[Pasted image 20251113171312.png]]
	- endast attributes i GROUP BY list får appeara unaggregated i HAVING clause

## Database  modifications
Insertion
- ![[Pasted image 20251113171543.png]]
- kan också omitta attribute names om man orderar insertade values rätt:
	- ![[Pasted image 20251113171740.png]]
- kan byta ut VALUES mot en subquery
	- ![[Pasted image 20251113172042.png]]
	- omitted values i INTO statement blir NULL
	- SQL standard krävs att hela query evalueatas innan insertar in i tablet
Deletion
- ![[Pasted image 20251113172234.png]]
- ![[Pasted image 20251113172252.png]]
	- kan inte simply specify tuple to be deleted
Updates
- ![[Pasted image 20251113172405.png]]
	- varje assignment har identifier equal sign och ny värde, komma separerade om flera
- ![[Pasted image 20251113172455.png]]

## Transactions
- för att motverka race conditions
- en transaction är informally group of operations that need to be performed togheter
- kan specifya att transactions måste vara serializable = behave as they were run serially = one at a time, with no overlap
**Atomicity**
- Är operations som måste hända antingen fullständigt eller inte alls
	- Ex transfera pengar i en bank
	- lösning är att göra jobbet lokalt, sen commit changes till databasen, changes blir där visible för andra operations
- Transactions
	- är en mängd atomic operations. 
	- transcations måste köras serializably
	- I sql:
		- transaction är en grupp statements
		- START TRANSACTION; böjrar
		- COMMIT; avslutar transaction successfully
		- ROLLBACK; avslutar unsuccessfully och rollar back changes
		- kan signalera resad-only genom ![[Pasted image 20251113175002.png]], DBMS tar ofta advantage av detta
		- eller ![[Pasted image 20251113175010.png]]
		- dirty data = data changed/inserted av ocommittad transaction
			- dirty read är läsning av denna data
			- nackdelar med preventa dirty reads:
				- ![[Pasted image 20251113175158.png]]
			- kan tillåta dirty reads:
				- ![[Pasted image 20251113175617.png]]
				- read uncommitted = kan läsa dirty data
			- isolation levels:
				- finns fyra:
					- serializable 
						- som att transactionens körs helt serially
					- repeatable read
						- samma query ger samma result om körd flera gånger, om inte phantom tuples = tuples som är newly inserted into the relation 
					- read commited
						- Får läsa data committed av andra transactions. Kan få olika svar från samma query mid transaction
					- read uncommitted
						- Får göra dirty reads
				- Concurrency och performance ökar i varje level men safety och repeatability minskar
				- ![[Pasted image 20251113181000.png]]

# Constraints and triggers
- skapar active elements = lagras i databasen och executas at appropriate time
**Foreign keys**
- Finns policies för ändringar / deletion:
	- Default: runtime errors kastas
	- Cascade: Updaterar / deletear de tuplesarna som referencar med foreign key
	- set-null: sätt fields som är foreign key till null om det de referencar ändras/raderas
- Deferred checks
	- för att ex undvika att circular references för foreign keys gör det omöjligt att inserta värden
	- skriver DEFERABLE efter constraint declaration![[Pasted image 20251113193310.png]]

**Check constraints**
- attribute based berör bara en attribute och kollas när den attribtuen uppdateras
	- kan innebära problem när involverar subqueries, eftersom de inte reevaluatas när relationsen de referencas ändras
- tuple based involverar fler attribtues och evaluatas när tuple ändras/insertas
	- samma problem som ovan kan uppstå
- kan ändra named constraints ![[Pasted image 20251113194451.png]]
- kan namnge constraints ![[Pasted image 20251113194521.png]]

**Triggers/Assertions**
- assertions
	- är statments som är del av database schema och som alltid måste vara sanna
	- ![[Pasted image 20251113194929.png]]
	- ![[Pasted image 20251113195108.png]]
	- ![[Pasted image 20251113195121.png]]
		- ekvivalent med ![[Pasted image 20251113195208.png]]

- triggers
	- en sequence actions som callas när en viss event händer, ex insertion deletion update transaction end
		- testar sen condition
		- om condition holds gör man något
- settings/options för triggers i SQL:
	- condition och action kan executas på state innan triggering event eller state efter
	- kan refera till old/new values of tuples
	- kan definaa events som limited till particular (set of) attribtues
	- kan specifya om trigger executar once for each modified tuple (row-level trigger) eller en gång för alla tuples changed in statement (statement-level trigger)
	- ![[Pasted image 20251113200124.png]]