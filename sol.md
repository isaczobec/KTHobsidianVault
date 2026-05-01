# Mästarprov i Paradigm 2026
Isac Zobec izobec@kth.se

**Källor**

https://en.wikipedia.org/wiki/Fixed-point_combinator för Y-Kombinatorn


http://www.zvon.org/other/haskell/Outputprelude/sum_f.html för typen av `sum`

https://wiki.haskell.org/Power_function för typen av `(^)`

# 1: Cellulära automater i Haskell och Python/Java

## (a) 

```haskell
safeIndex :: [[Int]] -> Int -> Int -> Int
safeIndex l i j = 
    if (i >= 0 && i < length l) && (j >= 0 && j < length (head l)) 
        then l !! i !! j
        else 0 

step :: [[Int]] -> [[Int]]
step l = res where
    i_max = length l
    j_max = length (head l)

    infected i j l =
        foldl max (safeIndex l i j) [
            safeIndex l (i-1) j,
            safeIndex l (i+1) j,
            safeIndex l i (j-1),
            safeIndex l i (j+1)
        ]

    res = [[infected i j l | j <- [0..j_max-1]] | i <- [0..i_max-1]]

test_arr :: [[Int]]
test_arr = [
    [0,0,0,0,0],
    [0,1,0,0,0],
    [0,0,0,0,0],
    [0,0,0,1,0],
    [0,0,0,0,0]
    ]


-- ger 
-- [
-- [
    -- [0,1,0,0,0],
    -- [1,1,1,0,0],
    -- [0,1,0,1,0],
    -- [0,0,1,1,1],
    -- [0,0,0,1,0]]
-- ]
```

## (b) 

```python
def step(l: list[list[int]]):

    def becomes_infected(i: int, j: int, l: list[list[int]]):
        if i < 0 or i >= len(l) or j < 0 or j >= len(l[0]):
            return 0
        
        return max(
            l[i][j],
            l[max(0, i-1)][j],
            l[min(len(l)-1, i+1)][j],
            l[i][max(0,j-1)],
            l[i][min(len(l[0])-1,j+1)],
        )

    i_max = len(l)
    j_max = len(l[0])

    result_rows = []
    
    for i in range(i_max):
        result_row = []
        for j in range(j_max):
            result_row.append(becomes_infected(i, j, l))
        result_rows.append(result_row)

    return result_rows


test_arr = [
    [0,0,0,0,0],
    [0,1,0,0,0],
    [0,0,0,0,0],
    [0,0,0,1,0],
    [0,0,0,0,0]
    ]

print(step(test_arr))

# [ resultat:
#     [0, 1, 0, 0, 0], 
#     [1, 1, 1, 0, 0], 
#     [0, 1, 0, 1, 0], 
#     [0, 0, 1, 1, 1], 
#     [0, 0, 0, 1, 0]
# ]
```

## (c)

Detta kan bli fel eftersom den givna imperativa lösningen använder värdena i arrayen för att avgöra vilka celler som ska bli infekterade i nästa tidssteg. Om vi itererar genom arrayen, och i en iteration skriver ett värde till en av cellerna kommer nästkommande iterationer att läsa detta värde och felaktigt tro att det härstammar från föregående tidssteg, och riskerar därför att felaktigt markera en cell som infekterad. Nedan ges ett exempel på hur detta skulle kunna leda till ett felaktigt resultat. Exempelet antar att vi itererar genom arrayn från vänster till höger, och sedan uppifrån och ned.
```
Ursprunglig array:
[0,0,1,0]
[0,0,0,0]

programmet skriver korrekt en 1a i (1,2).
[0,1,1,0]
[0,0,0,0]

programmet skriver korrekt en 1a i (1,4).
[0,1,1,1]
[0,0,0,0]

programmet skriver felaktigt en 1a i (2,2) eftersom den ser 1an som skrevs tidigare.
[0,1,1,1]
[0,1,0,0]

programmet skriver korrekt en 1a i (2,3).
[0,1,1,1]
[0,1,1,0]

programmet skriver felaktigt en 1a i (2,2) eftersom den ser 1an som skrevs i förra steget.
[0,1,1,1]
[0,1,1,1]
```

