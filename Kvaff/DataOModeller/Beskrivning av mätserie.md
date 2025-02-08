#KvaffKap2
- Analytikers jobb är analysera relevanta mönster från data som avslöjar något om verkligheten
- Måste dock kunna beskriva en mätseria och få översikt

- God vana att alltid skaffa översikt av dataset
	- bra översikt: förenkla så mycke som möjligt utan förvanska

- Mest översiktligt: Sammanfatta med ett antal *mått*
	- Lägesmått:
		- Medelvärde
		- median
		- mode
	- Spridningsmått:
		- Varianse
		- Standardavvikelse
- Kombination av dessa ger bild av intervall för var "typiskt" värde befinner sig
- Ovannämnda kan förvrängas av extremvärden, etc
	- Kan säga mer om fördelnignens utseende med kvantiler
		- vanligt med kvantiler (4)
- Låddiagram kan visualisera kvantiler och medelvärde
- Histogram delar i i delintervall
	- Kan ge information om outliers, extremvärden
- Täthetskurva = en utjämning av histogram
	- Om liknar en täthetsfunktion kan vi använda den för att modellera

## Jämförelse mellan mätserier
- Ofta interesant för analytiker
- Kan jämföra lägesmått, spridningsmåt, eller grafiskt genom histogram
- Analytiker föredrar i många fall överskådlighet ist för nyanser - gillar arbeta med jämförelser medelvärden
	- Jämförelse av medelvärden kan dock ge oriktiga bilder - kan ha varit väldigt varmt en dag och ungefär lika varmt resten av dagarna, medelvärde säger ändå att ena är varmare
- --> Ofta vanligt vilja ha mer kvalificerad jämförelse, formellt hypotesttest
	- Kan testa nollhypotes medelvärden skiljer sig ej åt
	- gör genom t-test, ok enl CGVS om lagom stora mätserier

Om har flera mätserier behövs generaliserat test för jämföra varians i dem
- Standardtest variansanalysis, ANOVA #läsmerkvaff
	- Om inte ger signifikant resultat förkastar man INTE att serierna har samma medelvärde
	- om ger signifikant res vill veta vilka serier som skiljer sig
		- Kan vara problematiskt jämföra 2 och 2: risk för felaktigt signifikant res ökar med antal mätserier
		- kan köra post-hoc test #läsmerkvaff efter anova som korrigerar för detta, bonferroni-korrigering för göra svårare för resultat att vara signifikanta #läsmerkvaff


## Beskrivning av samvariation
- korrelation och kovarians bra mått
- Kan vara så att mätserier korrelerar väl för vissa värden, dåligt för andra, måste använda scatter plots för att undersöka detta