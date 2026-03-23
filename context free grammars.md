
definition av CFG
1. set of symbols; terminals
2. set of variables; languages or set of strings
3. Start symobl; defines the language
4. Rules that define recursive definition of a language; productions
	1. Varje har head symbol, pil, och string av zero or more terminals eller variables
5. G = (V, T, P, S)

Kallas *recursive interference* om man tar strings from language of every variable och sätter ihop de enligt reglerna för att komma till startsymbolen

Kallas *derivation* om man börjar från startsymbol och expanderar alla definitioner till man bara har en string av terminals
- använder => för att denota derivation step
- =>* med stjärna över för flera steg
- subscript med G för grammar

rightmost / leftmost byter alltid ut en av de yttersta variablerna mot en av sina production boies
![[Pasted image 20260321153806.png]]

Language of a grammar
![[Pasted image 20260321153844.png]]
- L är context free languageS


![[Pasted image 20260321154421.png]]
![[Pasted image 20260321154428.png]]


The yield av parse tree är att läsa vänster till höger på leaf nodesen
- alla yields av alla parse trees med startsymbolen som rot är language of the grammar

kanske läsa mer om hur inference implicerar trees osv