Om vi vill göra `step` in-place kan vi göra följande:
iterera över arrayens rader, och sedan dess kolumner genom indexering. Om något av värdena i de 4 intilligande cellerna är 1, och värdet i den nuvarande cellen är 0, skriv 2 till den nuvarande cellen.
Efter denna iteration är klar, iterera igen genom arrayn och ändra alla celler vars värde är 2 till 1. Pythonkod:
```python

def step_inplace(l: list[list[int]]):

    def becomes_infected(i: int, j: int, l: list[list[int]]):
        if i < 0 or i >= len(l) or j < 0 or j >= len(l[0]):
            return False
        
        return any(
            [l[i][j] == 1,
            l[max(0, i-1)][j] == 1,
            l[min(len(l)-1, i+1)][j] == 1,
            l[i][max(0,j-1)] == 1,
            l[i][min(len(l[0])-1,j+1)] == 1],
        )

    i_max = len(l)
    j_max = len(l[0])

    for i in range(i_max):
        for j in range(j_max):
            if becomes_infected(i, j, l) and l[i][j] == 0: l[i][j] = 2

    print(l)

    for i in range(i_max):
        for j in range(j_max):
            if l[i][j] == 2: l[i][j] = 1

test_arr = [
    [0,0,0,0,0],
    [0,1,0,0,0],
    [0,0,0,0,0],
    [0,0,0,1,0],
    [0,0,0,0,0]
    ]

step_inplace(test_arr)
print("res from inplace:")
print(test_arr)

#
# [
#     [0, 1, 0, 0, 0], 
#     [1, 1, 1, 0, 0], 
#     [0, 1, 0, 1, 0], 
#     [0, 0, 1, 1, 1], 
#     [0, 0, 0, 1, 0]
# ]
```

Haskellösningen undviker denna problematik genom att lösa problemet med en ren funktion, som tar som input koordinater av en cell, samt föregående tidsstegs array, och returnerar 1 om cellen vid de givna koordinaterna blir infekterad i detta tidssteg, och 0 annars. En ren funktion är en funktion vars returvärde alltid är detsamma för samma inputvärde, och som inte har några sideoeffekter på andra delar av programmet. Alla funktioner i Haskell är rena, så det är garanterat att alla evalueringar av `ìnfected` kommer ske oberoende av varandra; de kan omöjligen påverka andra evalueringar så att de blir ogiltiga. Detta faktum säkerställs även av oföränderlighet; att objekt aldrig kan muteras eller få ändrade värden. eftersom att arrayen `l` ges som input på samma sätt i alla evalueringar är det per oföränderlighet garanterat att varje evaluering av `infected` kommer se den originella, korrekt värdet på listan. 

# 2: Kvadratrot med Newton–Raphson och högre ordningens funktioner

## (a) Haskellkod

```haskell
applyN :: Int -> (a -> a) -> a -> a
applyN 0 f x = x
applyN n f x = applyN (n-1) f (f x)

sqrtStep :: Double -> Double -> Double
sqrtStep a x = 1.0/2.0 * (x + a/x)

sqrtNewton :: Int -> Double -> Double
sqrtNewton n a = applyN n (sqrtStep a) 1.0
```

Resultaten blir, för a = 2.0 och olika n:

| n=0 | n=1 | n=2                | n=3                | n=4                |
|-----|-----|--------------------|--------------------|--------------------|
| 1.0 | 1.5 | 1.4166666666666665 | 1.4142156862745097 | 1.4142135623746899 |

för n=4 är svaret detsamma som 1.41421356 för de 8 givna decimalerna.

## (b) Imperativ kod

```py
def run(a: float = 2.0, n: int = 4):

    x = 1.0
    for i in range(n):
        x = 1.0/2.0 * (x + a / x)

    return x

print(run())
```

för a=2.0 och n=4 ger pythonkoden svaret 1.4142135623746899, vilket är exakt samma som för haskell upp till alla givna decimaler (1.4142135623746899).

## (c) Diskussion

`applyN` är en högre ordningens funktion (en högre ordningens funktion är en funktion som kan ta funktioner som indata, eller returnerar funktioner). Denna funktion är en högre ordningens funktion eftersom den tar en funktion `f` och applicerar den `n` gånger till någon given indata. Argumentet `f` har typen `(a -> a)`, vilket innebär att `f` tar input av en typ och returnerar ett värde av samma typ, i detta fall en `Double` (detta är vad "`f` får göra").

