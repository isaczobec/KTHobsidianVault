#InteractionDesignKap12 
design, prototyping och konstruktion alla del av develop i [[Double diamond]]
prototyper facilitatar iterative design-evaluation-redisign cykler

finns två aspekter av design:
- Conceptual: handlar om iden om produkten, vad den kommer göra
- Concrete: detaljer om design, ex fysiska widgets och graphics
Dessa två behöver consideras för att kunna prototypa ideer, vilka evolvar konceptet

kvaliteen på prototyper ändras och utvecklas genom designprocessen

---
Prototyper ger manifestation av idée vilken tillåter designers kommunicera deras idéer och användare att prova de
- prototyper kan vara lite vad som helst

### Why prototype
- Tillåter kommunikation, evaluation av idéer och deras feasability, tydliggörande av vaga krav
-
- Finns skillnad product och service prototypes
	- service prototype involverar role playing och personer (vilka är integral del av prototypen och produkten själv)


### Low fidelity prototypes
- limited funcitonality, inte samma material som slutgilltiga produkt
- enkla, billiga att producera OCH ändra/iterera efter nyupptäcka krav
- bra tidigt i development, eftersom prototyper bör vara flexibla och uppmuntra exploration och modification
- en typ LOFI prototyp är storyboarding, en vidareutveckling av [[personas and scenarios|scenarios]] 
	- kan använda [[sketching]] för att göra ännu tydligare
- ##### andra typer av LOFI prototypes
	- Index cards: kort med element från produkten på sig
	- Wizard of oz: någon människa sitter och kontrollerar en digital prototype som användaren interagerar med

### High fidelity prototypes
- Ser mer ut som slutliga produkt och har mer ffunktionalitet
- ofta ökar fidelty av prototypes genom design stages
- att kunna använda prototypes i real context (in situ) kan ge bra insights o feedback, fördel m HIFI prototypes


### Kompromissar i prototyping
prototyping innebär alltid kompromissar, ex lofi så funkar sällan produkten som tänkt
- måste alltså fokusera på de frågor man vill ha svar på genom prototypen
- ***Två typer av prototyping:***
	- Horizontal prototyping: Många features men lite detail
	- Vertical prototyping: mycket djup/detaljer för några få funktioner
- Vanligt tradeoff är robusthet vs förmåga att förändra prototypen, ofta negativt korrelerade
- kompromiss av hifi-prototyp kan vara att users mindre beredda att kritisera produkt de percievar som färdig
- Behöver alltid mer rigorös testning än prototyping tillåter innan shippar
-
- Två filosofier av prototyping:
	- Evolutionary prototyping: prototype evolvas till slutgiltig produkt
	- Throwaway prototyping: Prototype är stepping stones för final design

### conceptual design
- conceptual model är view av vad kan göra med produkt, o koncept som behövs för att förstå produkten
	- det senare beror på vilka users komme vara, vilken interaction som behövs, etc
- huvvuddel i conceptual model är mapping mellan concept och user experience
- sätt att generera potential conceptual models:
	- ***Interface metaphors***
		- kombinera familiar och ny knowledge
		- kan göra det med metaforer
	- ***Interaction types***
		- vilken typ av interaction passar produkten bäst?
		- kommer kunna använda flera typer i en produkt
	- ***Interface types***
		- Bra tänka olika interfaces eftersom de supportar olika interface types
		- kan prova olika, vilken som väljs (kan) bero på vilka [[requirements]] som finns

#### Expanding the initial conceptual model
- måste fråga vilka funktioner användaren respektive produkten är ansvariga för
	- måste balansera så får rätt nivå av cognitive load/frihet hos användaren
- hur är funktioner relaterade; detta kan indikera suitable restrictions/task structures hos produkten
- tänk på data [[requirements]] i conceptual model

### Concrete design
- göra mer detaljerade val
- kan vara att deala med konkurerande [[requirements]]
- se till att usability and user experience goals möts, ex genom att välja interface type och design considerationsen som kommer med de; dessa är desiscions inom concrete design
- accesability också viktigt


## Generating prototypes
- STORYBOARDS s. 448
	- ta [[personas and scenarios|scenario]] och bryt ner till steps som fokar på interaction, en scen för varje step
	- storyboards kan fokusera både på själva produkten och environment
	- 
- CARD-BASED PROTOTYPES
	- för att förstå users interaction, ex exchanges mellan syst och användaren
	- Fördel att kan flytta kort för att simulera vad som kommer hända
	- Kan kombineras med expirence wheel / experience map (eller andra representationer), se s. 453


## Construction
- när prototyping och alternativa designs progressar kommer mer tid läggas på bygga ihop komponenter och utveckla final product
- kan ta fysisk/programvara form eller båda
- ***ovanligt att behöva utveckla allt fr scratch för supporta development, finns två resurstyper för hjälpa med detta***
	- **Physical computing kits**
		- bygga prototyper med fyska material, programering, chip, elektronik etc
		- ex arduino
	- **SDKs**
		- Package av programming tools som supportar development av applikationer
		- ofta IDE ingår


![[Pasted image 20250223185328.png]]