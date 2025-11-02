
hur queryar / data manipulatar [[Relational model]]
- = operations i den [[data model]]

fördel med query langueage är att det inte kan göra allt = simplare att implementera och compiler kan omptimiza kod

## algebra
= consists of atomic operands and operators

### Relational algebra
- Atomic operands = 
	- Variables that stand for relations
	- constants, which are finite relations
- Operators
	- vanliga set operators
		- när applyar dessa måste två relations ha samma schema och domains och order of attributes
	- selection, tar bort tuples
	- projection, tar bort columns
	- operations that combine tuples, ex cartesian product eller speciella joins som selectively pair tuples
		- natural join: para alla tuples som agreear i alla attributes i unionen av R och S
		- Theta join: to produkten av R och S och behåll alla pairs som uppfyller någon condition C
	- renaming, ändrar inte tuples men namnen på ex attributer