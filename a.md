
# Mästarprov i Funktionell programmering 2026
Isac Zobec izobec@kth.se CDATE
  
## 1. Rymdsonden Voyager - Immutability
  
### 1.1 Kod
```haskell
  
-- Datatyp för sonden och status
data Status = Idle | Moving | Sampling
    deriving (Show)
  
data Probe = Probe {
    x :: Int,
    y :: Int,
    battery :: Int,
    status :: Status
} deriving (Show)
  
-- De möjliga kommandona för sonden
data Command = Move Int Int  
             | Sample
             | Recharge
  
-- Implementationer av de olika kommandona
updateProbe :: Probe -> Command -> Probe
  
-- Kolla att bateriet är >= 10 så att värdet
-- efter Move inte understiger 0
updateProbe sond (Move dx dy)  
    | battery sond >= 10 =
        sond {
            x = x sond + dx,
            y = y sond + dy,
            status = Moving,
            battery = battery sond - 10
        }
    | otherwise =
        sond
  
-- Kolla att bateriet är >= 5 så att värdet
-- efter Sample inte understiger 0
updateProbe sond Sample
    | battery sond >= 5 =
        sond {
            status = Sampling,
            battery = battery sond - 5
        }
    | otherwise =
        sond
  
updateProbe sond Recharge
    = sond { status = Idle, battery = 100 }
```
  
### 1.2 Svar
  
#### *Beskriv skriftligt och muntligt hur konceptet immutability (oföränderlighet) tillämpas i din lösning. Varför "uppdaterar"vi inte bara variablerna i sonden?*
  
Alla funktioner i Haskell ska vara "rena". Detta innebär att deras värde inte ska bero på någon state i programmet, och de ska inte heller producera några side effects som påverkar andra funktioner; samma inputvärde ska alltid ge samma outputvärde. Att låta en variabel (sond) ändras som ett resultat av ett funktionsanropp går emot denna princip, det är en side effect. Istället definierar vi en funktion som beskriver hur en sond påverkas av de olika kommandona, och returnerar en ny sond; en ren funktion som mappar en sond och ett kommando till en ny sond. Detta strider inte mot avsaknaden av state eller immutability.
  
## 2. Aktieanalys med Högre Ordningens Funktioner
  
### 2.1 Kod
  
```haskell
average :: [Double] -> Double
average x = foldl (+) 0 x / fromIntegral (length x) -- from integral gör om till double
  
-- Funktion som tar bort outliers. Denna tar bort alla förekomster
-- av det högsta/lägsta talet - antar att uppgiftsbeskrivning tolkas
-- så istället för att man bara ska ta bort ett av de högsta/lägsta
-- värdena.
removeOutliers :: [Double] -> [Double]
removeOutliers x = res where
    maxItem :: [Double] -> Double = foldl max 0
    minItem :: [Double] -> Double = foldl min 99999999999 -- godtyckligt värde som med all sannolikhet är större än alla värden i listan
    res = (filter (maxItem x /=) . filter (minItem x /=)) x
analyzeStocks :: [(String, [Double])] -> [(String, Double)]
analyzeStocks =
    fmap (\(name, prices) -> (name, average $ removeOutliers prices)) . -- ta bort outliers, sen ta average
    filter (\(name, prices) -> length prices > 5) -- filtrera först bort de med 5 eller färre loggar
```
  
### 2.2 Svar
  
#### *Beskriv skriftligt och muntligt vilka högre ordningens funktioner du valt och varför.*
  
För att beräkna snittet samt minsta/största värdet av en lista har `foldl` använts. Denna funktion har typsignatur `(a -> b -> a) -> a -> [b] -> a`. Det är en högre ordnings funktion eftersom den kan returnera en funktion med signatur `[b] -> a`, vilket görs i exempelvis `maxItem`. Som inputs tar `foldl` alltså en funktion, ett startvärde, och en lista. Den applicerar sedan funktionen till startvärdet och första elementet i listan, "tar bort" första elementet, och upprepar detta. Alltså "ackumuleras" ett värde över hela listan. Att använda funktionen `(+)` och startvärdet `0` med `foldl` ger summan över en lista, som sedan delas med antalet element för att få snittet. `max` med `foldl` kommer hitta det största värdet i listan, eftersom det i varje "iteration" väljer ackumulatorvärdet endast om det är större än nästa element i listan. Vi börjar med startvärdet `0`, som vi kan anta är mindre än alla aktiekurser. På samma sätt få vi det minsta talet med `min`.
  