En ren funktion är en funktion som för samma inputparametrar alltid ger exakt samma returvärde, och som inte har några sidoeffekter i programmet. `sqrtStep a` är en ren funktion eftersom att dess returvärde endast beror på värdet som stoppas in i funktionen; den beräknar alltid $f(x) = \frac{1}{2}(x + \frac{a}{x})$ vilket deterministiskt endast beror på $x$. Den har inte heller några sidoeffekter. `applyN` är en ren funktion eftersom att den givet samma `n`, `f` och `x` deterministiskt returnerar exakt samma resultat; värder som ges av att applicera `f` på `x` `n` gånger. Den har inte heller några sidoeffekter.

Den funktionella lösningen använder rekursion genom `applyN` för att applicera `f` många gånger, medan den imperativa python-lösningen iterativt applicerar `f` många gånger till `x`. Loopkroppen kan inte sägas vara ren funktion, eftersom den har den väldigt tydliga sidoeffekten att `x` ändras i varje iteration (och x är definierad utanför loopen).

# 3 En Turingmaskin

# (a)

tillstånd $q_e$ och att läsa inputsymbol 1 ger enligt transitionstabellen att $\delta(q_e, 1) = (q_o, 1, R)$. Alltså byts tillstånd till $q_o$, en 1:a skrivs (ingen förändring), och maskinen går höger. Bandet ser nu ut så här:

```
| > | 1 | 0 | 1 | # | # | # |
          ^
 Läshuvud i tillstånd qo
```

# (b)

Vi fortsätter körningen från (a).

```
| > | 1 | 0 | 1 | # | # | # |
          ^
 Läshuvud i tillstånd qo

delta(qo, 0) = qo, 0, R

| > | 1 | 0 | 1 | # | # | # |
              ^
 Läshuvud i tillstånd qo

delta(qo, 1) = qe, 1, R

| > | 1 | 0 | 1 | # | # | # |
                  ^
 Läshuvud i tillstånd qe

delta(qe, #) = qE, #, R

| > | 1 | 0 | 1 | # | # | # |
                      ^
 Läshuvud i tillstånd qE

delta(qE, #) = qh, 0, S

| > | 1 | 0 | 1 | # | 0 | # |
                      ^
 Läshuvud i tillstånd qh

delta inte definierad för någon symbol då tillståndet är qh; maskinen haltar nu.
```

Maskinen beräknar om antallet ettor på bandet innan en blanksymbol hittas är udda eller jämnt (och skriver en 1:a om det var udda, och en 0:a annars). Detta kan vi se eftersom om antalet ettor hittils sedda är jämnt så att tillståndet är $q_e$, och vi sedan ser en etta, slår tillståndet över till $q_o$ för signalera att vi numera har sett ett udda antal ettor, och går till höger. På samma sätt slår tillståndet över från $q_o$ till $q_e$ om vi ser en etta och befinner oss i $q_o$. I tillstånden $q_o$ och $q_e$ så bevarar vi alltid nuvarande tillstånd när vi ser en 0:a, vilket visar att dessa inte är vas som 'ränkas' i beräkningen. I första steget i uppgiften har vi sett 0 ettor (ett jämnt antal), och maskinen börjar i tillstånd $q_e$ vilket är konsekvent eftersom 0 är jämnt.

Resultatet kommer hamna ett steg till höger om det första blanksteget som ses efter den kontinuerliga sekvensen av 1:or och 0:or maskinen har läst. Detta ser vi eftersom att när maskinen går till höger efter att ha läst den sista siffran, kommer den läsa ett blanksteg #, gå och sedan byta tillstånd till $q_E$ eller $q_O$ beroende på om den innan befann sig i $q_e$ eller $q_o$, och också gå ett steg till höger. Nu befinner sig pekaren allstå två steg till höger om sista siffran. Här kommer den nu skriva resultatet, en 1:a om tillståndet är $q_O$ (och vi sett ett udda antal 1:or) och en 0:a om tillståndet är $q_E$ (om vi sett ett jämnt antal 1:or).

$q_E$ och $q_O$ behövs eftersom dessa tillstånd är ansvariga för att skriva resultatet. En turingmaskin, som den är definierad, haltar om övergångsfunktionen inte är definierad för ett givet tillstånd och läst indata. Om detta är fallet skriver den inte någon symbol. Vi måste alltså ha två tillstånd som är designerade för att skriva resultatet och sedan övergår till ett tillstånd som haltar direkt ($q_h$).

# (c)

En turingmaskin är en teoretisk konstruktion för beräkningar, medan Von Neumann-arkitekturen beskriver en fysisk arkitektur för datorer. Detta medför skillnader i var instruktioner lagras och hur de utförs.

