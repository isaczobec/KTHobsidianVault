
en transaction är en series of operations en [[DBMS]] måste executa amotically och isolated
- ensurar durability genom att alltid spara resultatet före och efter varje transaction
- har en *transaction manager* som acceptar *transaction commands*
- transaction processor gör följande:
	- Loggar data: skriv alla ändringar
	- Concurrency control: *scheduler* se till att inga konstiga effekter av flera transactions samtidigt
		- har locks och lock tables
	- deadlock resolution från stage ovan
	- 