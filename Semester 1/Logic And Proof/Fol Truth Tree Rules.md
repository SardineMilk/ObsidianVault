
Normal PL truth trees
BUT

**New-Name Rule**
You replace $(\exists x)P(x)$ with $P(a)$
where "a" is a *new* constant on the branch

**Never-Ending Rule**
You replace $(\forall x)Q(x)$ with $Q(a)$ 
where "a" is an *existing* constant on the branch

#### Negations - De Morgan's Laws

$\neg ((\exists x)P(x))$
|
$(\forall x)\neg P(x)$

$\neg ((\forall x)Q(x))$
|
$(\exists x)\neg Q(x)$

#### Examples

$\neg ((\forall x) (P(x) \land Q(x)))$
|
$(\exists x)\neg (P(x) \land Q(x))$ *use De Morgan negations*
|
$\neg (P(a) \land Q(a))$ *use new-name rule*
/                         \
$\neg P(a)$                   $\neg Q(a)$ *use PL rule*
