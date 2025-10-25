
# accounting.md
#FinFL1
Stock (financial status) vs flow (rate of change) variables
**financial status**: balance sheet
**rate of change**: income statement


# finance.md
#FinFL1
= Anskaffa resurser för projekt
- firma har resurser för vissa projekt men inte alla, måste prioritera
	- $\rightarrow$  är ett projekt bättre än andra?

Investment desciscions är long term
- Men osäkerhet gör det svårt att investera long term

handlar om quantitative desiscion making
- quantifying benefits/costs så att desiscion making blir simplified
- 
Accounting ger mycket av siffrorna man använder
- visar dock inte [[opportunity costs]]

Business activities uppgörs av
- 1. valuation av assets
- 2. management av assets

måste measura för kunna valuera
objectives + valuations -> desciscions



# management.md
#FinFL1
How should i save/spend?
what buy/sell?
when buy/sell?

# opportunity costs.md
#FinFL1 

vad man är missing out on när man investerar i något annat

Skapa business när $Revenue \gt Costs$


# risk.md
#FinFL1
How model the unknown?



# time.md
#FinFL1
Cash flows now not same as cash flows then
- consumptions needs
- can invest now
- $\rightarrow$ how should we model temporal differences?

   

# valuation.md
#FinFL1
How are financial assets valued
- how should be valued
how do financial markets deermine asset prices
how well do financial markets work

# Finansiering_Lecture11.md
Två pelare för resource allocation:
- Market economy pursuar effektivitet
- goverment correctar market failuires när dåliga externalities (=effekter från ekonomisk transaktion för tredje part) hindrar effektivitet

Shareholder value approach: Corporations ska kontrolleras av profitmaxxande shareholders medan andra stakeholders skyddas av kontrakt och regulation

att intenaliza externalities: företag får själva kostnaden/benefit av sina externalities
- Motstånd mot detta kan vara
	- capture av lobbying och andra
	- territorialiy of jurisdiction
	- inefficiency, high transaction costs, poor infomraiton and high delivery costs (gov failure)

Hur passar sustainiability in i NPV modellen?

corporate governance = se till companies not run by owners run in owners best interests
- Guiding principles:  
• Provide a clear norm for good corporate governance in Swedish listed  
companies based on established and accepted principles,  
• be sufficiently ambitious to provide an alternative to legislation on issues  
where self-regulation is preferable, and  
• be applicable to all stock exchange listed companies without causing  
unnecessary administration or unjustifiable expense.

**Bolagsstyrning i sverige**
- Valberedning för bolagsstämma
- styrelsen: bolagets organisation och förvaltning av angelägenheter
	- majoritet ska vara oberoende av bolaget/bolagsledningen
	- minst två oberoende av största aktieägarna
- VD: löpande förvalta bolaget
	- bereda med styrelsen det som faller utanför löpande förvaltning
- REVISOR utses av bolagsstämma
	- Granskar årsredovisgning & bokföringen & styrelse/vds förvaltning
	- informerar om risk för ersättningsskyldighet

**Corporate governance generellt** [[agency costs of levarege]] [[agency benefits of leverage]] [[agency costs and the tradeoff theory]]
- Problem separation ownership och mangagement och förena intressen
- OFta tidshorisont av managers/insiders för kort för att ärligt försöka bygga bra reputation
- exempel privatjet: [[agency benefits of leverage]]

**monitoring**
- görs av board och t.ex. finansinspektionen
- tänker ofta på andra stakeholders än bara shareholders

**Dual class shares**
- shares med fler röster, ofta ägda av controlling party som bara issuar vanlig stock, för att behålla kontroll

![[Pasted image 20251005190006.png]]
![[Pasted image 20251005190227.png]]

PE-backade firmor har bättre business practice

**CSR**
- kan tänka att edt finns business case för bra CSR behaviour
	- Finns evidence att csr beteende och returns korellerar, korrelation/kausalitet?
	- skillnad i operating performance och stock market performance
- Kan också tänka sacrafice profits för social good
![[Pasted image 20251006120416.png]]
	- financial materiality is information that is likely to be important for investors to make investment desiscions
	- material sustainability issues är issues som likely kommer påverka företagets performance och stakeholders

**ESG**
- Gör CSR efforts measurable

# Finansiering_Lecture12.md

**Climate risks and market efficiency**
- [[hong et al]] 
- mäter om drought risk index påverker stock prices av food stocks
	- Finding är att drought index forecastar poor profit growth för food companies och poor food stock returns i samma land, av vilket man kan dra slutsatsen att marknaden inte effektivt reagerar på climate change risks

i teori ska goal of firm bestämmas av firms owners
- management/cheif officiers prioriterar ofta employees, customers och environment högt också


![[Pasted image 20251005202035.png]]

# GRAHAM
textbook model only partly fits reality
- short horizon for reliable forecasting, only accurate two years ahead
- simple sticky heuristic desiscion rules. Use rules that worked, dont change often.
- more attention to minimizing negative suprises than attaining positive surprises
- uncertain forecasting - error prone
- more focus get revenue grwth and other stakeholders than just textbook shareholder value creation
- capital structure may vary from academic predictions

Implications of this
- managers use good enough rules and patterns instead of perfect because the world iscomplex and rapidly changing
- om leder företag med dessa heuristics kommer agerande variera från det rationella optimerade long term modeller säger
- firms prioriterar near term cash flows, conservative desiscions och risk minimization

Hurdle rates
- Hurdle rates är ganska mycket högre än WACC
- Dessa ändras sällan, ändras inte angående fluctuations i market interest rates, conservative approach för investement desiscions
- höga hurdle rates eftersom
	- Buffer mot osäkerhet
	- minimera risk
	- simplify desicion making att ha hög tydlig cutoff
	- agency: vill undvika negativa implikationer med att inte nå expectations
- detta kan leda till att positive npv investements inte görs

# firm-specific vs systematic risk.md
#FinKap10
stock prices fluktuerar ofta baserat på två typer av news (kopplade till [[types of risk|independent och common risk]]):
- firm specific news (firm-specific risk)
	- enskilt till firman
	- independent risk
- market-wide news (market/systematic/undiversifiable risk)
	- hela marknaden eller ekonomin, påverkar alla stocks, ex att interest rates blir lägre
	- common risk

No arbitrage:
- independent return firmor (med expected return högre än risk free rate) borde inte ha en riskpremie, eftersom:
	- Kan låna till risk free interest rate
	- köpa många independent aktier så att risken går mot noll
	- detta är essentially arbitrage. Priset kommer gå upp och opportunityn kommer försvinna
- slutsats: diversifiable risk har ingen risk premium
	- istället har securities som systematiskt rör sig med ekonomin risk premium

se [[meausuring systematic risk]]

# meausuring systematic risk.md
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

# risk and return.md
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

# types of risk.md
#FinKap10
common risk:
- risk som är perfectly correlated

Independent risk
- ingen korrelation
- averaging out of risk i stora portfolios med independent risk = diversification


skillnaden blir att man delar med kvadratroten av antalet observations i independent risk, men inte i common risk (mer risk!)

detta påverkar risk of stock portfolios: se [[firm-specific vs systematic risk]]

# Fördelar med CAPM.md
#FinKap12
errors i cost of capital ger mindre påverkan än ex i cash flows
assumptions man måste göra är straight forward och enkla att dokumentera
- managers fipplar mindre
får managers att tänka på risk på rätt sätt - inte bry sig för mycket om diversifiable risk


# debt cost of capital.md
#FinKap12
debt yield är IRR av att hålla till maturity, alltid högre eller lika med expected return (då kan defaulta)
- så $\text{Bond expected rat of return} = r_d = y - pL$ s. 454
- detta blir ens debt cost of capital

# equity cost of capital.md
#FinKap12
Under capm assumptions: cost of capital av en investment opportunity blir expected return av en investment med samma beta som denna (se [[meausuring systematic risk]] )
- kan använda denna cost of capital för att värdera stock ex i [[discounted free cash flow model]]


för att använda CAPM behövs en market portfolio att jämföra med
- kan göra en market portfolio genom att vikta alla aktier efter deras market cap i proportion till total market cap
- kan också använda market indexes (ex SNP 500)
- Dow Jones är price weighted: har equal number of each stock
- #clarifyFin vad är value vs price weighted?
- kan investera i dessa genom index funds eller ha exchange traded funds (ETFs) som motsvarar ownership i portfolios

Dessa securities är bara market proxys- följer inte exakt "true" market portfolioe

### Determinig risk-free rate
- Kan använda rates from corporate bonds istället för treasury rates för att dessa ibland är högre
- använd rate av bonds som motsvarar tidsperioden av investeringen
- risk premium har declined over time, bmindre risky att investera nuförtiden?

**Problem med using historical data to esitimate market risk**
- fortfarande stor standard error i returns fortfarande stora med mycket data, se [[risk and return]]
	- kan istället anta constant growt och ta $r_{Mrkt} = \frac{Div_1}{P_0}+g$ #clarifyFin varför funkar detta? s.449
		- mer rimligt med const growth för hela marnaden

### Estimating Beta
- beta är mått på market risk
- Beta verkar hålla sig ganska jämn över tid för de flesta företag, så använder in practice beta från historisk data
- kan plotta Excess return för market portfolio och för securityn, se beta

#skippedFin använda linreg s.452

# project cost of capital.md
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



# identifying alpha.md
#FinKap13
Alla som håller market portfolio kommer kolla required return (räknas ut med CAPM-metoden) och deras expected return, och skillnaden mellan dessa (skillnaden mellan market portfolio line i grafen med expected return och volatility) är alpha
- att köpa om man ser är högre eller sälja om ser är lägre drar alla investments mot linjen (se sida 482, 483)
- enligt CAPM assumpitons är marknaden alltid effektiv, men obviously är market portfolio inte alltid det. Competition gör det dock nära

# investing styles.md
#FinKap13
## Size effects
- small stocks har historically högre returns än market, också högre betas och market risk, men ändå högre returns, detta kallas *Size effect*
	- större stocks har lägre beta, lägre alpha och lägre expected excess retur
- Book to market ratio, hög för value stocks, låg för growth. 
	- value stocks brukar ha hög alpha, growth brukar ha låg

en anledning till size effects kan vara att stocks med hög expected return måste ha lågt pris och låg market cap, så att de ger de höga returnsen. Om marknad inte perfekt effektiv kan man profita på dessa då, men mindre och mindre likely desto större stocksen blir

## Momentum
evidence visar att tidigare höga alphas ibland korrelerade med höga framtida alphas
enligt CAPM bör detta inte kunna hända

Att investors gör positivve alpha investment strategies implicerar en av två saker för CAPM:
1. Att investors inte tar dessa investments som har högre NPV
2. Att det finns systematisk risk som inte korrekt fångas i Beta (kanske för market portfolio inte efficieant)

Det finns mycket information och många funds som gör strategierna, så förmodligen är option 1 fel, lämnar option 2: market portfolio inte helt efficient
- anledningar varför:
	- proxy error: värklig portfolio har ALLT i ekonomin, finns ingen data för allt
	- fatta inte behavioural biases s.504 #clarifyFin 
	- Andra risk preferences: kan vara villig att hålla diversifiable risk om det ex finns liten chans för väldigt hög payoff

# Market value balance sheet.md
#FinKap14

en application av MM proposition I är att kan göra market value sheet:
- ta med även *intangible* assets som brand name etc
- använd market value för allt
- värdet av alla securities issuade av firman måste equal alla assets

Kan därmed beräkna market value of equity genom: market value of assets - market value of all debt and liabilities

att ex låna för att köpa tillbaka shares ändrar inte priset på aktier, se s.533
- får mindre equity och mindre shares outstanding: Equity per share fortfarande samma
- värdet för shareholders är fortfarande samma


# equity vs debt financing.md
#FinKap14
vanligast financa investeringar genom antingen bara equity eller equity och debt kombination

### FInancing firm with equity
- Present value av equity cash flows om financar projekt med equity är cash flowsen discountade till appropriate equity cost of capital 
- använd expected cash flow
- företaget kan då financa med equity och behålla hela NPVn av projektet
- ^^ exempel s 525
- detta är om har *unlevered* equity - equity i firma utan debt

### Financing firm with debt and equity
- Interest/debt payment kommer före equity
- Om garanterad få större cash flows än det man behöver betala tillbaka blir debt risk free, så kan låna till risk free rate. 
	- Men equity bler mer risky

