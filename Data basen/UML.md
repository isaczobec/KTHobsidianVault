
## Classes
- som ER entity sets
- kan ha metoder
- PK efter members i key (primary key)

## Associations
- som relationsships, men måste vara binary
	- får bryta ned multiway 
- har label som avgör rangen av tillåtna ingående relationsships
- kan ha associations till sig själv
**association classes**
- som klasser som läggs till emellan associations

## Subclasses
- primary key kommer från root of hierarchy som i ER
- kan vara
	- complete vs partial: complete om objekt måste tillhöra en subclass
	- disjoint vs overlapping: om kan vara flera subklasser samtidigt
	- gör dessa deiscisons i varje nivå av hierarchu
- assumar har samma relationships och attributes som superclasses
- open arrow för subclass

## Aggregation & composition
- som association fast many to one där one är där det finns en diamond
- aggregation = öppen diamond = <= 1 koppling
- composition = closed diamond = exakt en koppling

## UML -> Relations
- classes -> relations
- associations -> relations genom att använda keys från båda klasser som attributes, och attributes för associationen
- för subclasses:
	- om disjoint överallt, ta object oriented representation
	- om disjoint och complete överallt, ta oo representation. Behöver bara relation för leaves
	- Om hierarchy är large and overlapping ta E/R
- för aggregations & compositions
	- kombinera som på samma sätt med many to one för E/R

## analog of weak entity sets
- antar att alla objekt är unika som i oop
- kan dock ha supporting classes om man skriver PK vid de, och har en many to one referentially integrity relationship med en supporting class
- ![[Pasted image 20251028194845.png]]