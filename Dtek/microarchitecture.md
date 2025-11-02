
artchitectural state = Program counter och 32 32 bit registers (specefikt i RISCV)


Micrarchitecutrue indelad i två delar:
- Datapath: alla sätt words of data är stored och operated upon(registers, memory, alu, multiplexers, etc)
- control unit: får instruktion från datapath och säger åt den hur instruktionen ska köras
	- skickar multiplexer select, register enable och memory write signals för detta

instruction memory, register file och memory är read combinationally, om adressen ändras kommer read busen ändras efter en simpel propogation delay, ingen clock involved
- Klockan kontrollerar endast writes
- eftersom state ändast ändras vid klock edges är fortfarande synchronous sequential circuit

Tre typer av microarchitectures:
- Single cycle microarchitecture
	- en instruction per cycle
	- limited by slowest instruction
	- behöver separata data och instruction memories
- Multicycle microarchitecture
	- executar instructions i flera kortare cycles
	- olika många cycles baserat på hur komplicerad instruktioner
	- kan återanvända delar, ex adders orsv, implementeras med nonarchitectural registers för intermediate results
	- endast ett minne, inte separat instruction och data memory
- Pipelined microarchitecture
	- som single-cycle processors, men kan executa flera instruktioner samtidigt
	- behöver extra logik och nonarchitectural pipeline registers
	- snabbre

för jämföra performance:
- det ända riktiga sättet är mäta execution time of program planning to run
- ![[Pasted image 20251026171456.png]]

runt s. 10 om hur datapath kan implementeras

Control unit har main decoder som genererar korrekta control signals till datapath baserat på vad instruktionen är, ALU decoder som dekodar vad ALU:n ska göra

kan vara bra att repetera 7.1-7.3 igen

# Pipelined processor
kör flera samtidigt, får högre throughput
har högre klockfrekvens så att alla steg hinns med på tiden det tar för en cycle i en singlecycle processor

**steg**
- Fetch, 
	- hämta instruktion från instruktionminne
- Decode, 
	- read source operands, decode instruction to produce control signlas
- Execute, 
	- computation med ALU
- Memory, 
	- read/write data memory om applicable
- Writeback
	- Skriv resultat till register file om applicable

delar in datapath i 5 stages
lägger till pipeline registers mellan stages för att propogata fram exempelvis write destination register in unison

kan bli errors om man försöker accessa värde man skrivit i subsequent instruction, inte hunnit komma till writeback stage än

kan lösa med forwarding: skicka fram värden från memory/writeback stages innan writeback till där de behövs i subsequent operations
- löser med multiplexers innan ALUn som bestämmer vad som ska användas som input

lw kan inte använda detta eftersom dess resultat inte blir tillgängligt innan memory stage, blir en two cycle latency instruction eftersom måste vänta två cycles till använda dess resultat
- kan lösa problemet med stalling: zeroa ut alla execute stage control signals så att ingen architectural state ändras, blir som en nop
- måste stalla alla innankommande stages om stallar en 
- måste flusha/cleara pipeline register direkt efter en stallad stage så bogus information inte propagatar frammåt
- implementar genom att kolla om lw i execute stage, och om loads destination register är samma som Rs1D eller Rs2D i decode stage
	- har sen enable registers och reset registers i pipeline registers

branch instructions computar om man ska hoppa i Execute stage, tills dess vet inte processorn vilka rätta nästa instruktioner är. Kan lösa genom att stalla i två cycles, men är inneffektivt, så predictar att branchen inte kommer tas och fortsätter executa vanligt. kastar bort resultaten om branchen tas.