#VLBokKap7
utöver val om [[basic layout types]] måste **mer detaljerad design** baseras på information om natur och volym acv flow att akomoderas, och workers/employee preferences

## Information for flow analysis of layouts
- finns väldigt många alterenativa sätt att organisera facilities relativt varandra på
	- --> in practice layouts bestäms av intuiton, common sense, trial and error, cad
	- kan ocks använda heuristic procedures; rules of thumb eller shortcuts i reasoning
		- kan hitta en bra subotptimal snarare än den aldra bästa


### Information and analysis for the design of fixed-position layouts
- detaljerad layout baseras på convenience av transforming resources, INTE födet av transformed resources
- gör layout så transforming resources kan maximera sin contribution
- kan bli väldigt komplext, speciellt om scheduled activities ofta ändras
	- ex building sites

### Information and analysis for the design of functional layouts
- innan börjar detaljerad design behövs information:
	- Area required by each work centre
	- constraints on shape of area of each work centre
	- degree and direction of flow between centres
	- desirability av proximity av olika centres/fixed points
-  Objective av design vanligen att minimera kostnader hänförbara t flöde i layouten (ex transportsträckor)
- kan använda manuella/cad metoder för detta

### information and analysis for the design of cell layout
- tar implicitly beslut när skapar celler:
	- the extent and nature of the cells to adopt
	- which resources to allocate to which cells
- huvudbeslut i detailed deisgn är att assigna appropriate  celler till appropriate produkter
- Ofta svårt att designa eftersom design är kompromiss av process och product layout
	- om väljer fokusera på process:
		- kan göra cluster analysis: 
			- vilka processer är naturally related; vilka produkter använder många linkande processer som således kan grupperas
		- kan göra production flow analysis (PFA):
			- ett sätt att allokera tasks och maskiner till cells
			- utvärdera produktkrav och process grouping samtidigt
			- ![[Pasted image 20241221153215.png]]
			- Sätt maskiner och components i matris och hitta groupings
			- Ofta inte jätte clean analysis: kan behöva investera kapital i maskiner som saknas i en cell, eller skicka vidare produkt till annan cell, vilket strider mot ordningen cell layout försöker skapa
				- kan också skapa remainder cells för det som inte tilldelades till celler, detta bibehåller ordningen

### information and analysis for the design of line layout
- eftersom tydlig process är detta snarare en fråga besläktad med [[process design]]
- main desiscions:
	- What cycle time needed?
	- How many stages needed?
	- How should task time variation be dealt with
	- How should the layout be balanced?
	- How should the stages be arranged (long thin short fat)?

--

### Information and analysis for the design of the appearance of facilities
- questionaires var vanligt för analysera customers och employees reaktioner t current och future workplace designs
	- tar reda på både dissatisfaction och satisfaction, eftersom de ofta är oberoende
- i modern tid använder ibland remote recording för förstå customers/employees reaktioner t layout och look av operations
