
Är en statement att om två tuples aggerar på en delmängd A av alla attributes måste de aggrea på en delmängd B av alla attributes
- A functionally determines B
- "R satisfies the functional dependency"
- för att vara en FD måste påståendet stämma för alla möjliga tänkbara instanser av en relation R

En delmängd av attributes är en key av en relation om de functionally determines alla andra attributer, och ingen proper delmängd functionally determines all other attributes
- två distinkta tupples kan omöjligen aggrea on alla attributer som tillhör keyn

kan ha mer än en key, väljer då ofta en primary key

superkey är en subset av attributes som innehåller en key
- behöver inte vara minimal
- alla keys är superkeys

två sets of FDs är equivalent om set of relation instances som satisfyar båda är exakt samma
- <=> två sets av FDs följer av varandra

En constraint är trivial om håller för alla instanser av R oavsett andra constraints
- alla FDs där högre sidan delmängd av vänstra är triviala
- kan ta bort alla attributes på högra sidan som också är på vänstra, ekvivalent

closure of a set of attributes and a given set of FDs S:
- a set of attributes B such that all instances of a relation satisfying all FDs in S also satisfy A1,A2,.. -> B
	- det som alla A functionally determinar följande av S
- closure är alla attributes endast om alla A:n är en superkey

FD är transistive

en equivalent set of FDs T till S är en *basis* för S
- limitar os själva till bases där högra sidorna endast är singletons
- minimal basis
	- alla right sides singletons
	- om en FD removed inte längre en basis
	- om tar bort en attribute från någon attribute i någon FD är inte längre en basis 
- finns flera minimal bases

projection of FDs
- om har $R_1 = \pi_L(R)$ så är de FDs som håller i $R_1$ alla FDs som
	- Följer från S
	- endast involverar attributes i L

### Anomalies
- problem som redundancy, kommer exempelvis när man försöker cramma för mycket data i en relation
- Update anomalies; ändrar data på ett ställe men unchanged någon annanstanns
- deletion anomaly: om man raderar en bit data försvinner mer än intended

#### Decomposing relations
- splitta relation i flera nya scheman för ta bort anomalies
- goal är splitta relation till flera så att ingen exhibitar anomalies = boyce codd normal form
	- BCNF <=> varje nontrivial FD i R har en superkey i vänsterledet
	- varje two attribute relation är i BCNF
	- för att decomposa till BCNF:
		- Ta violating FD
		- dela upp i en relation som innehåller alla As och Bs
		- dela upp i en annan som innehåller resten av alla element som inte är B:n men inte A:n
		- lägg i varje steg till alla Bn som alla An Functionally determinar, blir mindre jobb

för en decomposition vill vi ha:
 1. elimination of anomalies
 2. recoverability of information
 3. preservation of dependencies: orginella fds retainas när man joinar

inte alltid möjlgit att ha alla tre

för att göra så att alla orginella FDs håller vid joins använder man *Third normal form* (s.103)
- 3NF
- Är om A1... -> B1 är en nontrivial FD är antingen
	- A1... en superkey
	- alla Bs som in är i A1... tillhör någon annan key
- attirbutes som tillhör keys kallas prime
- för att göra en sådan decomposition:
	- skriv om alla FDs till minimal basis
	- Skapa en schema för varje FD i varje minimal basis
	- ta bort de som är proper subsets av andra
	- om det inte finns någon schema vars attributer är en superkey lägger man till en sådan