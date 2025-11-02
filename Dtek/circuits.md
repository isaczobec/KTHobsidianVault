en/fler diskreta input/outputs
specefication av funktion och timing=delay mellan inputs och outps

elements = egna black box circuits
nodes = sladdar mellan elements, exempelvis inputs och outputs till en element

combinatorial circuit memeoryless, output beror bara på nuvarande input
- sequential circuit beror på sequence av inputs och tidigare inputs

### Combinatorial
- timing specification handlar bara om upper/lower bound av reaktion på outputs
- CL notation i black box betyder endast combinatorial logic användes
- streck genom wire med nummer = bus, flera input signals bundeled

använder boolean algebra

### Illegal values
$X$ om nod drivs mot ex hög och låg samtidigt = contention

$Z$ om drivs till varken hög eller låg voltage, ok om värdet inte är relevant för operating
- ex missing input voltage är inte iekvivalent med input med värde 0

tristate buffer: Har input A och E (enable). När enable är på är det simple buffer, annars allowed to float

## Combinatorial building blocks

- **Multiplexor**
	- Control signal $S$ som bestämmer vilken av input signals som skickas cidare
	- Kan cutta size av multiplexor in half ?? s. 83
- **Decoder**
	- $N$ inputs, $2^N$ outputs. skickar ut en 1:a i exakt det nummer sladden som skickades in


## Timing
mäter delay som max tid från 50% point av rising edge av input till 50% point av rising edge av output
har *propagation delay* $t_{pd}$ (max time from input change till output change reaches final value) och *contamination delay* $t_{cd}$ (minimum time från change input till att output börjar ändras (kan vara instabil))

critical path är den pathen genom en circuit som har längst tid mellan att inputs ändras och att output reagerar. *critical* eftersom limitar speed at which circuit operates.
- short path är ist kortaste path
- $t_{pd}$ är summa av $t_{pd}$ för varje element i critical path, $t_{cd}$ är summa av contamination delay för varje elemnt i short path

glitch är när flera ändringar i output sker, endast problem om vi dependar an output innan $t_pd$ har passerat
något om hur motverkar glitches med extra components s.92

# Sequential logic
simplest bilding block = bistable element, bara två stable states

SR-Latch har set och reset men agerar konstigt då båda set till 1

D-Latch har en SR latch och en CLK bit som avgör om man ska uppdatera SRlatchen. Uppdaterar iså fall kontinuerligt

D-Flip-Flop: Två D latches kopplade med motsatta clock-signaler. Ändrar bara värde då CLK risar från 0 till 1, emmitar annars gamalt värde.

En register är N st flip flops med samma CLK input. Base building block för flesta sequential circuits
- *Enabled flip flops* är en variant där man har en ENable input, endast när den är på uppdaterar man värdet vid rising edge, annars kommer man bara ihåg gamla
- kan bli en glitch om ändrar Enable medans CLK = 1, se s.114?
- kan ha resetabble flip flop: har en reset bit, när den är 1 stter man output till 0 och ignorerar D, annars är det en vanlig flip flop. Kan vara synchronous eller asynchronous

kan bygga flip flops med transistors istället för gates, se s.114-115 (skippade)

en circuit är en synchronous circuit om och endast om
▸ Every circuit element is either a register or a combinational circuit ▸ At least one circuit element is a register ▸ All registers receive the same clock signal ▸ Every cyclic path contains at least one register

## Finite state machines
finite state machines med k registers har 2^k possible states
- i Moore machines beror outputs bara på current state, i Mealy machines beror på current state och current input

## Adders
- Half adder: input A och B, output A+B och carry
- Full adder: input A B carry, output Summan och carry
- långsamt att chaina ihop flera full adders eftersom måste propogata carry genom alla, kan istället dela upp i block där man snabbt räknar ut om en carry kommer från ett block för att slippa vänta på hela tiden (se s.239)
- s.242-243 om hur man kan göra en adder med logaritmisk komplexitet (fattade inte exakt)

## ALU
heart of most computers
- har en control signal som bestämmer vilken operation som ska göras, implementerad med multiplexors exempelvis
- har ibland flags för ex carry outs osv