`filter` används för att filtrera listor, både för att ta bort kurserna med 5 eller färre värden, samt för att ta bort outliers. Den har typsignaturen `(a -> bool) -> [a] -> [a]`, och kan alltså returnera en funktion från en lista till en filtrerad lista. Som input tar den en funktion med signatur `(a -> bool)` som bestämmer vilka värden som ska behållas i listan, samt en lista att filtrera, och returnerar en filtrerad lista. För att filtrera bort för korta aktiekurser används funktionen `\(name, prices) -> length prices > 5`, och för att filtrera bort outliers används `filter (maxItem x /=)`, vilken ger `True` för värdena som inte är störst i listan `x`. För att ta bort de minsta värdena används `minItem` på samma sätt.
  
Slutligen används `fmap` för att mappa varje element i listan till en tuple med namnet och snittet av kursen. `fmap` har signaturen `Functor a => (b -> c) -> a b -> a c`, och kan alltså returnera en funktion från en funktor som wrappar typen `a` till typen `b`. I lösningen används den som `fmap (\(name, prices) -> (name, average $ removeOutliers prices))`, det vill säga att den mappar varje par av företagsnamn och aktiekurs i en lista (som är en funktor) till ett par av företagsnamn och genomsnitt av aktiekursen med outliers borttagna.
  
## 3. Tribonacci-tal och Lat Evaluering
  
### 3.1 Kod
```haskell
tribonacci :: [Integer]
tribonacci = zipWith3 (\x y z -> x + y + z)
    ([0] ++ tribonacci)
    ([0,0] ++ tribonacci)
    ([0,0,1] ++ tribonacci);
  
-- hitta första talet strikt större än någon gräns
-- förutsätter icke-minskande lista
firstOver :: Integer -> [Integer] -> Integer
firstOver t (x:xs)
    | t < x = x
    | otherwise = firstOver t xs
  
firstTribonacciOver :: Integer -> Integer
firstTribonacciOver x = firstOver x tribonacci
```
  
### 3.2 Svar
  
#### *Beskriv skriftligt och muntligt hur lat evaluering fungerar i Haskell och hur det möjliggör arbete med oändliga datastrukturer.*
  
Lat evaluering innebär att uttryck evalueras först när deras slutvärde behövs, snarare än exempelvis direkt när de ges som inputargument till funktioner. Om vi exempelvis vill evaluera uttrycket `f (h x)`, men `f` är definierad som exempelvis `f x = 10` så är resultatet oberoende av `h x` och denna funktion behöver inte evalueras. De "reducibla uttryck" (dvs uttryck som kan "förenklas", alltså skrivas om till en form som är närmare att vara helt evalueard) som finns ytterst i ett uttryck evaluearas alltså (oftast) först. Om det finns flera yttersta uttryck evalueras det längst till vänster först.
  
Kort sakt möjliggör detta arbete med oändliga datastrukturer eftersom lat evaluering kan innebära att endast "en del" av datan i datastrukturen behövs för att evaluera uttrycket. Om vi hade evaluerat de innersta reducibla uttrycken först hade man oundvikligen behövt evaluera en oändlig datastruktur om en sådan finns med i uttrycket, men genom att börja ytterst kan man undvika detta.
  
Nedan följer ett (något slarvigt) exempel på detta:
```haskell
infOnes = 1 : infOnes
  
take 0 _ = []
take _ [] = []
take n (x:xs) = x : take (n-1) xs
```
Att evaluera de yttersta uttrycken först gör att vi aldrig måste evaluera `infOnes`:
```
take 3 infOnes
1 : take 2 infOnes
1 : (1 : take 1 infOnes)
1 : (1 : (1 : take 0 infOnes))
1 : (1 : (1 : []))
[1,1,1]
```
  
#### *Förklara specifikt hur din tribonacci-lista evalueras när du kör take 10.*
  
Vi förutsätter samma implementation av `take` som innan, och tillåter att indexera en lista med `[i]`, `[i:j]` eller `[i:]` (för ökad läsbarhet). Dessutom skippas ett antal steg i evalueringen för att detta stycke inte ska bli för långt.
  
