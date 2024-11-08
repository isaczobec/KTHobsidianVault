#VLBokKap10
en del av [[planning and control]]
*beslut angående i vilken ordning jobb ska utföras*
prioritet som ges till olika jobb avgörs av regler som ibland är komplexa:

### physical constraints
- Olika jobb kanske har fysiska kvaliteer som gör att de schedulas efter varandra
	- ex i fabric cutting kan små bitar bli waste om inte sequencar bra
### Customer priority
- en kund eller item prioriteras först beroende på om den är mycket större/viktigare än andra
	- eller ex missnöjda kunder i hotell, de kan påverka andra kunder negativt
- kan erode andra kunders service
- kan sänka performance av [[operations]] om flow disruptas för att tillgodose någon kund 
### Due date
- prioritera jobb efter när det ska vara klart
- ökar ofta deliver dependability and speed, och kan öka flexibilitet för urgent requests
- kan minska produktivitet genom förbiser mer effektiv sequencing
### Last in first out
- den sista som kommer in kommer ut först, ex i hissar
- inte equitable
### First in first out
- processesa items exakt i ordning de kom
- ex sortera mail/applications efter arrival date
### Longest operation time
- sequenca jobbet som tar längst tid först
- kan vara bra för maximerarar utilization genom att minska ställtider mellan jobb
- tar inte speed reliability flexibility into account; kan jobba direkt mot dessa
### Shortest operation time first
- prioritera den som tar kortast tid
- kan vara bra för att öka likviditet
- kan öka totalt levererade jobb, men kan minska produktivitet och skada service till larger customers

## Judging sequencing rules
- dependability, speed och cost viktiga för judga effektiviteten av sequencing rules
- några performance objectives som vanligtvis används:
	- meeting due date (dependability)
	- minimising time job spends in progress (throughput time/flow time) (speed)
	- minimising wip inventory (element of cost)
	- minimising idle time of work centres (element of cost)

Bra exempel S. 338