Miller och modigilani menar att total value av firm bör vara oberoende av financing i perfect capital markets
- enligt law of one price måste combined value av equity och debt vara NPV av alla cash cash flows från projektet, så levered equity E = unlevered equity - debt (s.527)
- samma NPV för entreprenören oavsett
- även fast NPV ökar för levered equity ökar också risken så då bör man inte discounta till samma cost of capital )(s.527)
- Levered equity holders får högre riskpremie

## Modigliani-Miller I: leverage, arbitrage, and firm value
- deras resultat håller under mer general conditions kallade *perfect capital markets*:
	- Allt tradas till NPV av future cash flows
	- Inga taxes/transaction costs
	- financing desiscions påverkar inte framtida cash flows
- MM proposar total value of firm securities = market value of cash flows generated by assets of firm, unnafected by capital structure
	- detta eftersom alla cash flows betalas till security holders, och enligt [[Law of one price]] måste dessa securities värde vara lika med alla assets värde, om financing desiscions inte påverkar cash flows

### Homemade leverage
- om inte firma har investors desired leverage kan de låna själva för att få det
- ekvivalent med om firm hade lånat, så länge interest rate är samma, exmepel s. 530
- kan istället hold bonds to reduce leverage


inget värde skapas/ändras i firman av att sälja/ändra securities

se [[Market value balance sheet]]

# leverage, risk and the cost of capital.md
#FinKap14
MM proposition 1 säger (market value of all) Equity + debt = equity if firm was unlevered = assets

kan uttrycka unlevered return som viktad average av return on equity och return on debt, skriv om dett för att se att return on equity ökar (om firman presterar bra) med leverage (s. 534 och 535)

detta leder till MM proposition II: $r_E = r_U + \frac{D}{E}(r_U-r_D)$
- denna formel gäller även för beta

## Capital budgeting and the WACC
då firmans assets motsvarar dess securities kommer deras cost of capital vara samma enligt proposition ovan, så den kommer bli equal pretax WACC (eftersom perfect capital markets), så $r_U = r_{WACC} = r_A$ just här
$r_{WACC}$ unnaffected av leverage i dessa conditions då $r_E$ ökar när debt ökar
- då man kan värdera enterprise value med WACC enligt [[discounted free cash flow model]], och wacc oberoende av financing, och vi antar att kassaflödena också är det, blir företagets värde unnaffected by financing

WACC om har mer än två typer av securities räknas ut som weighted average av alla

unlevered beta (mäter assets underlying risk) konstant med olika financing men inte equity beta, se formeln ovan


Leverage ökar Earnings per share, men risken ökar också och security transactions i perfect capital markets måste vara 0 NPV, så share price kommer inte ändras
- extra earnings kompenserar extra risken som tas så ingen ändring i share price
- då equity cost of capital ökar discountar vi mer vilket sänker share price och kompenserar ökningen

tack vare att price to earnings och EPS ändras med levarage måste man använda valuation multiples som tar EBIT (earnings innan *interest*) into account om jämför firmor med olika capital structures

en annan fallacy är dilution: om tar in nya pengar växer assets vilket motverkar att mängden aktier växer, och aktiepriset bör vara oändrat om de issuas till ett fair price. gain or loss av detta för shareholders beror ändast på investeringarna som görs med nya kapitalet

ett sätt att reframa MM propositions är att i perfect capital markets adderar eller subtraherar inte financial transactions value, utan bara repackagar risk och därmed ändrar returns

# interest tax deduction.md
#FinKap15
Anledningen varför financing desisicons spelar roll (se [[equity vs debt financing]]) är eftersom att världen inte är en perfect capital market, utan execmpelvis *taxes* finns

men då leverage innebär  att de minskar tax (och interest betalas till debt holders) ökar totala cash flow avaliable to investors (debt och equity)
- gör att man kan raisa mer capital

detta kallas för interest tax shield
- = extra amount would pay if did not have leverage = $\tau_c \cdot \text{interest payments}$
- för att värdera denna, använd [[NPV Desiscion rule|NPV]] av alla cash flows skölden ökar
	- cash flows ökar med denna skölden för investors
	- Detta ändrar MM proposition I till att levered firms är värda mer än unlevered firm med present value av tax shieldrn
	- så om vi vet alla interest payments kan vi värdera den
		- Detta är sällan fallet, mängden debt kan ändras, interest rate kan ändras, tax regler, osv
		- men om constant interest payment blir PV $=\tau_c \cdot r_f \cdot D / r_f = \tau_c \cdot D$ (eftersom perpituity formula)
		- market value of debt är present value av alla framtida interest payments

WACC med interest tax deduction blir att man multiplicerar debt termen med 1 - tax rate
vissa siktar constant debt to equity istället för konstant debt

se [[recapitalizing to capture the tax shield]]

# optimal capital structure with taxes.md
#FinKap15
för external funding preferar firms ofta debt
- men mer capital expenditures en extern debt, visar att majoritet av investments görs ex med retained earnings
	- även fast ny equity inte issuad så ökar då market value of equity eftersom firman har växt

ofta har företag cash för att offsetta effective debt
- net debt = debt - cash
	- denna låg eller negativ för ex biotechnology, hög för ex automotive industry


för att få optimal tax reduction måste man inte ha 100% debt funding
- måste ha taxable income till en viss del, kan inte exceeda 30% av EBIT avdragen
- när når 30% gör extra debt inget, ingen extra tax shield
- en formel för hur det blir sämre för personal investors med för mycket debt på s.576
- med detta i åtanke blir optimal level debt den som är exakt på limiten för avdragning

## Groawth and debt
- om inte har någon taxable income hjälper debt inget, ger ingen tax shield
- om förväntar growth bör interest payments fortfarande vara lågt under EBIT
	- Om har limit på deduction $K \cdot EBIT$ så är $\text{Interest} = r_D \cdot Debt \leq K \cdot EBIT \iff Debt \leq K \cdot EBIT / r_D$
		- Så optimal nivå debt proportional till earnings
		- högre growth rate gör också equity mer värdeful så då bör *ration* equity till debt som är optimal också bli lägre

in practice har firms lägre debt än det som presenteras som optimalt här
- den sannolika förklaringen är att debt ökar risken för bankruptcy, inte tagits hänsyn till här

# recapitalizing to capture the tax shield.md
#FinKap15
när ex tar debt för att buyback shares kommer equity value minska med hela firmans värde öka (se [[interest tax deduction]])

### Share repurschase
- låt säga att köper tillbaka till current share price, då kommer share price öka så att de som är kvar blir värda mer. denna ökning motsvara ökningen i PV av firman som orsakas av tax shielden
	- men detta blir arbitrage, så när uppköp announcas kommer marknaden justera sig själv aoutomatiskt: öka direkt till value of equity innan debt tas + tax shield PV
	- ökar till priset mittimellan gamla och nya priset efter repurchase så att de som behåller/blir uppköpta tjänar lika mycket
	- kan kolla market value balance sheet p s.567 för att se detta

# Financial distress costs and firm value.md
#FinKap16
då bankruptcy kan ha indirect costs, och detta bara kan hända om har leverage, kan i motstridighet till MMs assumptions om att capital structure inte påverkar cash flows violatas och därmed kan firm value påverkas av financing
- exempel s.599
- shareholders bryr sig inte om dessa kostnader efter bankruptcy
- creditors kommer i utbyte vilja låna ut mindre i början - NPV av dess kostnader mindre (de betalar mindre för debt)
	- detta gör att firman får mindre pengar till investments, dividends, repurchase shares, vilket minskar pengarna för equity holders
	- så *egentligen* är det shareholders som betalar för NPV kostnader av bankruptcy

för bestämma optimal nivå debt med detta i åtanke: [[The tradeof theory]]

sammantaget är det inte själva risken att bankruptcy händer som minskar firm value, utan kostnaderna *associerade med* bankruptcy som gör det

# The tradeof theory.md
#FinKap16
för hitta optimal nivå debt, så måste man balansera [[interest tax deduction]] och [[Financial distress costs and firm value]]

enligt tradeoff theory är value of levered firm = value of unlevered firm - PV (Interest tax shield) - PV(FInancial distress costs) (se s.600)

för att beräkna PV(Financial distress costs) måste man veta
1. probability av distress
	1. beror på mängd debt, volatility av cash flows/asset values
		1. så firms med steady cash flows (ex utility) kan ha mer debt än ex semiconductors
2. costs associerade med distress
	1. Beror ex på typen av assets: om mycket tangible lätt att likvidera (ex Real estate), låga kosts. om istället mycket human capital behöver man mycket costs för att se till att de stannar/hire new personal etc
3. cost of capital av distress
	1. Eftersom dessa inversly korrelerar med hur bra företaget gör ifrån sig, kommer beta likely vara opposite för dessa -> låg för hög beta firms -> högre NPV av distress costs

Enligt denna theory bör man öka debt till max vörde är nått, när value of levered firm är max

ett annat sätt som cash flows kan påverkas av capital structure är [[agency costs of levarege]]

# agency benefits of leverage.md
#FinKap16
kan ist för [[agency costs of levarege]] öka motivation för managers att göra bra saker att vara debt financed
benfits:
- **conentration of ownership**
	- Orginella ägare får alla benefits/earnings om de äger all equity, kan motivera de att jobba hårdare
	- om ist har equity jobbar man kanske mindre hårt och köper massa corporate perks för att man inte själv behöver betala
	- agency costsen som kan uppstå av att ha equity betalas av shareholders: värdet på aktierna går ner, speglar dålig performance av firman

managers ofta low stakes i firmorna, kanske inte blir lika motiverade som om de hade mer

en annan concern är om managers gör unprofitable investments
- kan vara villig att göra -NPV investments för aura: empire building (gillar runna stora företag)
- även overconfidence

för att kunna vara wasteful måste excess cash kunna finnas: *free cash flow hypothesis*
- Egentligen behövs inte mer cash än så mycket att man kan göra alla +NPV investments och möta payment obligations
- mer sparsam med tight med cash: leverage genom interest payments kan göra firmor mer sparsamma
- threat av financial distress kan också öka managerial vigor

se [[agency costs and the tradeoff theory]]

# agency costs and the tradeoff theory.md
#FinKap16
med [[The tradeof theory]], [[agency benefits of leverage]], [[agency costs of levarege]], [[Financial distress costs and firm value]] får vi en mer komplett ekvation för levered firm value (se s.613)

exempel på nivåer debt för olika firmor s.614
- R&D volatil, låga cash flows -> lite debt
- Low growth, mature firmor: tangible assets, stabila, höga cash flows och möjlighet till tax shield -> mer debt

# agency costs of levarege.md
#FinKap16
en potentiell konsekvense av att ha levarage: eftersom managers ofta håller shares själva kan de ibland ta desiscions som är bra för shareholders men dåligt för debt holders, och minskar värdet av hela firman för alla investors

exmpelvis när facar financial distress:
- då kan de ta desiscions som är väldigt risky och har negativ NPV, för shareholders har inget att förlora på det (om de gör inget och det blir bankruptcy förlorar de allt). Det är bara debt holders som förlorar. Essentially gambling med deras pengar (exmepl s 603-604)
- att byta safe assets mot risky assets såhär kallas *asset substitution problem*
	- debt holders kommer i anticipation av detta kanske betala mindre initialt
- i financial distress finns också risk för debt overhang/under-investment-problem:
	- Kan inte raisa funds genom equity för positive NPV investments: måste ge returns till debt holders innan equity holders, som minskar equity holders returns och gör att investeringen har negativ NPV för de men positiv NPV för firman
	- dåligt för både equity och debt holders med missad NPV, och mest prevalent i firmor med lönsamma opportunitites som kräver stor investering
- Cashing out finns också: sälja assets till lågt innan defaultar/distress så att investors kan få viss mängd utvelning trotts väldigt negativ NPV
- för att estimera när investors kommer göra ett projekt kan man använda cutoffen (s. 605-606) $NPV/I > D/E \cdot \beta_D/\beta_E$

även fast detta ökar value för shareholders in time of distress så minskar det värdet överlag för de, för creditors ger mindre betalt för debten initially. Minskar share price med mängden av NPV av alla dessa kostnader och distress costs
- alltså påverkar även agency costs optimal leverage

