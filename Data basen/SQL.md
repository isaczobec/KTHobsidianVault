
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