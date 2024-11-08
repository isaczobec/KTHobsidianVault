#VLBokKap10
del av [[planning and control]]
efter man planerat genom [[loading]] [[sequencing]] [[scheduling]] måste man kolla att planen följs och rectifya deviations
- planera för sköta deviationsen, när ny deviation kommer återupprepas cyclen

## Push and pull control
- periodic intervention i activities av [[operations]] är en del av control
	- distinction mellan intervention signals som push / pull work genom processer
	- **push**
		- aktiviteter schemaläggs av centralt system
		- pushar igenom work utan tänka på om följande work centre kan göra något med det
		- eftersom actual conditions varierar från planer så kan detta leda till idle time, inventory and queues
	- **pull**
		- work station signalerar till tidigare station att de behöver produkter
		- produktion triggras av customer demand, passas baklänges

### Inventory consequences of push and pull
- pull ger mindre inventory; vanligt i lean

## Drum, buffer, rope
- kommer från TOC
- Visar var kontrol ska hända i en proccess
	- Alla workstations kommer inte ha samma load
		- --> en kommer vara en bottleneck
		- denna bör kontrolleras mest eftersom den bestämmer pace av the operation
		- bör ha en buffer av arbete efter bottlenecken så att det alltid finns något att arbeta på
		- bottleneck bör alltid producera
		- stationer innan borde inte producera snabbare än bottlenecken, ger bara buildup av massa produkter
			- bottleneck Måste alltså ha något sätt att kommunicera med tidigare stadier: Rope


skippade sista på s. 346 eftersom inte med i läshänvisningar #skipped 