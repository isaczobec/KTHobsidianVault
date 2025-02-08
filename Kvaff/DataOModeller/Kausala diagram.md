#KvaffKap7
ofta är analytikers arbete cykel av att modellera och utvärdera
- menar dock finns värde i börja modellering tidigare än så

Kan vara bra att visa orsakksammanband på grafiskt sätt med DAG (directed acyclic graph)
- visa förståelse för samband X o Y baserad på tillgänglig teoretisk förståelse/kunskap
	- visa förståelsen av systemet och datagenererande och dess samband 
	- kan vara utgångspunkt i vilken strukturell form i regressionsmodell man ska använda
	- Kan finnas förväxlingsfaktor (confounder) som påverkar både X och Y, om iinte kontrollerar för denna skattas sambandet mellan x och y systematiskt fel
		- Ex kan upplevt samband mellan x o y egentligen bero på att confoundern c gör att både x och y blir höga
	- Om S linjärt beroende av X (kolinjär) kommer de samvarierar, en del av variationen i X kommer tillskrivas S, blir skevt
	- Medierande variabel är en vilken är mellan beroendet av X och Y
		- om X endast påverkar Y genom M så är det full mediering 
		- kan skatta M genom ekvationsystem, med strukturell ekvationsmodell där båda ekvationer skattas samtidigt:
			- $Y = \alpha + \beta_1 X + \beta_2 C + \beta_3 M + \epsilon$
			- $M = q + w X + \epsilon$
	- Kan bortse från övriga variabler, om man inte anser att de kan påverka Y och *kanske* kan påverka X och således vara förväxlingsfaktorer


Finns vidare *Modererande Faktorer*
- Variabler/faktorer som påverkar styrkan av förhållandet mellan X och Y
- om = Z kan få följande ekv i regressionsanalys:
	- $Y = \alpha + \beta_1 X + \beta_2  X  Z$
- kan också kallas interaktionsterm, påverkar hur X påverkar Y; interagerar med X
- Kan studera moderation genom dela upp datamängd efter variabel man vill undersöka (som man tror är modererande (?)) 
	- Ex dela in i olika kategorier, Ex olika utbildningsnivåer
	- skatta $\beta_2$ i exemplet ovan, visar "styrkan" på moderationen
	- bra exmpel på detta s. 73
	- Nackdel med denna indelning är man förlorar data, färre mätpunkter för varje skattning -> bredare konfidensintervall, större std


