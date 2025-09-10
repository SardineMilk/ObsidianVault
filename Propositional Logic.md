#logic 

Propositional Logic (PL) is a formal language. It is composed of [[Atomic Statements]], linked together by [[Logical Connectives]] (aka Propositional Connectives) into [[Compound Statements]].

> A statement that cannot be analysed further using the propositional connectives is called an *atomic statement* or simply an *atom*. Otherwise a statement is said to be *compound*. The truth value of a compound statement can be determined once the truth values of its atoms are known by applying the truth tables of the propositional connectives.

[[Logic-book.pdf#page=19&selection=126,0,139,58|Logic-book, page 19]]


> We now define the formal language called propositional logic. This consists of a set of symbols called atomic statements or atoms [...] from which we construct well-formed formulae (wff)

[[Logic-book.pdf#page=21&selection=66,7,94,4|Logic-book, page 21]]

### Well-Formed Formulae (wff)

Statements in PL are known as Well-Formed Formulae.
Wff are defined by the following rules:

1. All atoms are wff
2. If X and Y are wff, so are all combinations of X and Y formed by [[Logical Connectives]]
3. All wff are constructed by repeating rules 1 and 2 a finite number of times

Any wff that aren't atoms are known as [[Compound Statements]]