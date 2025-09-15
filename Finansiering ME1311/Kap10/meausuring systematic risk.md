#FinKap10
måste göra detta för veta vilken riskpremie man vill ha

kan titta på korrelation mellan securities pris och en portfolio med endast systematisk risk - *efficient portfolio*
- efficient portfolios risk kan inte sänkas utan att sänka expected return
- kan anta att S&P är lagom stor för att vara fully diversified

för att hitta hur sensetive till systematisk risk:
- linreg efficient portfolio pris och secutitien
- får $\beta$: expected % change for 1% change in return of market (efficient) portfolio
	- tolkas som Hur sensitive security är till underlying economic conditions
	- beta låg för regulerade stabila branscher som ex läkemedel, hög för mer volatila som AMD eller Netgear

## Estimating the risk premium
mer risk averse investors vill ha högre
market risk premium:
- = expected return av efficient portfolio minus risk free ränta
- om beta är 1 är detta premiumen vi vill ha
- om ex beta är 2 kan vi istället för 1 kr i aktien investera 2 kr i perfect portfolio och fortfarande ha samma (absoluta) risk, men kunna tjäna 2x så mycket
	- Så då blir riskpremien 2x så hög
Så med allt detta blir
$$\text{Cost of capital for investment} \ I = r_I = r_f + \beta_I \cdot (E[R_{Mrkt}]-r_f)$$
Denna ekvation kallas *Capital asset pricing model* (CAPM)