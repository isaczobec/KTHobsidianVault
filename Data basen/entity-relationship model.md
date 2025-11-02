
ett sätt att representera structure of data graphically, med
1. entity sets
	1. entity är abstract object of some sort, entity sätt är grupp av liknande objekt, lite som en class
	2. ex är movie en entity, set of all movies är en entity set
2. attributes
	1. saker som varje entity har, ex movie entity har length och title
	2. assumar att attributes har primitive types
3. relationships
	1. är en connection mellan två eller flera entity sets
	2. är som relations från basmatten

Entity-relationship diagrams
- olika former för relationships, entity sets och attributes, i en graf

relationship set for R är set av tuples där varje tuple innehåller entities som är related

Multiplicity of binary E/R relationships
- by default ingen limit på hur många element i E ett element i F kan ha relationen R till
- Many to one from E to F: varje entity i E kan vara related till max en i F
- one to one om båda kopplade till max en från andra settet
- many to many om vardera
- pilar till / FDs visar att någon entity set blir en funktion av andra genom relationen, eftersom uniquely determined

multiway relationships
- mer än två entity sets
- för att beskriva alla situationer måste man använda set of FDs istället för pilar

Roles in relationships
- Varje entity kan appeara multiple times, skriv ut roller längst med sidan av diagramet

relationsships kan ha attributes om de är unika för relationen
- dessa för vara functionally determined av någon kombination av entity setsen involved, inte en enda
- dock aldrig necessay - kan istället lägga till ny entity set med attributen och involva den i relationen

subclasses
- om vissa entities har extra attributes definierar vi en till entity set med dessa, och har en one to one *isa* relationship som kopplar dessa. triangel form
- en entity kan tillhöra flera subclasses/vara relaterade till flera

design principles
- faithfulness till reality
- säg inte samma sak flera gånger, ex ha inte samma attribute på två olika entity sets som är related
	- kan leda till wasted space eller update-anomaly
- ha inte onödigt kompliecerade structures, ex ha inte en useless one to one relation

### Choosing the right relationships
- ta inte med redundant relationships vars existens kan deducas från andra

Kan byta ut en entity set med attributes om
- All relationsships involving E are many to one (e is *one*)
- den enda keyn för E är alla attributes
- No relationsship involves E more than once
för att byta:
- Lägg alla attributes i E till R
- Om multiway relation med E, ta strecket mellan E och R

### constraints
Keys
- är som keys i relational model
- varje entity set måste ha en key
- brukar ta bara en key och kalla primary key även om finns många'
- om isa-hierarchy måste nyckeln finnas i roten
- måste vara unika

Referential integrity
- rounded arrow visar man to one och referential integrity

Degree constraints
- har exmepelvis en <= 10 symbol vi en entity set och relation, visar connected till max 10 sådana entities genom relationshippen

## Weak entity set
om en entity sets key är composed of attributes some or all belonging to another entity set
- för att bli uniquely named måste de ha attribute från någon annan entity de är relaterad till (many to one)
- keyn för en weak entity set är 0 eller fler egna attributes och key attributes från sets (supporting entity sets) som de når genom many-one relationships=supporting relationsship
för att vara supporting relationship:
- Binary many to one
- referential integrity
- keys för E måste vara keys av F (eller rekursivt en "parent" av F om F också är weak)
- kan ha komponenter av nyckeln från olika element i F om har flera supporting relationsships

## From E/R Diagrams to Relational Designs
- för att converta:
	- Turn each entity set into a relation with same attribute
	- replace relationship by relation whoose attribute are keys for connected entity sets
	- kan ex merge entity sets och many to one relantionship med någon annan entity set
- för converta relationsship
	- ta key attributes från båda, och attributer av relationsshippen om de finns
	- renama entities attributes om de ingår flera gånger

om har en many to one från E till F,
- kombinera R och E genom ta alla attributes från E, key attribs från F, och alla attributes av R

För göra relations från weak entity sets
- relation måste innehålla attributes från weak entity set W och också key attributes från supporting sets
- alla relationships där W ingår måste dess key vara alla attribut som utgör keyn för W, inte bara de i W
- supporting relationship måste inte nödvändigtvis bli en relation, kan bli attributes istället som nämnt ovan

• If W is a weak entity set, construct for W a relation whose schema consists of: 1. All attributes of W. 2. All attributes of supporting relationships for W. 3. For each supporting relationship for W , say a many-one relationship from W to entity set E, all the key attributes of E. • Do not construct a relation for any supporting relationship for W.

## Converting subclass heirarchys to relations
tre sätt:
1. en relation per entity set E med keys från rooten och attributes från E
	1. ingen relation för *isa* relationshipen
2. för varje möjligt subtree, skapa en relation med alla attributes
3. Null values: null på alla attributes entity inte har

s. 169 om comparision av dessa

se också [[UML]]