
en [[data model]]
based on tables/relations
finns olika sätt att fysiskt implementera relations

operations är ex fråga om alla tuples med ett specefikt värde som en attribut

constraints är ex att det finns set tillåtna värden för en attribute

finns också *object-relational model*,
- values kan ha structure
- relations kan ha methods

relational bra eftersom simple och limited approach som ändå är veritile
- programmen man skriver är simpla, och kan också därför implementeras effektivt under the hood

Några saker i structuren
- Schema
= name och set of attributes for a relation
- Tuple
en row i en relation, en componennt för varje attribute

## Domains
relational model kräver varje component av tuple ska vara atomic = elementary data type
- varje attribute i en relation behöver en domain = particular specefied elementary data type
	- som domain i matte
	- domain brukar ingå i schema

### Equivalent representations of a relation
relations tuples har ingen order; relation är set of tuples

om ändrar ordning på attributes/headers, måste permutata alla tuples på samma sätt
dock är olika ordningar på attributes i relations ekvivalent

### Relation instances
- relations inte static, exepect change
- changes eller deletion av tuples
- schema ändras inte lika ofta
	- dyrt att ändra/ta bort/lägga till attribtutes

### keys of relations
- En subset av attributes form key om man inte låter alla vara samma för any two tuples

## Relations in SQL
- tre typer:
	- stored relations = tables
		- exists in database, can be modified and querid. Normal
	- Views
		- inte stored men contructed by computation when needed
	- Temporary tables
		- Inte stored men created by SQL language processor när executar queries och data modifications, thrown away

SQL primitive data types:
- `CHAR(n)`
- `VARCHAR(n)`
	- Variable length??? ingen padding??
- `VARCHAR(n)`
- `BIT(n)`
- `BIT VARYING(n)` = up to n bits
- `BOOLEAN` = true/fale/unknown'
- `INT/INTEGER`
- `SHORTINT`
- `FLOAT/REAL`
- `DOUBLE PRECISION`
- `DECIMAL(n,d)`
- `DATE`
- `TIME`

se [[algebraic query language]]

## COnstrains on relations
- kan använda uttryck från relational algebra för att uttrycka constraints

- referential integrity constraint
	- asserts a value appearing in one relation appears in some other related context
	- ex $\pi_A(R) \subset \pi_B(S)$
		- ex om ett värde dyker upp i R måste det dyka upp i B

- key constraints
	- ofta att en cartesian product av en relation med sig själv där man selectar alla tuples med samma unique key bör bli tomma mängden

andra constraints:
- kan ha tillåtna värden för en attribute
- kan också theta joina och sen välja otillåtna värden, asserta är tom