```haskell
t = tribonacci
  
take 10 t
  
t[0] : take 9 t[1:]
  
-- eftersom vi bara är interesserade av det första
-- elementet här, och vi redan har ett element i
-- varje av de tre listorna behöver vi inte
-- 'rekursera' tribonacci-listan mer för att få fler
-- element i sekvensensen. Listorna Zippas bara ihop
-- för första elementet och ger 0+0+0=0
(zipWith3 (\x y z -> x + y + z)
    ([0] ++ tribonacci)
    ([0,0] ++ tribonacci)
    ([0,0,1] ++ tribonacci))[0]
: take 9 t[1:]
  
-- Alltså förenklas t[0] till 0
0 : take 9 t[1:]
  
-- nu är vi interesserade av det andra elementet i
-- sekvensen, och eftersom den första listan bara
-- har ett element kommer `zipWith3` ge en lista
-- som också har endast har ett element. Därför
-- måste vi "rekursera" en gång med det första
-- elementet i tribbonacci-listan, 0.
0 : ((zipWith3 (\x y z -> x + y + z)
    ([0] ++ tribonacci)
    ([0,0] ++ tribonacci)
    ([0,0,1] ++ tribonacci))[1]
    : take 8 t[2:])
  
-- Här har vi lagt på [0] i slutet av alla tre
-- listor. Nu har alla 2 element och `zipWith3`
-- kommer ge [0,0], vars andra element är 0.
0 : ((zipWith3 (\x y z -> x + y + z)
    ([0,0] ++ tribonacci)
    ([0,0,0] ++ tribonacci)
    ([0,0,1,0] ++ tribonacci))[1]
    : take 8 t[2:])
  
-- Det andra elementet blev som sagt 0.
0 : (0 : take 8 t[2:])
  
-- Återigen, rekursera till vi har lagom många
-- element för att få det begärda elementet i
-- listan
0 : (0 : ((zipWith3 (\x y z -> x + y + z)
         ([0] ++ tribonacci)
         ([0,0] ++ tribonacci)
         ([0,0,1] ++ tribonacci))[2]
         : take 7 t[3:]))
  
-- efter två rekursioner får vi att listan blir
-- [0,0,1], tredje elementet är 1
0 : (0 : ((zipWith3 (\x y z -> x + y + z)
         ([0,0,0] ++ tribonacci)
         ([0,0,0,0] ++ tribonacci)
         ([0,0,1,0,0] ++ tribonacci))[2]
         : take 7 t[3:]))
  
0 : (0 : (1 : take 7 t[3:]))
  
-- Osv...
...
  
-- Tills alla element blivit evaluerade
0 : (0 : (1 : (1 : (2 : (4 : (7 : (13 : (24 : 44))))))))
  
[0,0,1,1,2,4,7,13,24,44]
  
```
  
Förhoppningsvis cachar eller sparar GHC de värdena i serien man hittils beräknas, så att de inte behöver beräknas från grunden varje gång ett element i serien behövs.
  
Följande visar hur ett godtyckligt antal element i serien beräknas rekursivt av `tribonacci`:
``` haskell
--   :[t]
--    -----------------
--    [0,t]
--    [0,0,t]
--    [0,0,1,t]
-- += [0,t]
--
--   :[0,t]
--    -----------------
--    [0,0,t]
--    [0,0,0,t]
--    [0,0,1,0,t]
-- += [0,0,t]
--
--   :[0,0,t]
--    -----------------
--    [0,0,0,t]
--    [0,0,0,0,t]
--    [0,0,1,0,0,t]
-- += [0,0,1,t]
--
--   :[0,0,1,t]
--    -----------------
--    [0,0,0,1,t]
--    [0,0,0,0,1,t]
--    [0,0,1,0,0,1,t]
-- += [0,0,1,1,t]
--
--   :[0,0,1,1,t]
--    -----------------
--    [0,0,0,1,1,t]
--    [0,0,0,0,1,1,t]
--    [0,0,1,0,0,1,1,t]
-- += [0,0,1,1,2,t]
--
--   :[0,0,1,1,2,t]
--    -----------------
--    [0,0,0,1,1,2,t]
--    [0,0,0,0,1,1,2,t]
--    [0,0,1,0,0,1,1,2,t]
-- += [0,0,1,1,2,4,t]
--
--    ...
```
  
## 4. Egendefinierade datatyper och svansrekursiv logg-analys
  
## 4.1 Kod
```haskell
data LogEntry =
    Info String |
    Warning String Integer |
    Error String Integer
  
totalRisk :: [LogEntry] -> Integer
totalRisk [] = 0
totalRisk (Info _ : ls)            = totalRisk ls
totalRisk (Warning _ errCode : ls) = errCode + totalRisk ls
totalRisk (Error _ errCode : ls)   = 10 * errCode + totalRisk ls
```
  
## 4.2 Svar
  
#### *Förklara kortfattat varför vi använder en Algebraisk Datatyp (ADT) här istället för att bara använda strängar eller tupler för att representera datat. Vad vinner vi gällande typsäkerhet och mönstermatchning?*
  
En stor fördel är att att vår loggfunktion endast kommer acceptera
loggar i rätt format - om vi försöker stoppa in något som inte är
av typ `LogEntry` kommer en compiler/runtime error kastas. Detta gör det lätt att upptäcka om vi gör något fel.
  
Att vi har de olika value constructorsen `Info`, `Warning` och `Error` gör också att det är lätt att matcha mönster i `totalRisk`-funktionen för att hantera de olika typerna av loggar på rätt sätt. Hade vi istället använt en sträng för att ange vilken allvarlighet felet hade hade vi behövt ha manuell hantering av dessa olika fall, och levt med risken att användaren kan inputtera ett ogilitgt värde, vilket vi hade behövt hantera manuellt. De algebraiska typerna gör det omöjligt (utan att få en compiler/runtime error) att göra denna typ av fel.