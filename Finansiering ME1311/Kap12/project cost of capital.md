#FinKap12
inte publivly traded company så kan inte använda historical data för beräkna beta eller denna
istället brukar man ta jämförbara firms cost of capital for assets
- exempelvis om firman är all equity:
	- Då är owning stock ekvivalent med owning assets, och om market risk av projektet vi ska göra liknar risken för average investments kan vi därmed använda equity beta och [[equity cost of capital]]
- Detta funkar inte om firm har levarage, då blir returns på firms equity inte representative av underlying assets returns,
	- EQuity blir mycket mer risky, så beta av equity blir dålig estimate
	- så måste därför ta portfolio med både equity och debt av firman
	- använd Unlevered cvost of capital $= \frac{E}{E+D}r_E + \frac{D}{D+E}r_D$
		- samma formel för beta
	- kan använda net debt istället = Debt - Excess cash and short term investments
	- kan average/använda flera asset cost of capital för liknande firmor för att minska estimation error


## Project risk characteristics and financing
- tidigare antagit att projekt bata finansierat med equity, ingen debt
- kan vara väldigt olik risk characteristics mellan olika avdelningar i samma business, kan vara bra jämföra bara med relevanta firmor (jämföra med relevanta comparables)
- opea´rating leverage hur stor andel i projektet som är fixed costs. Högre andel = högre market risk, bör ha högre cost of capital

## Financing and the WACC
- Några resultat angående hur man väljer att finansiera ett projekt:
- I perfect capital market (= market utan taxes, transaction costs etc) så har alla sätt att finansiera (debt respektive equity) samma [[NPV Desiscion rule|NPV]]
	- alla financing transactions blir 0 NPV
- Tax:
	- Får dra av interest rate payment från taxable income
	- Så interest rates på debt blir essentially mindre: $\text{Effective after-tax interest rate}=r(1-\tau_c)$
- WACC:
	- Så interest rate blir lägre och får accounta för det när man räknar ut cost of capital (dra av skatten på interest från från Unlevered cost of capital ($r_U$)):
		- $r_{WACC}=\frac{E}{E+D}r_E + \frac{D}{D+E}r_D (1-\tau_c)$
		- unlevered CC kallas alltså ibland pretax WACC
		- $r_U$ används för värdera projekt med enbart equity financing, eftersom ingen debt finns, och vi därmed inte kan dra av från skatten (vi begär därmed högre return). Kollar bara business/operating risk utan effekt från financing (ofta mer risky!)
		- $r_{WACC}$ för projekt som har samma ratio finansiering som firman, eftersom vi kan dra av lika mycket skatt
			- har också $r_{WACC} = r_U - \frac{D}{D+E}\tau_c r_D$ (discounta med skatt)

