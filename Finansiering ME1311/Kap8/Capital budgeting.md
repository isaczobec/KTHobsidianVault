#FinKap8
capital budget list alla projekt som man kommer göra under ett år
- bestäms genom processen capital budgeting

## INcremental earnings
Brukar börja med bestämma incremental earnings
- = hur earnings ändras av att man tar projektet
- != cash flow ändring

- Kan estimera alla kostander, och sedan beräkna net income för projektet som i [[Income statement]]
- Brukar inte ta  bort  interest expenses från EBIT här eftersom de hänförbara till valet av finansiering. Vill se incremental earnings av *själva projektet*
	- Kallar alltså uträknade earnings för ***unlevered net income***
- Ta bort income tax: $EBIT \cdot \underbrace{\tau_c}_\text{Marginal corporate tax rate}$

så
$$\text{Unlevered Net Income} = EBIT \cdot (1-\tau_c) = (Revenue -  Costs - Depreciation) \cdot (1-\tau_c)$$

## Indirect effects on incremental earnings
Utöver direkt invokade costs kan man ex ta resurser från annat projekt, ändra earnings på det viset
**Opportunity costs**
- Om använder resurs redan har, inte gratis, utan måste räkna bort värdet som best alternative use hade kunnat ge
**Project externalities**
- Extra kostander/losses inte direkt hänförbara till projektet som kan ge earnings/loss
	- Ex om säljer extra tillbehör till produkten, eller cannibalization

## Sunk cost and incremental earnings
kostnader som redan tagits eller kommer tas från projektet, kan inte påverkas
- ta inte med dessa i kalkylerna/incrementel earnings, kan inte påverka
- *"If our desiscion does not affect the cash flow, the cash flow should not affect our desiscion"*
- exempelvis
	- fixed overhead expenses
	- Past research and development
	- unavoidable competetive effects: om cannibalization inte gör något för att det är unnavoidable att vi ändå förlorar sales, exempelvis.

## Real world complexities
- ofta inte units sold eller pris konstant över tid
- många komplexa faktorer för företag

## Detemining free cash flow and NPV
- incremental income av projekt är inte cash flow
- ändringen av tillgänglig cash utan finansiering inkluderat är *free cash flow*
- för att bestämma free cash flow från incremental earnings
	- **CApital expenditurs and depreciation**
		- lägg tillbaka depreciation
		- ta bort för capiatl expenditures
	- **Net working capital**
		- = current assets - current liabiliteis = cash + inventory + recievables - Payables
		- måste eventuellt ha en viss nivå för att kunna göra projektet, måste räkna in i free cash flow
			- räkna med ändringar också
			- free cash flow är ju cash som inte är tied up, hence free
			- ökad NWC -> free cash flow minskar

man kan beräkna free cash flow direkt utan att först beräkna unlevered net income genom
$$\text{Free Cash Flow} = (Revenues - Costs - Depreciation) \cdot (1 - \tau_c) + Depreciation - CapEx - \Delta NWC$$
- Så depreciation ökar cash flow med en faktor av tax raten

## Calculating the NPV
- använd cost of capital som är best expected return on investment man kan få med samma risk och maturity
- summera ihop alla discountade cash flows som vanligt

## Choosing among alternatives
kan beräkna free cash flows och sen NPV för alla, och sen enligt [[NPV Desiscion rule]] ta den som har högst

## Further adjustments to free cash flow
**Other Non-Cash items**
- lägg tillbaka ex amortization av patent
**Timing of cash flows**
- kan ändra till månadsvis eller continous basis om behövs
**Accelerated depreciation**
- ?? verkade bara applya till US
**Liquidation or Salvage Value**
- Om likviderar/salvagar assets bör det läggas till i cash flow
	- måste betala skatt/frias från skatt baserat på gain on sale = sale price - book value
		- Book value = Purchase price - accumulated depriciation
**Terminal/continuation value**
- om inte forecastar alla perioder som projektet lägger
- lägg till en temination/continuation value som motsvarar marknadsvärdet av alla future cash flows *vid tidpunkten av terminationen*
**Tax loss carryforward**
- Om gör förlust ett år får man carrya fram losses och dra av på skatten upp till en procentsats av Pre-tax för kommade år (US 80%??)