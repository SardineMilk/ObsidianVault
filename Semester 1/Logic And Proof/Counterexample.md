#fol

To prove a sentence is (logically/universally )valid, you would have to prove infinitely many interpretations are true

To prove a sentence is not valid, a counterexample can be shown
If a single interpretation is not true, the sentence is not valid

We shall only be interested in sentences S and we want to show either $\vdash S$ or not

----
Entscheidungsproblem
"Decision problem"

A box you put in S, which outputs Yes if $\vdash S$ and No if it is not logically valid

Turing showed this problem cannot be solved in general

----
**Example** 
D = all people
F(x, y) 'x is the father of y'

A = $(\exists x)(\forall y) F(x, y)$
B = $(\forall y)(\exists x) F(x, y)$

A says when interpreted:
' There is someone who is the father of everyone' which is FALSE

B says when interpreted
'Everyone has a father'

**Example**
$X=(\exists x)[A(x) \land B(x)] \implies [(\exists x) A(x) \land (\exists x) B(x)]$

x is a sentence
structure will look like this:
(D, w, z)
$w \subset D$
$z \subset D$

A(x) -> '$x \in w$'
B(x) -> '$x \in z$'

To show that X is true in an interpretation
show that $(\exists x)[A(x) \land B(x)]$ implies $[(\exists x) A(x) \land (\exists x) B(x)]$

$(\exists x)((x \in w) \land (x \in z))$
implies
$(\exists x)(x \in w) \land (\exists x)(x \in z))$

That there is something in both w and z
this implies
There is something in w and there is something in z