en annan agency cost: om redan har debt, och tar mer, kommer de potentialla downsidsen för de nya creditorsarna falla på de och de existerande, inte på shareholders, så redan leveragede firmor kan villja ta mer debt så att shareholders kan få payout (s.607)
- vidare: om har excessive debt kan man vara ovillig att minska debt, eftersom risken med debten kommer bli mindre och den kommer bli dyrare, vilket är gynsammt endast för debt holders (s.607)
dessa kallas *leverage ratchet effect*: kan vara villig att skaffa debt fast minskar value, eller ovillig minska debt även fast ökar value 

Agency costs mest prevalent för lång maturity debt eftersom mest opportunitties att missbruka då
kan göra kovenanter som creditor: regler för vad firman får/inte får göra, ska minska agency costs, ex inga excessive pauouts
- kan dock försvåra management och göra det svårare att göra +NPV instructions



# assymetric information and capital structure.md
#FinKap16
managers mer likely att ha curcial information än outside investors

credibility principle: managers som claimar saker i sitt och firmans egna intresse måste backa upp det med actions som hade varit för costly om stamtementsen inte var sanna
kan signalera att man tror man kommer växa mycket genom att ta debt: hade inte kunnat betala tillbaka annars/hade varit dumt: *signaling theory of debt*

**Adverse selection**
- lemons principle: När säljare har ***privat*** information så discountar köpare priset för de är skeptiska, pga adverse selection:
	- Ex om säljer begangnad bil till lågt pris tror man något är fel med den, betalar ett lägre pris
		- -> endast de med faktiskt sämre bilar säljer = adverse selection

detta gäller även för raising equity. Om firm vet att deras stock price kommer gå upp till följd av unannounced opportunity vill de inte issua shares till det nuvarande låga priset, och tvärtom
- köpare discountar för att det finns risk att managers har dålig information, och allt detta är en kostnad för firman

### IMplikationer
- Stock price sjunker när issuar shares (eftersom folk tror firman tror shares är overvalued)
- stock price ökar ofta innan announcement of equity issue
- firms brukar issua equity när assymetry är minimerad, ex innan och efter rapporter

### Implikationer för capital structure
- Om managers tycker stocken är underpriced kommer de, så att shareholders inte ska förlora värde, prioritera att issua debt eller använda retained earnings
- tvärtom vill ofta issua stock om tycker den är overpriced
	- Detta kommer dock minska share price vilket kan vara en deterrent

generellt prioriterar managers retained earnings ; *pecking order hypothesis* (issua equity minskar share price)

överlag innebär detta att financing desisicons utöver det som nämns i [[agency costs and the tradeoff theory]] påverkas av hur managers tror firman är värderad right now (over/underpriced)

# bottom line of capital structure.md
#FinKap16
enda saken som gör att capital structure påverkar mer än bara risk för equity holders är market imperfections: taxes, agency costs, financial distress costs

# default and bankruptcy in perfect market.md
#FinKap16
financial distress är när man inte har råd betala obligations/interest/owed money till debt holders?

firms obliged att betala sina debts, kan resultera i default
- equity har inte denna risk

enligt MMs propositions i perfekt marknad behöver detta necesarily inte vara en disadvantage
- enligt de kan man i capital market issua ny equity eller debt om *assets exceed liability* och betala tillbaka debt även om man inte har allt i cash
- om istället inte har lagom assets för att betala kan debt issuers ta legal ownership. Kan dock inte stämma shareholders på värdet eftersom de har limited liability, så de får acceptera en viss loss
- om har leverage eller inte påverkar inte hur mycket en firma förlorar vid dåliga investments, se s.591
- alltså, återigen MM1: financing påverkar inte hur mycket som förloras, ingen nackdel med debt, och kan raisa lika myckert från investors initially oavsett structure

Däremot shifta bankruptcy värde från investors till debt holders (men totalla värdet för alla investors ändras inte)

dock så är bankruptcy inte så friktionsfritt som perfect capital markets assumar
- exmpelvis om flera creditors bitvis tar assets minskar remaining värde eftersom assetsen inte är värda lika mycket apart
- finns för att motverka detta flera typer av liquidation:
	- Chapter 7 och 11, se s.593 (7 liquidation med auktion, 11 är reorganization plan)
	- Dessa processer har stora fees, ex för investment bankers / legal teams etc
		- vissa fasta kostnader gör att procentandelen tappat värde pga detta är större för små firmor
		- kan försöka göra prepacked bankruptcy, planera hur ta sig ut innan
- finns andra indirect costs av financial distress:
	- loss of customers, suppliers, employees, receivables, fire sale of assets, innefiicient liquidation, costs to creditors

eftersom creditors/investors kan välja om ska göra bankruptcy osv bör de inte göra det om ovannämnda kostnader är större än kostnaderna av att renegotiata / göra workout eller prepackaged bankruptcy


för att estimata impact of dessa indirect costs:
- estimata losses till total firm value, inte bara för debt eller equity holders
- sen estimatar man [[Financial distress costs and firm value]]

# comparasion of dividens and share repurchases.md
#FinKap17
vilken [[distributions to shareholders]] är bäst?

enligt MM i perfect capital market är repurchase vs dividend samma, spelar ingen roll

om har dividend:
- då share price = PV(all future dividends) ökar den innan dividend med dividenden, och efter ex-dividend date sjunker den med dividenden. shareholders wealth ändras alltså inte över ex-dividend date då de blir berättigade till utdelningen
- mängden cash sjunker vid ex-dividend date och då sjunker också stock price

om har buyback:
- Minskar värdet av assets genom att  minska cash, men mängden shares outstanding minskar också vilket offsettar detta och gör att share price håller sig samma
- priset minskar inte heller eftersom att framtida dividends blir större med färre shares outstanding
- sså ingen effekt på priset

### Vad prefferar investors?
- Samma totala wealth efteråt, men en andel i cash om dividend
- men kan bara sälja/köpa stock efteråt baserat på sin preference, så ingen verklig skillnad oavsett => indifferent

om ger higher dividend direkt genom att ex issua equity kommer shares outstanding att öka, och därmed kommer utbetalda dividends bli lägre, och share pricet vara konstant, så detta gör ingen skillnad heller.
- högre utdelning nu, lägre sen

allt detta är MM dividend irrelevance: In perfect capital markets, holding fixed the investment policy of a firm, the firms choice of dividend policy is irrelevant and does not affect the initial share price
- dividend policy påverkar alltså inte, men att *överhuvudtaget ha divident* påverkar share price
- i perferct capital market endast free cash flow (som kan leda t dividend/payout) påverkar firm value

se [[tax disadvantage of dividends]]

# distributions to shareholders.md
#FinKap17
med [[discounted free cash flow model|free cash flows]] kan firman antingen:
- Retain
	- Invest in projects
	- increase cash reserves
- Pay Out
	- repurchase shares
	- pay dividends

## dividends (s.637)
- Dividens bestäms av board på per share, 
- declaration day är när de authorizar dividens och blir obliged betala
- ex-dividend date är när köpare av stocken inte längre obliged t utdelning
- record date: registered by this date recieve dividend
- payable date: får dividenden

kan splitta stocks

om betalar dividend som paid-in capital eller liquidation of assets taxas företaget som för capital gains, annars taxas investors

## Share repurchases s.638
- använder cash för att köpa stock, håller den sedan i corporate reserves
- tre typer:
	- **Open market repurchase**
		- Announcar att de vill köpa tillbaka viss mängd över en period
		- inte obliged att köpa alla och kan göra det lite hur de vill
		- får inte manipulera priset
		- köper som på vanlig marknad
		- största delen av alla buybacks är dessa
	- **Tender offer**
		- säger att de ska köpa tillbaka under en kort period till en premium, shareholders säljer om de vill
		- dutch auction finns också, listar en mängd pris och shareholders får sälja så många shares de vill till priset de vill ha
	- **Targetted repurchase**
		- att negotiata med en party och köpa deras stock
		- kan vara bra om inte liquid marknad och party inte kan göra stor sell order utan att ändra priset mycket
		- kan också buyout party för undvika hostile takeover = *greenmail*

se [[comparasion of dividens and share repurchases]]

# dividend smoothing & signaling.md

firms ändrar sällan [[dividend]] dividend amount även om firms earnings väldigt volatila
- brukar ökas svagt
- kallas dividend smoothing
- increase way more frequently than cut

detta eftersom
- management tror investors prefererar stable utdelning med sustained growth
- vill hålla earnings som en fraction av long term earnings

kan variera sina dividends till olika nivåer genom buybacks eller issues och mändged retainad cash


### dividend signaling
- Ökad/sänkt dividend signalerar managements beliefs:
	- Om ökad tror management att man kommer kunna sustaina ökad dividen i foreseeable future
	- om minskar tror man inte earnings kommer rebounda och man tänker måste spara cash

# payout vs retention of cash.md
#FinKap17
hur ska man fördela earning?
- i perfect capital market ska man göra alla positive NPV investments och sedan är man indifferent för att hålla kvar cash eller betala ut den
- med imperfections får vi att cash kan reduce cost of raising capital in future eller kan också increase taxes and agency costs

irrelevant vad som gör efter +NPV investments eftersom att investors kan göra samma sak som firman med payed out cash
- MM payout irrelevance: Att investera excess cash flows i securities är ekvivalent med betala ut det direkt

## Taxes and Cash retention
- eftersom cash är negative leverage, och leverage har tax benefit, har cash tax disadvantage
- Måste betala skatt på interest vi får. Om investors behöver betala mindre skatt vill de ha pengar direkt så de kan investera själva

