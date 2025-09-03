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