- För en turingmaskin kan instruktionerna eller själva programmet sägas helt lagras i övergångsfunktionen: Det är entydigt den som bestämmer hur turingmaskinen ska reagera på den lästa symbolen och nuvarande tillstånd: Vilket tillstånd maskinen ska gå in i, vad den ska skriva och vilket håll läshuvudet ska gå åt. Av samma anledning kan även denna sägas styra kontrollflödet (vilken instruktion som körs härnäst), eftersom den styr vilket nästkommande tillstånd kommer vara, vad som kommer skrivas till bandet och åt vilket håll läshuvudet kommer flyttas. Däremot så påverkar även vad som finns på bandet hur maskinen kommer bete sig, så även de skulle kunna kopplas till kontrollflödet. Angående vad som kör själva instruktionerna (interpretering); då en Turingmaskin är en teoretisk matematisk modell blir detta något av en tolkningsfråga, men man skulle kunna säga att det är övergångsfunktionen $\delta$ som är ansvarig för att köra övergångarna i transistionstabellen, eftersom denna funktion evaluears med nuvarande tillstånd och läst symbol för att bestämma vad som ska hända härnäst.
- En Von Neumann-maskin har en mer fysisk tolkning av var själva programmet lagras: Det lagras som binära maskinkodsintruktioner i minnesenheten (Memory Unit), ofta sekventiellt över flera adresser. Dessa binära instruktioner representerar olika instruktioner som får sidoeffekter som CPU:n har ansvar att utföra. Kontrollflödet, d.v.s. vad som styr vad nästa steg/instruktion kommer vara, är programräknaren (program counter). Den håller koll på ett tal som refererar till en minnesaddress där nästa instruktion att köra befinner sig; när nuvarande instruktion har körts klart hämtas nästa instruktion från minnet, och programräknaren inkrementeras. Vidare kan det även sägas att vissa speciella instruktioner (branch-relaterade) kan sägas påverka kontrollflödet eftersom de kan påverka adressen lagras i programräknaren, och därmed ordningen i vilken instruktioner utförs. Angående vad som utför instruktionerna (interpretering) är det Kontrollenheten och ALU:n innuti CPUn som är ansvariga för att köra den hämtade instruktionen: se till att den (eventuellt) på något vis ändrar tillståndet i maskinen.

Man kan argumentera föra att Turingmaskinen har skarp syntaktisk skillnad mellan program och data, medan Von Neumann-maskinen suddar ut den. Detta eftersom att programet i en Turinmaskin kan sägas kodas in i övergångsfunktionen $\delta : Q \times \Sigma \mapsto Q \times \Sigma \times \{L, R, S\}$ (eventuellt genom en transitionstabell), som är (syntaktiskt) separat från datat i programmet, som istället largras som symboler i $\Sigma$ på ett sekventiell, oändligt långt band. Å andra sidan lagras data och instruktioner i en Von Neumann-maskin på exakt samma sätt: som en sekvens av bitar i samma minne.

Det kan vara värt att nämna att i motsättning till det som sagts här skulle man kunna konstruera en turingmaskin som kan tolka data på bandet som ett program/instruktioner, och att programmet därmed även skulle kunna sägas därmed befinna sig delvis på bandet. Exakt var instruktionerna lagras i en Turingmaskin blir alltså något av en tolkningsfråga. Däremot kräver denna konstruktion att övergångarna i transitionstabellen stödjer att läsa data som instruktioner.

# (d) 

Här antar vi att det med `null` menas samma definition som i haskell - ett predikat som är sant om en given lista är tom och falskt annars. Vi definierar en hjälpfunktion