om retainar, måste företaget betala dividend tax och corporate tax
om betalar ut direkt måste bara betala dividend tax, och investors får en refund (? s.656 #clarifyKvaff)
- se formelsr s. 656-657
- pga double taxing är det för average investor bättre med instant payout (se s.657)

fördelar med att ändå hålla/accumulata cash:
- Om inte tror kommer tjäna lagom i framtiden för att funda +NPV projects
- Om vill undvika transaction costs av att raisa equity eller debt (se ex [[assymetric information and capital structure]])
- om har volatila earnings kan cash minska risken för financial distres

måste balansera dessa advantages/disadvantages av retaining

agency av retaining:
- om mycket cash finns finns risk att managers gör negative npv pet projects, köper excessive luxuries etc
- om har mycket debt kan equity holders villja att earnings betalas ut, se [[agency costs of levarege]]

sammantaget bör anledningarna att retaina earnings vara samma som för att ha lite leverage: undvika financial distress, vilja kunna göra investment opportuniyies
- måste vägas mot dess tax disadvantages för att hitta rätt nivå
- enligt management entrenchemnt theory kan managers interest variera från shareholders, och de kommer bara betala ut när pressured av shareholders

Dividend signaling
- Managers vill ha steadily increasing dividends för att folk ska tro på ökande vinst (? s.661)
- om managers ökar eller sänker dividends signalerar om de tror earnings kommer öka eller minska (ex sänker om tror kommer vara short on cash pga låga earnings nästa år)
- dividend signaling svagare än leverage signaling eftersom det är sämre att inte kunna betala debt än att sänka dividends
	- Ökning i dividend kan också visa att man inte tror att man har så många profitable investments, och tvärtom
- share purchases är lite mindre av en signal eftersom de inte händer lika snabbt och inte måste dela ut full amount
- 

# tax disadvantage of dividends.md
#FinKap17
capital gains tax betalas om säljer stock
dividend tax betalas på dividend

om det man betalar i capital gains tax genom att göra homemade dividend vid rebuy är högre än dividend skatten föredrar investors dividend
- om tax rates är samma är repurchase bättre för long term investors eftersom skatt delayed till de säljer

För issua equity för att ge högre dividend:
- Om dividend taxad mer än capital gains får investerare ut mindre än de stoppa in #clarifyFin s.645

## Optimal dividend polict with taxes
- Om capital gains tax lägre preferar share repurchase, optimalt med *inga dividends*

firmor använder fortfarande dividens trotts detta, kallas *dividend puzzle*
-

# The WACC Method.md
#FinKap18
en metod för att valua projekt med leverage

cost of capital för debt blir mindre pga tax shield, så använd after-tax wacc för att värdera projekt om firman har leverage
- använd net debt (subtrahera cash)

discounta sedan alla cash flows till detta

sätt upp alla cash flows i en spreadsheet (kom ihåg add back depreciation, ta bort capex och delta NWC) och discounta sedan

om man vill maintaina konstant debt-equity ratio kan man antingen minska cash eller lägga till debt för att göra projektet
- matcha andelen man redan har

kan räkna ut debt capacity $D_t$ at date t:
- Amount of debt required to keep debt-equity ratio constant
- $D_t = d \cdot V_t^L$ där $V_t^L$ är continuation value vid date t

# apv with other leverage policies.md
#FinKap18
ominte antar konstant D/E kommer WACC över tid ändras och då blir [[The WACC Method]] och [[the FTE method]] jobbiga implementera
- APV dock enkel

om håller interest payments till en konstant ratio till FCF har de en *constant interest coverage* ratio
- $k = \text{interest paid in year t}/FCF_t = \text{Konst.}$
- eftersom tax shields värde då beror på projektets outcome har den samma risk som projektet, och unlevered cost of capital bör användas
- men då blir PV(interest tax shield) propotionerlig mot PV(unlevered projektet) (se s.698)
	- $\implies V^L = (1+\tau_c k) V^U$

Om FCF ökar m konstant rate är konstant D/E equiv med konstant interest coverage ratio

## Predetermined debt leves
om vet exakt hur mycket debt vi kommer ha och det inte beror på outcome av projektet
då är tax shield mer konsekvent och mindre riskfylld så debt levels bör vara lägre än projektet
- risken liknar debts risk, så använder debt cost of capital för dessa
- om har konstant debt: $V^L = V^U + \tau_C \cdot D$
- #clarifyFin var något på s.700 om att predetermined debt gör att man inte kan använda några andra ekvationer?

WACC enklast om D/E konstant, annars APV enklast, FTE ganska komplicerad

# other effects of financing on projects.md
#FinKap18 
transaction/issuance costs: ex för lånen, osv
- dessa bör inkluderas i investeringen och i projektets NPV

Security mispricing
- Om managers tror att securities är over/under priced och de ska issua nya så kommer detta vara en desiscion som påverkar NPV för present shareholders, ta med denna i NPV för projektet
- om har felaktig credit rating och får interest rates som inte motsvarar firmans faktiska risk måste man ta detta into account (se s.702)

agency och financial distress costs (expected) måste accountas för
- kan antingen lägga till de till project cash flows eller enskillt beräkna de och lägga till till värdet sen

# project based costs of capital.md
#FinKap18
måste beräkna egen CC för projektet om risken av det differar från firmen overall - vanligt om ex har många divisioner

om ska estimata unlevered cost of capital får man beräkna pre tax WACC för comparable single division firms som gör samma sak som projektet, sen averaga ihop dem (om dessa firmor har constant target leverage level (? s.694))

om firman vill ha annan debt equity ratio för projektet får man rearanga pre-tax WACC-ekvationen och stoppa in denna där, samt den beräknade unlevered CC för projektet för att beräkna equity CC för projektet 
- när har fått $r_E$ beräknar man WACC med den och använder denna
- finns formel s.695

måste också veta hur mycket extra debt vi ska ta från projektet för att beräkna WACC
- *incremental financing*
- måste inte vara samma financing ratio för nytt projekt som för hela firman
	- om använder en annan proportion debt får ändra på debt något annat ställe i firman
	- men appropriate debt amount blir fortfarande samma

cash är ekvivalent med negativ debt

om har fixed payout policy kommer projektet vara 100% debt financed eftersom 100% av created cash flows går till ren cash som reducar debt eller till att betala tillbaka debt

eftersom agency costs, costs associated med financial distress inte beror på enbart projektet kommer optimal nivå av debt för projekten vara annorlunda fölr olika firmor

safe cash flows kan discountas helt: kan financa 100% med debt och leava overall risk unchanged, så kan discounta med raten $r_D(1-\tau_C)$

# the APV method.md
#FinKap18
adjusted present value method

beräkna först unlevered value och sedan lägg till PV av tax shield
$$V^L = APV = V^U + PV(\text{Interest tax shield})$$

använd pre tax wacc som cost of capital
- detta är unlevered CC eftersom det representerar risken av att hålla hela firman, därmed firmans själva risk
- Assumar att overall risk independent av choice av leverage

för valua tax shield:
- interest paid in year $t = r_D * D_{t-1}$
- vilken CC för interest tax shield?
	- Om går bra för projekt kan ta mer debt och ha större shield, om sämre måste ha mindre debt och mindre shield
	- $\implies$ samma risk och CC som projektet självt och *unlevered* CC ***bör användas för denna***
		- iallafall om har konstant debt to equity nivå (? s.687)
- 

# the FTE method.md
#FinKap18
flow to equity method för valuera projekt

denna calculatar alla payments till och från debt holders och därefter cash flows remainnig to equity holders
getr samma resultat som [[the APV method]] och the [[The WACC Method]]

börja med att räkna ut net cash flow to equity (subtrahera o addera cash flows eller betalningar till/från debt holders (intereset osv))
- ex increasing cash eller repaying principal minskar debt, ta med dessa (är i net borrowing)
- Net borrowing kommer bero på debt capacities: $D_t - D_{t-1}$ (s.691)

kan också beräkna FCF först och sen FCFE genom att subtrahera $(1-\tau_c) \cdot (\text{interest payments})$ och lägga till $\text{Net Borrowing}$

remaning cash flows should be discounted at equity cost of capital

eftersom vi måste beräkna debt capacity i denna och i [[the APV method]] kan [[The WACC Method]] ibland vara enklare att använda
- wacc och apv räknar ut enterprise value, FTE räknar ut equity eller mer transparent kring value to shareholders

# Financial Manager.md
#FinKap1
responsible tre main desciscions
- **1. Investment desicions**
	- bestämma vilka projekt som har bäst benefits/costs och således som ska göras; hitta bästa sätt att allokera ägarnas kapital
- **2. Financing Desiscions**
	- när bestämt vad ska investera i måste bestämma hur man ska finansiera: debt eller equity
- **3. Cash Management**
	- Se till att ha lagom cash att möta day to day obligations, att lack av cash inte hindrar utveckling/success
	- = *Managing working capital*o

# Ownership versus control of corporations.md
#FinKap1
inte handy att alla många ägare är med i managementen av företaget
- har ist board of directors och CEO som har kontroll
- **Corporate management team**
	- ultimate desiscion making authority, framröstas av shareholders
	- en share = en vote
	- board bestämmer policy, monitors performance, etc
	- CEO ska utföra the will av board
	- [[Financial Manager]] (kan vara ex CFO som rapporterar till CEO ofta) 

# four types of firms.md
#FinKap1
### Sole propreitorships
- En ända ägare som äger och runnar
- flest till antalet men står för liten del av revenue i ekonomin
- **properties**:
	- Lätta sätta upp, många nya businesses blir detta
	- Ingen separation firman ägaren; *endast* ägaren får äga
	- Unlimited libaility för ägaren, återbetalningsskyldig/personlig konkurs
	- svårt transferra ownership
- brukar konvertera till annan typ snabbt, många disadvantages

### Partnerships
- som sole proprietorship, men flera ägare som alla är liable för debt
- sluatar om någon lämnar eller dör, men likvidation kan undvikas om ex alternativ för buyout finns i avtalet
- vanliga i busniess där reputation viktigt; många law firms partnerships
- *limited partnership:* finns *general partners* (vanliga), och *limited partners*, deras liability limited till deras investment
	- limited partner death/withdrawal dissolvar inte 
	- för limited partner ägarskap transferable
	- limited får inte vara med i management
- limited partnership vanligt i pe och venture capital

### Limited liability companies
- som partnership, men bara limited partners, inga general, och de får vara med i running av businessen

### Corporations
- legal entity/artificial being
- separat från ägare, själv liabale/ respoonsible
	- ägare ej liable
- **Ägarskap**:
	- Små delar av ownersship = stock
	- All stock = equity of the corporation
	- Vem som helst får äga stock => fördel med corporations är lätt kan raisa kapital
- **Tax implications**
	- Företaget betalar skatt på vinst och sedan ägarna betalar individuell skatt, double taxation
	- *S-corporation*: Ägarna får vinst utbetald direkt och måste betala inkomstskatt på den, men inget mer
- se [[Ownership versus control of corporations]]

## Goals of firms
- ofta för corporations vill alla owners att värdet på shares ska öka

# incentives within corporations.md
#FinKap1
[[agency theory|Agency problem]] - att managers sätter sina egna behov framför shareholders även fast de är hired av shareholders
- vissa menar att separation av ägarskap och management kan minska incentive
- vissa tycker åtgärda detta genom att knyta prestanda till shareholder value
	- Kan dock göra att man tar för mycket risk, inga managers vill ha jobbet
- finns andra stakeholders än bara shareholders och managers som managers kan ta hänsyn till: ex employees
	- alla kan dock tjäna på det, ex bra publicitet etc
		- finns också corporate charity: handlingar som gör att shareholder value minskar

# stock market.md
#FinKap1 
handlar shares i publicly traded companies

om liquid kan man snabbt sälja stock för pris nära den man köpte för
- attraktivt, flexibilitet angående investeringar

primary vs seconsary stock market:
- när företag issuar shares till ägaren första gången: primary stock market
- När tradar publicly mellan investors: secondary ( <- majoritet av trading här )

bid price: pris vill köpa för
ask price: pris vill sälja för
på elektronisk stock market: postar limit order att sälja/köpa fixed amount at a fixed amount
limit orders are givers of liquidity, market orders (att köpa eller sälja direkt till bästa priset ) är takers of liquidity
- risken för limit orders är att priser rör sig
- high frequency trading för att påverka detta

dark pool: ser iinte limit order books

# IPO puzzles.md
#FinKap23
**Underpricing**
- Shares säljs ofta till lägre pris än de publicly tradar för slutet av första dan
- original shareholders tar kostnaden för detta eftersom de hade kunnat sälja equity för mer i slutet av första dagen
- är också inte en superbra opportunity att participata i IPOs bara för att de ofta är undervalued
	- Detta eftersom att man bara får igenom hela sin offer när stock är underpriced och färre vill köpa, kan inte göra lika stor investment när den visar sig vara profitable
	- måste underprica för att underinformed investors ska vara villiga att participate??? (s.888)

**Cycliacality**
- Vairer starkt hur många IPOs som görs
- beror på viss del till att behovet av kapital för att växa ändras, beror ex på ekonomin
- dock finns det ingen förklaring till den stora magnituden av svängnignarna

**COST OF IPO**
- är dyra, både i spread och extra costs
- ändå inte extra lucrative, men folk ändå insensetive till denna kostnad
- en möjlig förklaring är att låga fees singlarerar låg kvalitée

**Underperformance**
- Många firms presterar sämre än index efter IPO har gjorts
- Dock försvinner effekten när jämförs med liknande firmor, så kan bero på typen av firmor som gör IPO



# seasoned equity offering.md
#FinKap23
Att issua ny equity
När man behöver capital för growth men inte har lagom retained earnings eller vill göra IPO

följer många samma steg som IPO, men marknadspris finns redan så ingen värdering måste göras

kan vara primary eller secondary shares som säljs - nyskapade eller sådana från existing investors

cash offer och rights offer finns: om alla får köpa eller bara existing shareholders
- rights offer skyddar existing shareholders från underpricing, eftersom om nya shares säljs till lägre än market price får endast existing shareholders windfallet av detta, om det hade varit bara nya owners hade exklusivt de fått benefitten (se s.893)

**Price reaction of SEO**
- Eftersom managers som bryr sig om equity holders bara vill sälja aktier om de nuvarande aktierna är korrekt eller övervärderade så kommer aktieägare inferra att aktierna är övervärderade, och priset sjunker. Se [[assymetric information and capital structure]]?
	- Kan dock mitigatas genom enbart göra rights offer (puzzle varöfr inte fler gör det)
- Något om growth options? (s.895)

Issuance costs ofta lägre än för IPOs (s.895)

# sources of funding.md
#FinKap23
privat familj etc nästan aldrig lagom mycket kapital för att sustaina growth -> behöver outside funding
- Måste avväga hur kontrol av företaget påverkas av detta

sources:
- Angel investors - vanligast i början
	- Investerare som hjälper nya företag i början
	- vavnligare nu för tiden - fler angel investors, angel groups, och billigare att starta busniess
	- investetrar ofta i speciell security som låter de köpa stock senare till discountat pris (convertible note eller SAFE=SImply agreement for future equity)
- venture capital
	- limited partnerships som ger större funding senare i livscukeln
	- investerar i många firms så partners får diversification
	- general partners brukar ta stor fee, ofta 20-30% carried interests (profits of the fund)
	- ofta kontrollerar venture capitalists stor del i firman och vill ha mycket inflytande, grundarna ser det som nödvändigt
	- se [[venture capital investing]]
- Private equity finns också
	- Investerar i större firms, men handlar mest privately held companies
	- Gör ibland LBO: köp existerande equity i publicly traded company (användande debt & equity)
	- samma fördelar som venture capital
- institutional investors
	- pension funds, stora corporations, mutual funds
	- investerar i många saker, exempelvis i venture capital, kanske genom att bli limited partners
- corporate investors
	- Ungefär som corporations som har egen venture-capital del
	- Får också ofta strategisk fördel av att köpa visst företag





# venture capital investing.md
#FinKap23
ofta när tar in equity i företag förstå gången får man preffered stock eller convertible (kan göras om till common)
- ofta preferential dividend, liquidation och voting rights
- dock inte ofta dividends

när raisar capital kallas *funding round*

value av alla shares innan nya läggs till efter funding kallas pre-money valuation
value av alla shares efter kallas post-money valuation (s.873)
- Post-money valueation = pre-money valuation + amount invested
- percentage ownership = amount invester/post-money valuation

## Venture capital financing terms
- Om går bra kommer ofta converta prefered stock till common stock, så alla investestors treated equally
- annars finns det preferences för preffered stock:
	- Liquidation preference: minimum amount betalda till dessa innan common stock holders
	- seniority??? s.874
	- Participation right: att man demandar att även utan att converta få samma payments som common shareholders osv
	- Anti-dilution protection: Om raisar nytt capital till lägre pris per share än innan så får gamla investors konvertera sina prefered stock till fler common stock, vilket skyddar dem mot dilution, men är tufft för original owners (s.875)
	-board membership: kan villja negotiata medlemskap in the board

## Exiting an investment in a private company
de som ger funding behöver sätt att profita/cash out sin investment från private company (kan inte bara sälja aktierna)
- vanligt att företagen blir uppköpta i M&A av large companies
- kan också göra *IPO*

## IPO
- fördel att liquidity högre (PE investors får möjlighet att diversifya)
- Får även större access till capital
- att kan diversifya kan även vara en nackdel: investors blir mer widespread och kan inte monitora företaget lika bra, kan vilja discounta priset av aktierna för att reflektera detta

Använder en underwriter (investment banking firm) som bestämmer structure av ipon
- first offering: Säljer nya aktier för första gången
- secondary offering: Gamla ägare säljer sina aktier som en exit strategy

Finns även best efforts IPO: försöker sälja till så bra pris som möjligt, men inga garantier att aktierna blir sålda
också firm commitment ipo: att underwritern lovar att sälja alla aktier till ett visst pris och betalar ett något lägre pris till firman
- mer risk för underwritern
Finns också online auction-based IPOs

## IPO mechanisms
- Finns main underwriter och syndicate, som är investment banking firms under den stora underwritern som också participatar
- företaget måste registras också
- måste jobba med underwritern för att valuera företaget
	- Använder exmpelvis [[discounted free cash flow model]] eller [[method of comparabels]], om dessa differar mycket baserar de fta värderingen på tidigare liknande IPOs
- sen road-show, underwriters och managers reser runt och förklarar rationale för värderingen/priset
- Customers berättar hur mycket de vill köpa (non binding men violatar trust att inte följa genom)
- sen bestämmer underwriters maximala möjliga priset baserat på demand
- om underwriters får procentandel av aktiepriset kallas det underwriting spread
- kan göra en greenshoe provision: att underwriters får issua mer equity och sälja för att skydda sig själva från en loss (fatta inte helt, s.885 #clarifyFin )
- underwriters brukar make a market för sharen efter den blir publicly traded, för ensure liquidity: ex assigna analyst osv

Se [[IPO puzzles]]


# bond covenants.md
#FinKap24
ska minska risken att bond issuers gör saker som minskar möjligheten för de att betala tillbaka, se [[agency costs of levarege]]
- ex inte ge excessive dividend, ta mer debt,
- om bryter covenants går bonds direkt in i default
- eftersom covenants minskar risk minskar de cost of debt och kostnaden att låna. detta och minskat agency problem kan väga ut minskd flexibility och vara positivt för firman



# corporate debt.md
#FinKap24
**public debt**
- En typ av debt där företaget issuar bonds
- stor del av financing av företagen
- behöver en prospectus som beskriver denna, ska innehålla indenture som beskriver relationen debtholders och företaget

om bonds säljs till discount kallas de *original issue discount bonds*

finns bearer och registered bonds
- Registered hålls koll på vilka som äger, de får coupon payments
- bearer är den som *fysiskt* äger som får payment

## Fyra typer debt:
- Notes
- debentures
- mortgage bonds
- asset-backed bonds

notes och debentures har inte företräde före andra debtholders vid bankruptcy; unsecured debt.
notes kortare maturiry än debentures

mortgage bonds och asset-backed bonds är secured debt
dessa har tillträde till property om mortgage bonds eller andra assets om asset bonds när bankruptcy händer
finns i bland olika tranches av debt (s.907)
Seniority viktigt för debt: måste vara tydligt vilken prioritet till aseets vid bankruptcy securitiesarna har. Ofta har nya lägre
- ny debenture med lägre priority kallas subordinated debenture



bonds olika kategorier beroende på kategorin av dem:
- domestic bonds
- foreign bonds (säljs av foreign company i local market)
- Eurobonds: bonds som är international men inte denominated i valutan av origin country (? s.908)
- Global bonds kombinerar alla dessa feautures; flera marknader samtidigt

### Private debt
debt som inte är public traded; sådan man tar ut från banker
- advantage inga registration costs men mindre liquid än public debt
- **två segments**: 
	- Term loans
		- debt som har bestämd tidsperiod
		- kan hållas av syndicate med en main member som negotiatar
	- private placements
		- Är private debt not publicly traded: offered till mindre grupp investerare
		- behöver inte registreras, lägre kostnad
		- simple notes funkar
		- kan tailoras till requirements
		- 

# other types of debt.md
#FinKap24
## Sovereign debt
- är debt länder issuar
- treasury bonds
- stor marknad
- gör att kan spendera mer än tax revenue

finns *treasury inflation-protected securities*
- outstanding principal justeras för inflation. Coupon rate konstant med dollar amount varierar.

sälja antingen i competetive eller non competetive auctions
- i competetive specefierar man amount och yield man vill köpa till, säljer upp till viss yield nivå (stop-out yield) s.910
- noncompetetive får alla köpa till ett och samma pris

## Muniplicial bonds
- som soverigin debt men issuas av en state eller local government
- behöver ofta inte betala federal tax på de, ibland inte state eller local tax heller (tax-exempt bonds)
- ibland flera maturity dates = flera payouts (*serial bonds*) s.911
olika typer baserat på source of funds som ska återbetala debten 
- revenue bonds: betala tillbaka med revenue från funded projekt
- backed by full faith and credit of local government = general obligation bonds
- muniplicial bonds ändå mer riskt än sovereign debt

## asset backed securities
- en security backed av en portfolio av andra securities/assets
- exempelvis mortage backed securities (cash flows för securities mirror cash flows för mortgages)
	- government insurar ofta mot risk
	- finns dock fortfarande risk att mortgage holders betalar tillbaka tidigt och att de inte betalar lika mycket interest - prepayment risk
- även private companies kan göra detta
- kan repackaga flera gånger -> CDO:s (collaateralized debt obligations), ofta olika tranches med olika risk



# repayment provisions.md
#FinKap24
kan repaya genom
- betala tillbaka coupons och face value som specefied
- göra en partial eller tender (allt) offer för outstanding debt/bonds och köpa tillbaka s.915
- eller call provision, att det finns en clause i bonds som låter issuer köpa tillbaka för set price en set date
- det är bra att calla om market yield har sjunkit, för då kommer bonds trada till en premium, och om call är satt till face value blir det billigare att calla och refinanca direkt. tvärtom om market yield ökar
	- eftersom detta blir mer risky för investors kommer callable bonds bli billigare och ha högre returns (s.916)
	- call options kommer också alltid vara billigare än non callable options eftersom investors anticipatar calls (s.917)
	- beräknar fortfarande yeild som discount rate som gör att current price = NPV av alla payouts
		- Eftersom callable options riskier blir de billigare och därför yield högre
		- Yield to call är samma fast calculated för första möjliga call date

Kan också repaya genom *sinking funds*
- är en fund som firman gör regular payments till, en trustee använder för att köpa tillbaka bonds
- Om bonds tradar till discount köper de tillbaka från marknaden, annars köper de tillbaka at par med lotteri (? s.919 #clarifyFin )
- ofta måste göra mer payments en detta, en stor sådan payment kallas en Balloon payment

kan också repaya med *convertible bonds*
- = bonds som debtholders kan konvertera till stock
- är som call option för debt holders
- har en ratio: hur många stocks per bond man får
	- om detta gånger share price är mer än face value bör man konvertera
	- aldrig optimalt att calla innan maturity (? s.920)
- finns också bonds som är convertible och callable
	- genom att firman callar måste debtholders converta vilket kan transfera remaingin time value från bondholders tilll shareholders (s.921)
		- shareholders kan behöva sälja till lägre än marknadspris
		- så cost of debt för bonds som är convertible blir lägre (mindre risky för debt holders)??? (s.921)

# compenstation policies.md
#FinKap29
vanligt att aligna incentives genom att tya compensation till performance

## Stock and options
- får ibland stock eller options så att de blir drivna att försöka få upp share price
- men ger mer risk till managers, får ge en lagom mängd som matchar deras risk aversion

## Pay and performance sensitivity
- stock options kan därmeot göra att managers vill manipulera stock, ex genom releasa bad news innan får options eller good new efter
- finns också *backdating* som är att man retroactively väljer en date of grant där priset var lågt (ibland illegal)



# corporate governance and agency costs.md
#FinKap29
eftersom corporations har separation av control och ownership behöver managers inte vara substaintial ägare - kan ge upphov t agency problems
- att aligna deras motives ökar risken för managers - en nackdel

corporate governance system ska mitigata conflict of interest mellan mangers och owners utan burdena managers
- ex ge stock ownership eller threaten med att bli fired

## Monitoring by the board of directors and other
monitoring är kostsamt, och om equity utspritt kommer ingen ensam förmodligen få så stora gains av detat
- därför har man board of directors, men de har inte heller något större incentive att göra detta
- -> finns reasonable nivåer av debt
- Så board of directors hirar och firar executives, godkänner större investeringar osv

### Types of directors
- Finns inside, grey och outside directors
	- Hur kopplade till firman eller personer i firman man är
	- Exempelvis inside om man är employee
- outside är mest likely agera independent in favor of shareholders

firm performance finns inget bevis är kopllat till independence of board 

board är *captured* änär deras monitoring duties compromisas till följd av koppling/lojalitet till managementen
finns acts och liknande som kräver independence av boards

smaller boards presterar ofta bättre, små grupper tar bättre desiscions

finns andra personer som monitorar: analysts, employees, lenders,
- analysts granskar ofta statements och ställer CEOs svåra frågor osv
- lenders har kovenanter osv för att öka sannolikheten att de kan bli återbetalda
	- Lenders har inte alltid samma incentive som shareholders: vill ofta minska risk ibland till expense av positive NPV projects
- Employers kan detecta fraud pga inside information
	- Kanske inte alltid vill reporta t.v. kan profita från fraud eller fears retribution from whistle blowing



# managing agency conflicts.md
#FinKap29
kan göra conjecture att managers med ownership göra färre value decresing choices
däremot om managers äger mer stock blir de svårare att fira vilket minskar potency av hot om firing

shareholder action
- shareholders kan electa att göra saker vid anual meetings, ex fira board
- shareholders måste också approva saker, ex major actions som acquisitions etc
- proxy contests: när man försöker electa helt ny board
- activist funds: köpa stor del i företag de tycker är undervalued och försöka tillsätta managers som fixar de, ofta succesful

## Management entrenchment
- Sätt att bli entrenched: Antitakeover statues, poison pills, staggered boards, restriction of shareholder action
- Firms med mindre restrictions på shareholder power performade bättre

## takeover
- Om ownership, compensation, board monitoring, och shareholder activism funkar kan de göra takeovers
- Ofta firas bad performing ceos oftare i active takeover markets

överlag är bästa corporate governance strukturen en tradeoff mellan benefits och nackdelar av compensation och entrenchment, och påverkas ex av vilken kultur man är i eller vilken firma

# Balance sheet.md
#FinKap1
alla assets och liabilities
equity på liability-sidan
- Stockholders equity är ett mått på net worth av firman
- högra sidan visar hur kapital raisas, vänstra hur det används

## Assets
Indelade i long och current term:
- *Current assets*:
	- kan bli konverterade till cash inom ett år
	- cash, marketable securities (likvida)
	- accounts receivable
	- inventory, WIP
	- Annat, ex insurance paid in advande
- *Long term assets*:
	- property, plant, equipment
	- producerar i mer än ett år
	- Värdet på dessa minskar över tid, gör avskrivningar (depreciation expense)
		- accumulated depreciation är totalen av detta
	- $book \ value = acquisition \ cost - accumulated \ depreciation$
	- goodwill/intangible assets blir om man köper för mer än bokvärde
		- Minskning som depreciation av dessa = amortization eller impairment charge

## Liabilities
Indelade i long och current term:
- *Current liabilities*:
	- sarisfied inom ett år
	- accounts payable, leverantörsskulder?
	- short-term debt, inkluderar också long term debt som kommer betalas inom ett år
	- taxes/salaries som inte har betalats än
	- deffered/unearned revenue; ex om man inte levererat proukter man sålt än
	- *current assets - current liabilites = net working capital*
		- cash avaliable in short term to run business
- *Long term liabilities*:
	- Long term debt, ex för inskaffa kapital långsiktigt
	- Capital leases; måste göra regular payments länge för att använda en asset
	- Defferred taxes: owed but not yet paid, kan uppstå om man har två sets av financial statements
- [[Stockholders equity]] är också på skuldsidan

# Income statement.md
#FinKap2
revenues och expenses över period of time
- bottom line är net income

visar flows av revenues och expenses som assets i [[Balance sheet]] genererar

har olika lines:
- **Gross profit**
	- revenues from sales - costs incurrade direkt för detta, ex material, manufacturing
	- *Summeras till gross profit*
- **Operating expenses**
	- kostnader för att runna business, tex administrativa, overhead, salaries, rnd, 
	- depreciation and amortization, inte cash expense, inkluderad här
	- *summeras till operating income*
- **Earnings before interest and taxes (ebit)**
	- saker som inte har direkt med business att göra
	- ex inkomst från finansiell inkomst hamnar här
	- *summeras till EBIT*
- **Pretax and net income**
	- deducta intereset från outstanding debt, och sedan ta bort företagsskatt
	- får då Net income
		- Ofta representerat på per-share basis
		- om issuar stock options eller liknande kan detta bli diluted

# Other financial statement information.md
#FinKap2
- Management discussion and analysis
	- Diskutera managementen, ge bakgrund, signifikant events
	- disclose off-balance sheet transactions
- Notes to the financial statements
	- viktig tilläggsinformation, ex accoutning assumptions, stock-based kompensation av employees

# Stockholders equity.md
#FinKap2
summa av liabilities och assets i [[Balance sheet]]
- kallas ***book value*** of equity
- accounting measure of net worth of the firm
- är inte helt korrekt assesement av värdet
	- värdet av assets kan ha ökat eller minskat
	- värdet av ex expertis eller reputation listas inte heller
- Pga detta kan man ofta låna över book value, equity säljs för mer än book value
- ***Market value*** = shares outstanding * market price per share
	- Kallas ibland market cap
	- låg market to book ratio -> Value stocks, hög -> growth stocks

# enterprise value.md
#FinKap2
Total value of the business itself, debt och cash borträknat
- = [[Stockholders equity|Market value of Equity]] + Debt - Cash
- hur mycket det kostar att ta över business och betala av all dess skuld

# financial statement analysis.md
#FinKap2
två vanligta sätt att använda [[financial statements]] för att evaluera en firma:
- jämför med sig själv över tid
- jämför med annan firma

## Profitability ratios
- gross margin = gross profit / sales
	- förmåga sälja för mer än producerade för
- operating margini = operiting income / sales
	- tar med fler kostnader av running businies
- EBIT margin = EBIT / Sales
- Net profit margin = Net Income / Sales
	- kan variera pga differences i leverage => hur mycket interest man betalar

## Liquidity ratios
- current ratio = current assets / current liabilities
	- Hur väl man kan möta short term liquidity needs
- Short ration = samma fast bara assets som är närmare cash
- Cash ratio = Cash / Current Liabilities
	- måste ha cash för att betala employees etc, detta ger bra mått på possibility att göra detta

## Working capital ratios
för se hur efficiently man använder net working capital
- Accounts recieavable days = acccounts recievable/average daily sales
	- Hur många dagar om average man tar att collecta accounts recieable
- Accounts Payable Days = Accounts Payable / Average Daily Cost of Sales
- inventory days = inventory/average daily cost of sales
- Inventory turnover = annual cost of sales / Inventory
	- Hur många gånger per år man säljer sitt inventory (?)
	- accounts receivable turnover = (annual sales/accounts receivable)
	- accounts payable turnover = (annual cost of sales/accounts payable)
	- Högre turnover => kortare days, mer effektiv användning av working capital

Mycket stora skillnader i turnover och days mellan olika branscher, ex långsamt i wine makers men snabb i airlines

## Interest coverage ratios
- för att se om man mter intereset payment krav
- En vanlig = EBIT/interest expenses
	- high quality borrower om över 5
- Eller EBITDA eftersom DA inte är cash expenses

## Leverage ratios
Hur mycket man reliat på debt för source of fininacing
- debt-equity ratio = Total debt / Total equity
- kan använda antinignen marknads eller bokvärde
	- book value av equity kan dock vara svårtolkad eller negativ om företaget lånar mycket, så ofta bättre att ancända market value af equity
- debt to capital = total debt / total equity + total debt
- Net debt  = Total debt - Excess Cash & Short-term investments
	- Kan bättre visa hur mycket risk man tar: ex om mnan har mer cash än lån tar man ingen extra risk
- Debt to Enterprise Value Ratio = Net Debt Market / (Value of Equity + Net Debt) = Net Debt / Enterprise Value
- Equity multiplier = Total Assets / Book value of equity
	- Visar amplification av accounting returns och amplification av risk för shareholders

## Valuation Ratios
- för att se market value of the firm
- Price-earnings (P/E) = Market cap / Net income
- Leverage påverkar, så inte alltid meningsfullt att jämföra mellan företag med olika leverage
- För undvika detta kan jämföra [[enterprise value]] med Operating income, EBITDA, EBIT, etc
- Dessa inte meningsfulla om earnings negativa, kan då jämföra med sales (var försiktig!)

## Operating returns
- Return on Equity = Net Income / Book Value of Equity
	- för return on investment
- Return on Assets = (Net Income + Interest Expense) / Book Value of Assets
	- Ha med interest eftersom att lån fundade assets
	- kan vara missvisande, ex om accounts reciavable & payable ökar lika mycket minskar ROA
	- för lösa detta kan ROIC Användas:
- Return on Invested Capital = EBIT (1 - tax rate) / (Book Value of Equity + Net Debt)
	- ta bort interest expenses/income, visar bra actual performance of business
- Dupont identity för bättre förstå ROE:
- $$
ROE =
\underbrace{\left( \frac{\text{Net Income}}{\text{Sales}} \right)}_{\text{Net Profit Margin}}
\times
\underbrace{\left( \frac{\text{Sales}}{\text{Total Assets}} \right)}_{\text{Asset Turnover}}
\times
\underbrace{\left( \frac{\text{Total Assets}}{\text{Book Value of Equity}} \right)}_{\text{Equity Multiplier}}
$$
- net profit margin är lönsamhetsmått
- asset turnover är hur äl man använder assets för att få sales
- Equity multiplier blir högre med leverage



# financial statements.md
#FinKap2
Ett sätt att evaluera och jämföra success med andra firms

måste ofta fila yearly och quarterly, public corporations måste göra public och skicka till shareholders

bra sätt få information om corporation, göra descisions

måste hyra en neutral auditor som kollar financial statement reliable

finns fyra typer:
- [[Balance sheet]]
- [[Income statement]]
- [[statement of cash flow]]
- [[statement of shareholders equity]]
- [[Other financial statement information]]

# statement of cash flow.md
#FinKap2
[[Income statement]] visar profit över tidsram, men statement of cash flows visar hur mycket cash som generats
- inte samma eftersom
	- Vissa poster, ex dpreciation och amortizaation inte svarar mot cash
	- ex att köpa buildings rapporteras inte i [[Income statement]]
- använder information från [[Balance sheet]] och [[Income statement]] för att se hur mycket cash som har genererats och hur det allokerats
- ***Har tre delar:***
	- Operating activity:
		- adjusta net income genom att addera tillbaka non-cash expenses (ex depreciation, amortizaztion)
		- Sedan, justera för ändringar i net working capital: accounts recievable, accounts payable, ökningar i inventory (alla dessa är inte cash) 
	- Investment activity
		- cash krävd för att köpa ex nuy property, plant, equipment: Capital expenditures
		- subtrahera capital expenditures och andra long term investments, ex acquisitions
	- Financining activity
		- addera/subtrahera angående stocken: ex om gjort utdelninng, repurchase stock, issua stock och få pengar
		- även borrowing

# statement of shareholders equity.md
#FinKap2
- delar in [[Stockholders equity]] i det som kommer från att issua shares och från retained earnings

# Aanalyzing costs and benefits.md
#FinKap3
först identify, sen quantify
- måste quantify/evaluate in the same terms: *cash today*
	- price som vara kan säljas/köpas för i *competetive market* (= market där den kan köpas och säljas för samma pris) avgör dess värde
	- Att kan jämföra competetie market price för att avgöra värde leder till *Valuation Principle:*
		- *The value of an asset to the firm or its investors is determined by its competitive market price. The benefits and costs of a decision should be evaluated using these market prices, and when the value of the benefits exceeds the value of the costs, the decision will increase the market value of the firm.*
- Denna princip lägger grunden för desiscion making, och utvecklar [[Net present value rule]]


# Law of one price.md
#FinKap3
*If equivalent investment opportunities trade simultaneously in different competitive markets, then they must trade for the same price in all markets*

# NPV Desiscion rule.md
#FinKap3
[[time value of money]] visar hur man kan beräkna värdet på pengar över tid

om man konverterar till samma tidpunkt kan man jämföra, vanligast att konvertera till present value

## NPV
$$NPV = PV(\text{Alla benefits}) - PV(\text{Alla costs})$$
om man konverterar till cash flows får man
$$NPV = PV(\text{All project cash flows})$$

## The npv desiscion rule
*When making an investment decision, take the alternative with the highest NPV. Choosing this alternative is equivalent to receiving its NPV in cash today.*
- detta implicerar att alla projekt med positiv NPV ska göras, om man inte väljer mellan flera, då ska man ta den med högst
- kan låna för att få benefitsen idag




# arbitrage.md
#FinKap3
Att sälja och köpa mellan olika competetive markets för att få mellanskillnaden
- Brukar sällan vara då priserna möts i mitten

- Har ingen risk eller investment
- en competeteive market där inga arbitrage opportunities finns är en *normal market*
- Allt detta Detta leder till [[Law of one price]]

# security.md
#FinKap3
= en investement opporutunity som tradas i en financial market

### Valuing a secutiry with the [[Law of one price]]
- lagen säger alla equivalent opportunities borde ha samma pris
- -> Kan värdesätta en security genom att lista ut priset på en av dem
- Ex värdesätt bonds till $\frac{Utbetalning}{\underbrace{1 + r_f}_\text{risk free interest factor}}$
- Kan shorta för att göra arbitrage på bonds: *short sale*

***No-Arbitrage price*** är priset där man inte kan göra arbitrage

för att prissätta generell secturity:
- identifiera alla cash flows den kommer ge
- Beräkna present value av de cash flowsen (kostander inkluderade?)
	- Allt detta ger *No-arbitrage price of a security*
- Priset bör = $PV(\text{alla cash flows från securityn})$

Om det inte finns någon arbitrage kan man bestämma risk-free interest rate genom risk free bond prices

i normal market är NPV av att trada securities noll
- Riktigt värde och NPV skapas bara av riktiga investments/opportunities. Trading av securities justerar bara timing och risk av cash flows för att suita needs
	- Detta leder till separation principle: Att man kan serparera NPV av investment desision separat från NPV av att finansiera den (separat från security transactions), separera investment and financing

- Allt detta leder också till value addativity: En security med samma cash flows som två andra måste ha samma pris som samlingen av de
	- Leder till att firman är värd summan av alla sina projekt -> öka värde av firman genom att göra desiscions med hög NPV

# time value of money.md
#FinKap3
vanligtvis costs och profits sker vid olika tidpunkter
### The time value of money
interest rate är exchange rate för pengar i framtiden
- risk free interest rate $r_f$ är räntan till vilken man kan låna eller ge utan risk
- $(1+r_f)$ är interest rate factor, dollar om ett år per dollar idag
	- dela med denna för att få pengar om ett år idag
- $\frac{1}{1+r}$ är one year discount factor
- På detta vis kan man få present value samt beräkna [[NPV Desiscion rule]]

# valuing desiscions.md
#FinKap3
bra desiscions har högre benefits än costs
- komplext i riktiga världen, ofta andra discipliner inblandade
- **Marketing**: to forecast the increase in revenues resulting from an advertising campaign
- **Accounting**: to estimate the tax savings from a restructuring
- **Economics**: to determine the increase in demand from lowering the price of a product
- **Organizational** Behavior: to estimate the productivity gains from a change in management structure
- **Strategy**: to predict a competitor’s response to a price increase
- **Operations**: to estimate the cost savings from a plant modernization

efter tagit dessa i åtanke för kostnad måste man [[Aanalyzing costs and benefits]]



# Internal rate of return.md
#FinKap4
Räntan som gör att NPV av en investering blir 0


# timeline.md
#FinKap4
för att värdera cash flows från olika tidsperioder

- *stream of cash flows* är flera cast flows över tid

**Några regler för desision making/time travel av pengar:**
- 1. Får bara jämföra värdet transferrade till samma tidpunkt
- 2. måste *compounda* värde (multiplicera med $1+r$, interest rate) för att flytta fram pengar i tiden (blir *future value*)
	- $\text{Future Value} = C \cdot (1+r)^n$ (wow)
- 3. För slytta bak måste discounting, dividera med interest rate
	- $\text{Present Value} = C /(1+r)^n$ (wow)

## Valuing a stream of cash flows
- Discounta alla future cash flows en investering ger till present value och summera dem

### Calculating NPV
$$NPV = PV(Benefit) - PV(Costs)$$

Perpetuity: samma utbetalning varje period för alltid
$$NPV(Perpetuity)=\frac{C}{r}$$
Annuitet: samma utbetalning varje period i N år
$$NPV(Annuity)=\frac{C}{r} \cdot \left( 1 - \frac{1}{(1+r)^N} \right)$$

### Calculating future value
Skifta fram, compounda NPV av annuitet/perpituitet
- $\iff \text{multiplicera med} (1+r)^N$

så
$$FV(Annuitet) = NPV(Annuity) \cdot (1+r)^n = \frac{C}{r}((1+r)^n - 1)$$
på samma sätt
$$FV(Perpetuity) = \frac{C}{r} \cdot(1+r)^n$$

### Growing perpetuity
will att utbetalningen växer med $g$ varje period, $g < r$
$$PV(\text{Growing perpetuity}) = \frac{C}{r-g}$$

### Growing Annuity
$$PV(\text{Growing annuity})\frac{C}{r-g} \cdot \left( 1 - \left( \frac{1+g}{1+r}\right)^N \right)$$

justera till att använda interest rate för tidsperioden vi är interesserade av

kan också lösa för årlig utbetalning etc

se [[Internal rate of return]]

# Interest rates.md
#FinKap5
# Typer av interest rates

## Effective annual rate
den interest som man earnar i slutet av *ett år*

ändra power av interest rate factor för att ändra vilken tidsperiod räntan avser
$$\text{Equivalent n-Period Discount Rate} = (1 + r)^n - 1$$
Måste adjusta till samma period som cash flows för att kunna använda

## Annual percentage rate
interest rate simply earned under ett år utan compounding
"*“6% APR with monthly compounding.” In this case, you will earn 6%/12 = 0.5% every month.*"
- lägre än Effective annual rate
- kan inte använda som discount rate eftersom inte är exakt vad man tjänar
- är istället ett sätt att uttrycka att $\text{Interest Rate per Compounding Period } = \frac{APR}{ k \ \text{periods/year}}$
alltså, för att konvertera APR till EAR
$$1 + EAR = \left( 1 + APR/k \right)^k$$

outstanding balance i lån är NPV av alla remaining payments

# inflation and real versus nominal rates.md
#FinKap5
kan få real interest rate genom att att dividera growth in money med growth of prices
- $Growth in Purchasing Power = 1 + r_r = (1 + r) / (1 + i) = Growth of Money \ / \ Growth of Prices$
- $r_r$ är real interest rate
- real interest används inte som discount för future cash flows, kan endast göras om man tar bort inflation för future cash flows, vilket är bökigt

- Nominell interest rate påverkas ofta av inflation, eftersom sparare har ett mål av att få viss ökning av purchasing power



# interest rate och investment.md
#FinKap5
ökning i interest rate minskar [[NPV Desiscion rule|NPV]] om vinsterna kommer i framtiden (ofta fallet för investeringar)



# risk and taxes.md
#FinKap5
kan påverka [[Interest rates]]

- U.S treasury notes virtually risk free => lägst ränta
	- Denna rate som menas med "risk free interest rate"
- Andra borrows har riska tt defaulta. Lenders tar därför också högre interest rates
	- Dessa interest rates är *max* man kan tjäna
	- 

the right discount rate for a cash flow is the rate of return available in the market on other investments of comparable risk and term.

Income tax påverkar även vilken interest rate man får egentligen: After tax interest rate
![[Pasted image 20250830111824.png]]
fattade inte riktigt hur tax deductible loans interesst grejen funkade #FinLäsMer

Använder i framtiden *opportunity cost of capital/cost of capital* för att discounta cash flows = *the best available expected return offered in the market on an investment of comparable risk and term to the cash flow being discounted*

# yield curve and discount rates.md
#FinKap5
Ofta beror interest rate på *term*/horisont/tidsperiod av lånet/investeringen
- detta relationship kallas *term structure*
	- grapha ut det i yield curve
	- ![[Pasted image 20250830102648.png]]

- använd rätt interest rate när discountar en investment av term $N$ perioder:
	- ![[Pasted image 20250830102825.png]]
- Om beräknar NPV för många cash flows kan man behöva discounta dem till olika rates (men inte om yeild curve är platt):
	- ![[Pasted image 20250830105235.png]]

## Yield curve and the economy
- Vad bestämmer hur yield curve ser ut?
	- kortsiktigt bestämmer federal reserves vilken rate banker kan låna funds overnight till: *federal funds rate*
		- resten av alla tems rates bestämms av marknaden: ändras till supply av lending matchar demand för borrowing
	- Kan också vara interest rate expectations:
		- Om short term förväntas falla:
			- Ingen vill låna long term för att man kan låna short term, och sen refinance till lägre ränta $\implies$ long term loans får lägre ränta
		- Om short term förväntas höjas:
			- Alla vill låna long term nu för att slippa högre ränta i framtiden $\implies$ long term priserna ökar
		- slowdown i ekonomin => sjunkande interest rates => downward sloping yield curve, kan på något sätt alltså indikera future economic growth
- Hade funnits en arbitrage opportunity om yield curven inte matchade framtida priser???

# bonds.md
#FinKap6
Bond certificate dokument med amounts och dates för payments

maturity date är final payment date
time remaining är term

coupouns är periodic interest payments
- coupon rate är utbetalningen vid varje tillfälle, andel av face value

face value är det den betalar ut i slutet ofta

zero-coupon bonds tradar lägre än face value prior to maturity date
- pure discount bonds

yield to maturity är IRR av att köpa vid current price och hålla tills maturity

- Om P är pris och zero-coupon:
$$P=\frac{FV}{(1+YTM_n)^n}$$

risk free interest rate utgår från yield to maturity
- zero coupon interest rates är grund för yield curve

## Coupon bonds
treasiry notes: 1 till 10 år
treasuty bonds: > 10 år

face value och yield kan båda användas för att beskriva priset


## Dynamic behaciour of bond prices

coupon bond kan tradas till prices som är lägre - discount, högre - premium, eller samma - par, till sin face value

yield to maturity kommer vara hörgre än coupon rate om säljs för en discount

yield to maturity kommer vara lägre än coupon rate om säljs till premium

par -> samma

## Time and bonds

IRR av bond är lika med yield to maturity även om man säljer tidigt

dirty price är med accrued interest, ökar linjärt till utbetalning av coupon, sen sjunker till 0 igen i sawtooth pattern
- clean price räknar bort dessa

om interest rates sjunker blir coupon utbetalningarna mer värdefulla -> markandspriset går upp -> YTM går ner
- tjänar om man säljer
- Vice versa

zero-copoun bond YTM måste vara samma som risk free interest rate med samma term (enligt [[Law of one price]]?)
- kan bestämma pris av bond med dess YTM (eller competetive risk free interest rate) genom att discounta alla payouts till denna rate

Kan enligt [[Law of one price]] värdera coupon bonds med en samling zero-coupon bonds

upward sloping [[yield curve and discount rates|yield curve]] ger högre YTM, och vice versa (????????)

copoun paying yield curve är plot av YTM för bonds med olika maturities

# corporate bonds
finns risk för default, *credit risk*

för att beräkna NPV, använd expected value av payout
de flesta investerare vill lägga till en risk premium till cost of capital
- expected yield/return är samma som yield för expected value av NPV

yield to maturity utgår från lovad return, så blir inte alltid samma som expected return

credit ratings ratar risk of default

credit spread är skillnad i vanlig yield curve respektive yield curve för corporate bonds med olika risk

### etc
soveriegn bonds = bonds issuade av stater
- kan defaulta och prissätts därför på liknande vis som corporate bonds



# NPV and standalone projexts.md
#FinKap7
[[NPV Desiscion rule]] säger att om man har ett standalone project (minskar inte ability att göra något annat) ska man ta det om NPV av projektet överstiger NPV av att göra ingenting (0)

#fråga varför kallar man interest raten cost of capital? (s.247 fysiska boken)
- cost of capital är opportunity cost av projektet, det som shareholders kräver. Discounta alltså till den; om NPV blir negativ lever inte investeringen upp till kraven

- NPV profile är NPV plottad som funktion av cost of capital, $r$.
	- IRR ger NPV = 0
	- skillnad IRR och cost of capital är maximala estimation error i cost of capital som får finnas utan att ändra investment desiscion (blir negativ NPV om större error)


# choosing between projects.md
#FinKap7
inte alltid möjligt att göra alla projekt
[[NPV Desiscion rule]] säger att man ska rangordna alla projekt med positiv npv och ta den med högst 

[[the IRR rule]] kan inte meningsfullt applias om har olika scale of investment, timing of cash flows, riskiness, för IRRs är inte jämförbara då
- **Scale**
	- Hög IRR på låg initial investment ger inte lika mycket pengar som låg IRR på hög initial investment (500% på \$1 vs 20% på \$1M)
- **Timing**
	- Om har längre horizon kan NPV vara högre även om IRR är lägre 
- **Risk**
	- IRR inte sensetive till risk men cost of capital är det; samma IRR men olika risk ger inte lika attractive investments

## Incremental IRR
kan användas för att jämföra två projekt
Är IRR av att byta från ett projekt till det andra
subtrahera första projektet cash flows från det andra
Incremental IRR är punkten där NPV av projekten korsar/är lika i NPV profiles

Har fortfarannde problemen som [[the IRR rule]] har
- även om negativa cash flows kommer före positiva måste det inte stämma för incremental IRR, blir svårtolkad i så fall
- säger bara om ett projekt mer lönsamt än ett annat, inget om deras NPV dock
- går inte om olika costs of capital för projekten, måste då använda [[NPV Desiscion rule]]

# profitability index.md
#FinKap7
$$PI = \frac{\text{value created}}{\text{Resource consumed}} = \frac{\text{NPV}}{\text{Money invested}}$$

= bang for buck
Kan ranka alla projekt efter denna och ta de i turordning till resursen slut

### Shortcomings
för att den ska vara reliable måste
- All tillgänglig resurs tas upp
- Bara finnas en reliable resurs

# project selection with resource constraints.md
#FinKap7
hur göra om olika investments har olika resource needs (ex pengar, lokaler, etc)?

måste hitta *best set* of investments firman kan göra

se [[profitability index]]

# the IRR rule.md
#FinKap7
För standalone projects: om IRR är högre än opportunity cost of capital (för samma risk och maturity) ska man ta projektet.

pitfalls där denna inte ger samma svar som [[NPV Desiscion rule]]:
- om det kommer kostnader i framtiden för investeringen och utbetalning direkt, blir inverterat (ger motsatt rekomendation)
	- blir som att låna pengar, då vill man ha lägre IRR än cost of capital (IRR blir som interest rate här)
	- IRR fortfarande användbar för att visa margin of errir i estimated cost of capital
- Om det finns två IRR som löser NPV = 0
	- Då blir de bounds, NPV positiv om under den lägre eller över den högre (exempelvis) (kan vara tvärtom)
	- När finns flera måste vi relya på [[NPV Desiscion rule]]
- om det inte finns någon IRR
	- Måste använda [[NPV Desiscion rule]]
	- Alltid positiv eller negativ NPV


se [[the payback rule]]

# the payback rule.md
#FinKap7
för evaluata standalone projects
räkna ut hur lång tid det tar att bli tillbakabetald för dessa projekt
- om lägre än bestämd period tar man projektet
- Räkna med faktiska kassaflöden och inte NPV

## Pitfalls
- Tar inte cost of capital eller time value of money into account
- ignorerar cash flows efter tidshorisonten
- Tidshorisonten är ad hoc/godtycklig

används för att den är simpel, om investeringen är för liten för justifya ta tiden räkna ut npv




# Capital budgeting.md
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

# break-even analysis.md
#FinKap8
om osäker på input till [[Capital budgeting]] kan man beräkna break even level, är när inputsen gör att NPV = 0
kan beräkna för olika parametrar
kan beräkna break even för exempelvis EBIT istället för NPV

kan också göra ***Sensitivity analysis***
- ta best och worst case för varje parameter, kolla hur de påverkar NPV

Sensitivity analysis påverkar bara en parameter, Scenario analysiss resonerar hur en parameter ändrad kan ändra andra

# Divident discount model.md
#FinKap9
*i sammanhang valuing stocks*
Cash flows man kan få från stocks är dividends och om man väljer att sälja den i framtiden

kan inte använda vanlit discount rate eftersom finns risk, använd equity cost of capital $r_E$ som är expected return of other investments with equivalent risk

[[NPV Desiscion rule]] applyar här också

[[Law of one price]] ger att stock price $P_0$ måste uppfylla $P_0 = \frac{Div + P_1}{1 + r_E}$  
$\iff r_E = Div_1/P_0 + (P_1 - P_0)/P_0$, alltså dividend yield + capital gain rate
Total return är summan av dessa procentsatser för *ett år*, och bör vara lika med equity cost of capital

### Multiyear investors
räkna in fler dividends
kommer däremot inte valuera stock annorlunda från one year investors, eftersom att de kan sälja till andra one year investors i slutet av varje år
- Om man substituerar in expressionsen för priset i börjar i varandra blir de samma

att göra detta N gånger year Dividend-discount model
ekvationen man får håller för alla N, investerare med samma beliefs valuerar stock samma oavsett vilken tidshorisont de har

om man tror constant growth får man att $P_0 = \frac{Div_1}{r_E - g} \iff r_E = \frac{Div_1}{P_0}+g$

# discounted free cash flow model.md
#FinKap9
estimerar en hel firmas värde för både equity *och* debt holders

- börja med att beräkna [[enterprise value]]
	- = market value of quity + debt - cash
	- interpretas som kostnad att köpa busnies,, betala av all skuld och ta all cash
	- Beräknar free cash flows för alla investors, debt och equity holders:
		- Free cash flow = EBIT * (1 - tax rate) + depreciation - capex - increases working capital
		- kan substituera net investment = capex - depreciation
	- Beräkna sedan PV av dessa, blir enterprise value. Lös sedan ut ur formeln för enterprise value:
		- P0 = (V0 + cash0 - debt0) / shares outstanding
	- Kan inte använda equity cost of capital eftersom det är cost för equity investors (?) måste använda weighted average cost of capital (WACC)
		- $r_{WACC}$ är average cost of capital firma betalar till sina debt och equity holders
		- gör på exakt samma fast med denna, och lägg till en continuation/termination fee som beräknas som innan
		- 

# dividends vs investment and grotwh.md
#FinKap9
från [[Divident discount model]] får man att growth rate eller dividend ökar stock price, men ge högre dividend minskar retained earnings vilket kan minska growth, blir tradeof för firmor

Dividend payout $Div_t = \frac{\text{Earnings}_t}{\text{Shares Outstanding}_t} \times \text{Dividend Payout Rate}_t$
- så kan öka dividend  ggenom öka earnings eller fividend pahyout rate (ignorerar shares outstanding)

Kan retaina eller dela ut earnings
- Om vi antar att ökade earnings **endast kommer från reinvestment:**
- Kan anta att change in earnings = new investment  \* return on investment = earnings \* retention rate * return on investment

earnings growth rate blir change in earnings/earnings = retention rate * return on new investment 

future earnings, som används i [[Divident discount model]], beror däremot på future earnings som beror på interest payments som beror på lån som beror på managements discretion, så parametrar i modellen kan vara svår att predicta
- så finns andra modeller för att värdera stocks:
- [[total payout model]]

# information in stock prices.md
#FinKap9
folk värderar stocks olika
- att handel sker implicerar detta: Att sälja eller köpa stock till samma pris kan inte båda ha positiv NPV
- The valuation triad: Share value (stock price), future cash flow, och cost of capital: kunskap om två gör att man kan uppskatta den tredje
- efficient market hypothesis: information och värderingar av investerare aggregeras på stock market tills NPV blir noll av köpa/sälja
	- gäller väl för easily avaliable information
	- långsammare om färre vet eller svvårt att interpreta
	- positive npv trades måsta vara svåra att göra, annars hade de competats iväg

För corporate managers:
- fokusera öka NPV och free cash flows, som [[Capital budgeting]] säger
- cash flow bättre än accounting earnings, marknaden kommer oundviktligt reflektera cash flows
-

Efficient market hypothesis säger att liknande risk investments måste ha samma expected return
no arbitrage säger att man inte kan göra arbitrage medans efficient market hypothesis säger att NPV måste vara noll av att köpa stocks

# method of comparabels.md
#FinKap9
[[Law of one price]] säger att liknande företag med samma payout, risk, horizon kommer ha samma pris, så kan jämföra olika firmor föra att värdera dem

## Valuation multiples
Att multiplicera någon measure av scale med genomsnittlig value/measure
- vanligt med P/E
	- Ta forward P/E: använd expected future earnings, de vi interesserade av för valuation purpose
	- om antar constant dividend growth: $P/E = \frac{P_0}{EPS_1} = \frac{DIV_1/EPS_1}{r_E - g}$
- kan även använda ex Enterprise value till EBITDA eller EBIT
	- Ofta EBITDA för att capex kan variera kraftigt

## Limitations of using multiples
- företag är obviously inte lika varandra så ta detta i åtanke om anvädner denna metod; exempelvis kan en firma ha bra management, en annan bra produktion, och detta tas inte hänsyn tiill
- värderar bara firmor relativt andra, inte värdet av hela industrin. Kan leda till bubblor (ex dotcom)

## Comparasion med [[discounted free cash flow model]]
- denna är shortcut, använder vad marknaden tror istället för värdera cash flows, cost of capital,
- dock fördel att man inte måste uppskatta dessa framtida värden som kan bli felaktiga
- dcf har dock fördel att man kan ta information om profitability, cost of capital, och att future cash flows är det som skapar verkligt värde för investerare

# total payout model.md
#FinKap9
share repurchase är när företaget köper tillbaka stocks
- minskar mängden pengar för dividends men ökar divident payouts per share

I total payout model beräknar man framtida cash flows NPV för *all* equity, och delar sedan på antalet shares outstanding
- ta med kassaflöden av att köpa tillbaka shares
- och dividends

se även [[discounted free cash flow model]]

# benabou triole CSR.md
Anledningar bakom CSR-rörelse:
- (i) social responsibility is likely to be a normal good;  
- (ii) information about companies’ practices throughout the world has become much more accessible and quick to travel;
- (iii) the scope of environmental and social externalities exerted by multinationals in less developed, more laxly regulated countries is likely to have expanded in pace with globalization;
- (iv) the long-run cost of atmospheric pollution (e.g. global warming), or at least the public’s awareness of it, has risen significantly

för dessa demands sacraficar ibland företag profits för social interests
- ibland steppar in för företag som failar att göra detta


incentives för pro social action kan vara
- genuin vilja göra gott
- få bättre image
	- Få donations är dock anonyma
- self image: man vill själv tro man är bra

## Tre syner på CSR
#### Win-win
- menar att CSR kan göra firms mer profitable
	- ett sätt detta kan hända är exempelvis att managers brukar ta short term desiscions, exmepelvis pga compensation eller overemphasis/bias för short term
	- att ta kortsiktiga beslut ger dock dåliga konsekvenser i framtiden, ex om man hamnar i lawsuits
	- alltså kan att vara CSR vara gynsamt och korellera med profits
	- Handlar om long lerm management osv
	- eller strategic csr som stärker market position

#### Delegated Phinaltropy 
- eftersom stakeholders/shareholders ofta är villiga att sacrafica profits för social goals vill de att firman gör det åt dem
	- Engage in philantropy on their behalf
- en anledning bakom detta är att det ofta är lättare för företaget än för individer att vara involverade i philantropy, exempelvis angående transaction costs
- exempelvis kan företag vara bättre på philantrophy än governments
- det kan också bli att firms gör CSR saker för att kunder och stakeholders demandar det, och därmed blir de även mer profitable
- CSR och profit maximization blir consistent

#### Insider-initiated corporate philantropy
- Att prosocial behaviour görs för att the board eller management själva vill engage in philantropy
- brukar gå till charities eller causes management favourar
- brukar inte bli så att profit maximizaas
- milton friedman säger att de inte bör göra charity med andras pengar
	- finns också folk som säger annat
- managers måste vara något entrenched för att kunna göra philantrophy som inte ökar profits för shareholders

är ofta otydligt/elusive vilken syn som följs

data säger det finns weak eller ingen correlation mellan CSR och profitablility
- problem med att se detta empiriskt
	- Behöver stort dataset om förutsätter att CSR minskar rare disasters
	- värdering ökar abnormalt snabbt när folk inser CSR viktigt

Challenges for delegated philanthropy
- free riding: folk är beredda att göra lite och verka bra, men ofta ovilliga att göra alltför mycket
- Data som visar vilka föratag gör bra måste vara public
- vissa dimensioner av företag är bra medan andra är dåliga
- svårt att veta vad som är socially responsible
- se till att firms inte panderar till sina constituencies biases
- firms vill frama saker på gynsammt sätt
- 

# hong et al.md

stock market reagerar inte på climate change risks: exempelvis drought risk minskar inte food stock price så mycket som det borde
- kan vara pga inattention, eller home country equity bias
- "findings confirm regulatory worries about markets underreacting to climate risks and suggest further exploration of the value of corporate disclosure of exposure risk"

# martinson et al.md

carbon pricing minskar emmisions

menar carbon tax kan minska utsläpp, evidence dock mixed

sverige har högst carbon tax
- när introducades i 1991 hade vissa exemptions för highest emitters så inte flyr till andra jurisdictions
- så de högsta hade väldigt låg skatt, endast modestly decreased mellan 1990-2015 för large firms, men de 90% mindre firmsen hade större reductions

marginal emmision cost och emmisions är signifikant negativt korrelerade

om det är lätt/cheap för firmor att reduca carbon costs (low PACE)är elasticiteten (pric per enhet carbon emmision relativt emissions) högre än i high PACE
- företag med high PACE och låg möjlighet flytta production är 80-90% av manufacturing emissions

i firms med high abatement costs är tillgång till finansiering starkt relaterat till elasticiteten: möjlgihet att raisa kapital för att minska utsläpp och därmed tax

endast *heating emissions* från att bränna fossil fuels är det som taxas
- ca 2/3 av alla emissions

när analyserar carbon tax, justera för changes in sales så att ser att företagen inte simply passar on tax till sina kunder

emiisions har decreasat 31% 1990-2015
- dels mindre carbon intensive businesses som körs
- en del är även carbon taxen


Ser att firms med högre marginal tax får lägre emission
- tar dock nog längre tid att implementera justeringar av teknologin och strategin för att helt implementera dessa
