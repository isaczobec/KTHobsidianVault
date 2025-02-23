#InteractionDesignKap11
statements om vad produkt/sustem ska göra o hur den ska göra det

- discovera requirements går ut på utforska problem space, definiera vad som ska utvecklas
	- = i interactionsdesign hur människors liv kan göras mer convenient av produkter 

eftersom [[process of interaction design]] iterativ nära linked process kommer evaluation, design, requirments vara nära relaterade
- Har dock olika mål och emfas

### What is the purpose of the requirements activity?
- Requirements-aktiviteten utgör två första faser i [[Double diamond]] och handlar om att utforska problem space, få insights i problemet, samt skapa beskrivning av vad som ska utvecklas
- Requirements kan discovras från targeted activities eller under ex prototyping och designfaser
- Requirements-activity är iterativ så att nyfunna insikter matas tillbaka i sig själva (?)
	- aktiviteten själv revisitas ofta

### How to capture requirements once they are captured?
- Hur strukturerat och formellt requirements måste vara definierade beror på komplexiteten av appen
	- ex workout monitoring app kan prototyp implicitly fånga requirements
	- Om ex mer komplext factory management system måste mer rigorös notation användas
- Kan dock vara bra att fånga requirements explicit så inte tappar något genom interationerna
- använd lämplig notation för reqiorments baserat på produkten

### Varför ska man samla requirements?
- Att definiera requirements gör så developers vet vad de ska bygga och att users kan hjälpa
- målet med iterativ [[User centered design]] med kontinuerlig evaluation och user involvement gör så att misskommunikation inte sker och så att produkten verkligen kommer uppfylla user requirements


## Vad är en requirement?
- statement om vad göra eller hur perform
	- om vaga requirements handlar requirements activity om att göra de tydligare, bryta ner i flera mål
	- requirements activity mål: identify, clarift, capture requirements.
		- Iteratict
		- kan också specefiera kriterier som visar att målen nåtts
- ***Hur skriva ner/fånga mål?***
	- Kan ha en requirements shell, som en mall man fyller i
	- *User stories*
		- kan vara meningar/beskrivningar av tänkta användare och vilket värde de vill få genom produkten
		- kan göra så att developers/stakeholders kommer koversera på ämnet
		- ![[Pasted image 20250223104559.png]]
		- vanligt i agile, ofta bas för en sprint
			- Mål, tid estimat, tester för att se att det funkar
		- user epics: väldigt stora user stories

### Different kinds of requirements
- reqs Kan komma från ex user community eller business community
- *Finns ett antal typer av reqs, varav de två översta är vanligast:*
	1. **Fuctional requirements**
		- vad produkten ska göra
		- basic facilities som måste finnas
	2. **Nonfunctional requirements**
		- characteristics av produkten
		- ex quality constraints, performance, usability
	- ![[Pasted image 20250223105219.png]]
	- ![[Pasted image 20250223105030.png]]
	1. **Data requirements**
		1. Typ, volatilitet, persistanec, size och krav på att handla data
	2. **Environmental requirments**
		1. Handlar om i vilken environment produkten ska operata
			1. finns ett antal aspekter av denna:
				1. physical envionment
					1. ex använd inte speech interface för public ATM, mycket snack i bg
				2. Social environment
					1. hur sammarbete inom produkten ska ske
				3. Organizational environment
					1. Ex finns träning tillgänglig, communication lätttillgänglig?
				4. Technical environment
					1. vad för technology anävnder produkten/ kommer användas i conjunction med?
	3. **user, usability, and user experience requirements**
		1. diskuteras i kap 2
		2. Kan använda usability engineering, välja meausers för hur mäta kvalitée tidigt i processen

Olika typer av produkter kommer alltid ha olika requirements

Se [[Data gathering for requirements]]