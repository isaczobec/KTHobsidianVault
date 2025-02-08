#KvaffKap5
## Analysalternativ
finns många verktyg tillgängliga, ex maskininlärning etc, lätt komma in i 
- dock ofta svårtolkade/komplicerade resultat
	- => viktigt överväga om man kan göra tolkningar man interesserad av med enklare deskriptiv analys

***För exmpel att mäta om kvinnor äter mer frukt än män:***

## Enkla medelvärden
- beräkna medelvärde för fruktkonsumption för de datapunkter med kategoriskt (nominellt) värde män respektive kvinnor
	- Måste se om statisktiskt signifikant bör använda något test:
		- t-test (jämförelse av medelvärde mellan två dataserier med kontinuerliga värden)
		- ANOVA-test (jämförelse av medelvärde mellan två dataserier med kontinuerliga värden)
		- $\chi^2$-test (jämförelse mellan två eller felera dataserier med kategoriska (nominala eller ordinala) dataserier)

## Normering av data
- Man kanske fått signifikant svar på frågan man ställde tidigare, och god [[reliabilitet och validitet|validitet]], men vet inte exakta orsaker bakom observerade resultat
	- Kan av denna anldening studera normerade data: ex *kvoten* mellan fruktkonsumption och total matkonsumption mellan datapunkter med olika kategoriska/nominella värden på kön för undersöka preferenser

## Trimming av data
- Ibland kan finnas faktorer som är korrelerade med variabeln man är interesserad av, och som systematiskt är korrelarad/annorlunda mellan olika kategorier (män/kvinnor)
- Ex kanske fruktkonsumption beror av hur många ggr/vecka man tränar, och denna systematiskt olika för män/kvinnot
- -> svårt att tolka vad resultaten faktiskt beror på, kanske vill undersöka skillnaden mellan två kategorier *allt annat lika*
	- Ett primitivt sätt åtgärda allt detta: Skära bort mätpunkter där den störande faktorn är över en viss gräns etc
		- Nackdelar: Studien får bara validitet för mindre del av stickprovet, och gör sig av med observationer, sämre precision i punktskattningar

## Regressionsanalys
Kan applicera multipel regressionsanalys, ex av normerade värden:
$Konsumtion = \alpha + \beta_1 \cdot kön + \beta_2 \cdot träningsfrekvens$
och ta $\beta_1$ (m konfidensintervall) som en indikator på styrkan av ev. samband mellan kön och konsumtion
- Mycket mer svårtolkat, kräver tekniskt förståelse hos mottagare av analys

