#InteractionDesignKap14 
Sätt att genomföra [[Evaluation]]
Tre typer baserat på setting, user involvement, level of control:
1. Controlled settings directly involving users
	1. ex labb för observera beteende
	2. huvudmetoder usability testing, experiments
2. Natural settings involving users
	1. lite kontroll över användares aktiviteter, vill se hur skulle användas i riktiga världen
	2. main method = field studies
3. Any settings not directly involving users
	1. experter/researches modelerar/prediktar most obvious usability problems
	2. ex inspections, heuristics, walk-throughs, models, anlaytics

Finns för och nackdelar med alla typer
- lab-based kan visa usability problems enkelt men missa context of use
- field studies kan visa hur teknologi används i intended setting men kan vara svåra att genomföra
- modeling kan vara snabba men missa unpredictable/subtle aspekter av [[User experience]]

vad som används beror på produkt, vad man vill testa, resurser tillgängliga


## Controlled settings involving users
- designade för kontrollera vad och hur users gör saker med produkten
*Vanlig approach:*
#### Usability testing
- Usability testing involverar datainsamling i kontrollerad setting
	- datainsamling genom observationer, intervju, questionnaires
	- Huvudsakligt mål: **Determine om intended users kan använda interfacen för att göra intended tasks**
	- Ta bort externa faktorer, testa specefikt några funktioner för att endast se **deras** påverkan
	- Logga ofta actions med video eller logger
	- questionnaires för samla info om upplevelsen
	- all kvantitativ/kvalitativ data används i conjunction för att avgöra hur väl usability mål nås
	- Findings summarisas ofta till *usability specefication* som framtida prototyper kan testas mot, notera nivåer av performance. nya ändringar kan implementas och trackas (om det blev bättre/sämre ????)
	- exmpel: kan testa text input med olika devices för att avgöra om något signifikant bättre än någon annan


## Natural settings involving users
- huvudmål evaluera produkter med users i natural setting
**HUVUDSAKLIG METOD: FIELD STUDIES**
- huvudmål:
	- Help identify opportunities for new technology
	- Establish the requirements for a new design
	- Facilitate the introduction of technology or inform deployment of existing technology in new contexts
- vanliga metoder: observation, intervirews, interaction logging
- ska försöka vara unobtrusive, men svårt att vara det helt
- in-the-wild studies: hur nya produkter har blivit deployade och används
	- tappar lite kontroll över vad som observeras, mäts, när är in the wild
	- kan ex behöva rekrytera några användare, säga till de att använda den men inte ge mer instruktioner
- Nackdel: Svårt anticipata om/när något kommer hända, kan bli svårare att vara där och kontrollera/observera jämfört med i *usability testing*
- kan göra virtual field studies, ex i spel

## Any Settings Not Involving Users
- när researcher själv måste modelera och anticipata ex problem utofrån knowledge av usability, behaviour och context of use
- Exempel på metoder:
	- *Heuristic evaluation*: Knowledge av typical users, rules of thumb, walkthroughs som steppar genom scenario eller answerra set of questions
		- problem kan vara att heuristics inte är så accurate som de verkade vara
		- *cognitive walk-throughs:* simulera users problem-solving process med applikationen. fokus evaluera designs ease of learning
	- analytics kan också användas
		- samla in data från kunden 
- metoder används primarily för att jämföra effectiveness av olika interfaces för samma application


## Selecting and combinig methods
- olika metoder används ofta i kombinqtion för att få djupare insikt
- fördelar o nackdelar finns med alla metoder:
	- I controlled kan kontrollera hhypotes och generalisera
	- i uncontrolled kan få unexpected insights som är bra

## Opportunistic evaluations/explorations
- = generally när man tidigt i designprocess provide designers med feedbacj
- bra för man kan veta om värt fortsätta

