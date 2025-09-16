#FinKap10
mer variable securities som small stocks och snp har högre potentiella returns än ex treasury bills men högre variability

expected return = $E[R], R \in [0,\infty]$
- använd detta eftersom inte alla investments har samma cash flows, initial prices, payouts etc för att kunna jämföra dem

variance/std för att mäta riskiness
- std är *Volatiltiy*

kan använda historical returns för att uppskatta framtida return distributions

Realized return är return som faktiskt händer över en tidsperiod. INkludera dividens och reinvestment!
- kan beräkna över flera perioder genom att multiplicera ihop
- kan averaga per year över en period, använda empirical distribution av returns under denna period
- volatility beräknas som stickprovsstandardavvikelsen = $\sqrt{\frac{1}{T-1}\sum_{1=1}^T (R-\bar{R})^2}$
- Standard error är volatility delat med $\sqrt{T}$, 95% confidence intervals längd är denna delat med 2

Nackdel med denna metodik är att lagom mycket data inte alltid finns

*Excess return* är average return av security över tid minus riskfri ränta (ofta tagen som average return av treasury bills) (visar riskpremie man får)
- mer risk/volatiliy = högre returns
- individuella stocks följer dock inte alltid detta lika mycket som t.ex index
	- Anledningen varför: se [[types of risk]]