$$
Odd = \lambda f . \ \lambda xs . 
\left\{
\begin{array}{cc}
0 & \text{om } null \ xs \\
(head \ xs + f \ (tail \ xs) ) \% 2 & \text{ annars}
\end{array}
\right.
$$

(där % är modulooperatorn). Lambda calculus stödjer inte att referera till funktioner via namn (dock använder vi namn här, som vilka då de används innebär att definitionen för den namngivna funktionen ska substitueras in i sagda formel), så vi kan inte upppnå rekursion genom att inkludera en funktion i sin egen definition. Vi använder därför Y-kombinatorn (från [https://en.wikipedia.org/wiki/Fixed-point_combinator](https://en.wikipedia.org/wiki/Fixed-point_combinator)) för att uppnå reukrsion. Denna är definierad som

$$
Y = \lambda f . \  (\lambda x . f \ (x \ x)) \ (\lambda x . f \ (x \ x))
$$

Om vi applicerar någon funktion $g$ på $Y$ får vi

$$
(Y \ g) = ((\lambda f . \  (\lambda x . f \ (x \ x)) \ (\lambda x . f \ (x \ x))) \ g)
$$
$$
= ((\lambda x . g \ (x \ x)) \ (\lambda x . g \ (x \ x)))
$$
$$
= (g \ ((\lambda x . g \ (x \ x)) \ (\lambda x . g \ (x \ x))))
$$
$$
= (g \ (Y \ g))
$$
alltså, Y-kombinatorn applicerad till någon funktion funktion ger funktionen applicerad till fukntionen applicerad till Y-kombinatorn. Detta möjliggör rekursion som kan pågå godtyckligt länge. Med detta får vi att en funktion som returnerar 1 om $xs$ innehåller ett udda antal 1:or och 0 annars (svaret på uppgiften) är
$$
\lambda xs . \ ((Y \ Odd) \ xs)
$$
För att se att detta stämmer kan vi expandera uttrycket $(Y \ Odd)$:
$$
((Y \ Odd) \ xs) = ((Odd \ (Y \ Odd)) \ xs)
$$
Nu, om $xs$ är tom evaluearas $((Odd \ (Y \ Odd)) \ xs)$ till 0. Om inte expanderar uttrycket på följande vis:
$$
((Odd \ (Y \ Odd)) \ xs) \\=
((head \ xs) + ((Y \ Odd) \ (tail \ xs)) ) \% 2
$$
Om vi nu expanderar $(Y Odd)$ en gång till får vi samma evaluering, men istället för $tail \ xs$. Det är på detta sätt rekursionen sker. Vi ser även att då $tail \ xs$ är strikt kortare än $xs$ kommer rekursionen gå mot basfallet, och måste därför terminera. Vidare sker kombinationen av resultatet för huvudet och svansen genom additionen modulo 2 här. Att resultatet blir korrekt kan rättfärdigas genom följande: Anta att $xs$ har $n$ element. Vi antar nu att den rekursiva delen av formeln, som körs med $tail \ xs$ som har $n-1$ element, returnerar 1 om den har ett udda antal 1:or och noll annars. om $head \ xs$ är 1 och $tail \ xs$ har ett jämnt antal 1or blir beräkningen (1 + 0) % 2 = 1, vilket är korrekt eftersom $xs$ i detta fall kommer ha ett udda antal element. På samma vis visar man att de andra fallen är korrekta. Alltså ser vi att formeln är korrekt för listor av storlek $n$ under antagendet att den är korrekt för listor av storlek $n-1$. För att visa basfallet $n=0$ ser vi från innan att formeln då evalueras till 0, vilket är korrekt eftersom den tomma listan har ett jämnt antal 1:or. Alltså ger funktionen korrekt returvärde för listor av alla storlekar.

# 4: Subrutiner, parametrar och metoder

## (a)

Ett exempel på hur stilen i Exempel A leder till problem är genom de namnkonflikter som globala variabler kan introducera. Om en subrutin anropar en annan subrutin som använder och skriver till globala variabler som den anropande funktionen också använder kan felaktigt beteende fås, speciellt om den anropande funktionen antar att dessa variabler är orörda. Om två subrutiner använder globala variabler med samma namn så finns det risk att de exempelvis skriver över varandras resultat eller returvärden; vi kan behöva skapa många separata returvariaber för att bevara alla returvärden, vilket snabbt blir svårt att hålla koll på. 

Rekursion som kräver att varje rekursivt anrop av en subrutin har något slags minne eller variabler som den ska kunna läsa när "djupare" rekursiva anrop har returnerat fungerar inte här. Eftersom en subrutin bara kan använda globala variabler, vilka det finns ett konstant antal av, kan inte antalet ihågkommna variabler öka obegränsat, vilket rekursion kräver. Direkt när ett nytt anrop skriver över de globala variablerna som används kan inte det föregående anropet längre läsa de originella värdena på dessa variabler.

Kursen beskriver ett programeringsparadigm som "en stil för att organisera kod och data", eller "en uppsättning språkegenskaper, dvs koncept, abstraktioner, principer och bakomliggande antaganden som formar hur vi programmerar". När den imperativa/strukturella programmeringen övergick till procedurell stil introducerades nya koncept som scope - en begränsad del av koden där exempelvis endast funktionen som deklarerar en uppsättning *lokala variabler* har tillgång till dem (detta fallet beskriver en funktions scope). Parametrar till funktioner introducerades även - att man kan skicka med ett värde som indata till en funktion, istället för att funktionen ska behöva läsa indata genom globala variabler.

Dessa nya koncept och egenskaper gjorde att sättet man strukturerede kod på ändrades: Nu kunde man till större grad dela upp kod i isolerade funktioner, där varje funktion "äger" alla variabler inom sitt lokala scope och inte behöver oroa sig för att de ska ändras från annat håll (som var fallet med globala variabler). Eftersom sättet kod strukturerades på ändrades kan övergången till procedurell stil sägas vara ett paradigmskifte enligt kursern.

## (b)

Ett *scope* i ett program är en avgränsad del av koden ifrån vilken en viss uppsättning av namngivna variabler är nåbara (går att läsa från/skriva till). Till exempel får vanligtvis varje funktion sitt eget scope: detta innebär att man endast ifrån innuti funktionen kan läsa och modifiera de lokala variablerna som definieras i den. Parametrarna en funktion körs med kopieras ofta (om de inte exmpelvis skickas "by reference" som i C++) till lokala versioner som ingår en funktions scope. Efter ett scope lämnas glöms variablerna som tillhöre det bort, det vill säga de kan inte refereras till längre (de kan inte refereras till utanför scopet). Under körtiden för ett program implementeras scope genom en *stackram*. Detta innebär när en funktion anroppas allokeras det på minnesstacken så mycket minne som behövs för att lagra alla funktionens lokala variabler (och en returadress till var exekveringen ska återgå efter funktionsanroppet returnerar) genom att flytta stackpekaren. När funktionen returnerar avallokeras det allokerade minnet genom att flytta tillbaka stackpekaren lika mycket. Returadressen läses också för att sedan återgå till den procedur/funktion som anropade sagda funktion.

Detta löser helt problemet med rekursion: Nu kan mängden allokerat minne (i teorin) öka obegränsat (så länge man inte får en stack overflow), så varje rekursivt anrop kommer ha egna lokala variabler sparade i minnet som bevaras över rekursiva anrop, och som (vanligen) endast kan modifieras innifrån deras scope.

Vidare, om vi med två samtida anropp menar att flera exekveringstrådar kan exekvera `multiply` fungerar detta nu eftersom att trådarna vanligtvis har varsin stack och därmed separata stackramar för variablerna (`k` inkluderat) `multiply` behöver ha tillgång till.

## (c)

I Java är det första implicita argumentet till en klass-metod `this`-pekaren; en referens till objektet på vilket metoden kallas, och genom vilken dess metoder och fält kan kommas åt. 

I (a) komms `k` åt genom en global variabel - när `multiply` kallas läses sannolikt värdet på den globala minnesadressen där k ligger för att få dess värde. I (c) komms `k` istället åt genom att följa `this`-pekaren för det anropande objektet och därefter läsa dess `k`-värde. En skillnad mot (a) är att i (a) kan `k` kommas åt från var som helst i koden, medan `k` för en viss instans av `Multiplier` i (c) endast kan kommas åt genom klass-metoder på sagda instans (encapsulation).

I (b) komms `k` åt som en parameter till en procedur. Om vi antar att `k` skickas med värde (inte med referens) till `multiply` innebär det en lokal kopia som endast existerar inom `multiply`:s scope har skapats. Detta är en skillnad ifrån (c): där har vi åtkomst till `k` genom referens (referens till det anropande objektet, `this`, genom vilken vi kommer åt des `k`-fält). Vi skulle alltså tekniskt sett kunna ändra `k` i multiply i (c), så att ändringen bevaras efter funktionen har returnerat, vilket vi inte kan i (b).

På grund av hur klassen `Multiplier` är skriven i (c) är `multiply` en ren funktion. Om vi explicit skriver ut förstaargumentet får `multiply` signaturen `multiply(Multiplier m, int x)`. Funktionen är ren eftersom två körningar av den där inputargumentet är samma (uppfyller likhet) alltid kommer returnera samma resultat. Anledningen bakom att detta är fallet är att `k` är markerad som `final` på `Multiplier` och därför inte kan ändras efter den har satts i constructorn. Alltså kommer anrop till `multiply` med samma instans av `Multiplier` och samma `x` värde alltid ge samma returvärde, eftersom `k` aldrig kan ändras mellan anropp. Vidare har funktionen inte heller några sidoeffekter, vilket är ett krav på rena funktioner.

Om vi däremot hade tagit bort nyckelordet `final` framför `k` och sedan introducerat något sätt `k` kunde ändras på hade inte `multiply` varit ren längre. Då skulle olika anrop till `multiply` med samma instans av `Multiplier` och samma `x` kunna utföras med olika värden på `k`, och därmed ge olika resultat.

# Uppgift 5: Tre paradigm, ett problem

## (a)

**Exempel A** kan sägas tillhöra den imperativa familjen, eftersom den utgörs av en sekvens av instruktioner med kontrollflöde, och beskriver exakt hur beräkningen ska gå till, samt att variabler som skapas förändras (bieffekter). Vidare kan exemplet sägas tillhöra den objektorienterade paradigmen på grund av språkegenskaperna stöd för polymorfi (och eventuellt enkapsulering) som exemplet uppvisar. Här menas med polymorfi möjligheten för en variabel, i detta fall `numbers`, att ha olika typer, samt att dynamiskt under körtiden binda till en metod på `numbers`-objektet. Vi ser i Exmpel A att vi kan köra `sum_of_squares` på alla objekt som har en `__iter__()`-metod definierad som returnerar en serie tal, utan att få runtime-errors eller felaktigt beteende. I `sum_of_squares` behöver vi inte heller veta något om hur `numbers`-objektet fungerar, utan vi bryr oss bara om interfacet det uppvisar - detta är ett exempel på enkapsulation. Följande kodstycke visar hur polymorfi och möjlighet att kalla på `sum_of_squares` med olika inputtyper, som bevisligen binder till olika funktioner under körtid:

```python
class TransactionHistory():
    def __init__(self, transactions):
        self.transactions = transactions

    def __iter__(self):
        for transction in self.transactions:
            yield transction

def sum_of_squares(numbers):
    total = 0
    for x in numbers:
        total = total + x * x
    return total

print(
    sum_of_squares(
        TransactionHistory([1, -2, 5])
        )
    )

print(
    sum_of_squares(
        [1, -2, 5]
        )
    )
```

```
╰─❯ python3 p.py
30
30
```

Angående vilken aspekt av imperativa språken som framkommer tydligast: Man skulle kunna argumentera att flödeskontroll är det mest synliga konceptet eftersom att kodstycket med sin for-loop bestämmer vilken instruktion som ska köras härnäst (om `total = total + x*x` ska köras igen baserat på om numbers har fler element kvar), och att denna for-loop är det som utför beräkningen i fråga. Dock kan man förmodligen även argumentera för att något av de andra kännetecknen framkommer tydligare (man skulle exempelvis kunna resonera att sekvens är mest framträdande eftersom summan av kvadrater beräknas genom en sekvens av instruktioner).

**Exempel B** kan sägas tillhöra den imperativa familjen, eftersom det återigen utgörs av en sekvens av instruktioner med kontrollflöde, som beskriver exakt hur beräkningen ska gå till. Bieffekter på deklarerade variabler finns även. Vidare kan det sägas tillhöra den procedurella paradigmen. Detta eftersom att exempelet innehåller en procedur där input-parametern `numbers` binder till ett värde, ett lokalt funktions-scope skapas, och ett returvärde ges. Dessa är språkegenskaper som introducerades iochmed den procedurella programmeringen, därav klassificieringen. Vidare är detta exemplet inte objektorienterat (iallfall till samma grad som A) eftersom att det inte stödjer polymorfi på samma sätt - värdet som binds till `numbers` kommer altid vara av typ `int[]` (en klass kan inte ärva från `int[]` i java) och vidare vet vi även exakt hur `int[]`-värdet som binds till `numbers` ser ut/fungerar; ingen enkapsulering sker. Vidare blir exemplet inte objektorienterat bara för att `sumOfSquares` är definierad i en klass - metoden är definierad med nyckelordet `static` vilket innebär att inte har en implicit `this`-pekare till en instans av `MathUtils`, utan istället beter sig precis som en vanlig procedur/funktion.

Eftersom kodstrukturen i exempel B är i princip exakt samma som i A (med avseende på hur summan av kvadraterna beräknas) med en for-loop skulle man även här kunna säga att kontrollflöde är det mest framträdande imperativa kännetecknet. Som sagt finns det sannolikt dock andra resonemang som kan göras även här.

**Exempel C** kan sägas tillhöra den deklarativa familjen eftersom kodstycket beskriver vad som beräknas, och utelämnar hur eller i vilken ordning det ska göras; kontrollflödet abstraheras bort. `sumOfSquares` har inte heller några bieffekter. Vidare kan exemplet sägas tillhöras den funktionella paradigmen eftersom funktionen är ren (inga sidoeffekter, och ger alltid samma returvärde givet samma indata) och uppvisar även  referenstransperens. Inget tillstånd sparas heller i exemplet vilket ytterligare talar för att det tillhör paradigmen.

## (b)

funktionskomposition är en funktion av typen `(a->b) -> (b->c) -> (a->c)`, och om den kallas med exempelvis `h = f . g` blir `h` funktionen som ges av att först applicera `g`, därefter `f`, så att `h x = f (g x)`. Uttrycket som ges när vi applicerar `(.)` till de två funktionerna i exempel C, det vill säga `sum . map (^2)` är referenstransperant, alltså att vi kan substituera applikationen av `(.)` med värdet  den ger utan att hela uttryckets värde ändras (och utan att programmet påverkas). Om vi gör detta får vi (lite beroende på hur `(.)` är implementerad) `(\x -> sum (map (^2) x))`, vilket har exakt samma värde som det tidigare uttrycket: en funktion som tar en lista med heltal och returnerar summan av kvadraterna av dessa heltal. `(.)` är även en ren funktion. Funktionen den returnerar kommer endast bero på de två givna inputfunktionerna, det är alltid funktionen som ges av att applicera den andra följt av den första funktionen. `(.)` har inte heller några sidoeffekter. Vidare garanterar dessa egenskaper hos rena funktioner referenstransperens: Eftersom de determinstiskt endast beror på argumenten de kallas med, och aldrig har några sidoeffekter kan de alltid substitueras med sina returvärden så att uttryck de är inkluderade i har oförändrade värden. 

`(map (^2))` har typen `[Int] -> [Int]` (eller egentligen `Numeric a => [a] -> [a]`, för att vara exakt) Som givet en lista av tal returnerar en lista med kvadraterna av dessa tal. Denna funktion är ren; den har inga sidoeffekter och returnerar alltid listan av kvadraterna för de givna talen. Vidare är både själva uttrycket `(map (^2))` samt uttrycket vi får om vi applicerar funktionen till en lista `xs` (`(map (^2) xs)`) referenstransparenta, vilket försäkrar oss om att vi i den givna kontexten alltid kommer få rätt returvärde (vi kan alltid ersätta `map (^2) xs` med en lista med `xs` kvadrerade värden). Om vi exempelvis evaluerar hela `sumOfSquares` med `xs = [x0,x1,...xn]` får vi sammantaget (eftersom att alla uttryck är referenstransperanta) att `sumOfSquares xs` kan ersättas med `(\x -> sum (map (^2) x)) [x0,x1,...xn]`, som kan ersättas med `sum (map (^2) [x0,x1,...xn])` som nu tack vare `map (^2)`:s eller `map (^2) xs` referenstransparens kan substitueras med att `sum [x1^2, x2^2,...xn^2]`, vilket uppenbarligen ger ett korrekt resultat. Här har vi alltså kunnat använda referenstransparens för att visa funktionens korrekthet.

typen `[Int] -> Int` avser en funktion som tar en lista med heltal och returnerar ett heltal, vilket innebär att detta är vad sumOfSquares måste göra. Däremot är typen för `sum` `Num a => [a] -> a` (http://www.zvon.org/other/haskell/Outputprelude/sum_f.html), vilket innebär att den kan köras på listor med alla numeriska typer av värden (inte endast heltal). `(^)` har typen `(Num a, Integral b) => a -> b -> a` (https://wiki.haskell.org/Power_function) vilket innebär att den kan användas för att upphöja ett värde av numerisk typ (inte endast heltal) till ett heltal. `map (^2)` får därmed typen `Num a => [a] -> [a]`, och därmed får `sum . map (^2)` (i teorin) typen `Num a => [a] -> a` (att definiera `qSum :: Num a => [a] -> a, qSum = sum . map (^2)` i ghci fungerar, och kan köras med både heltal och flyttal). Genom att tilldela typen `[Int] -> Int` till `sumOfSquares` tvingar vi därmed den att endast acceptera heltal och utesluter möjligheten att köra den på exempelvis `Double` (flyttal).