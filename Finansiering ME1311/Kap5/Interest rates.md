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