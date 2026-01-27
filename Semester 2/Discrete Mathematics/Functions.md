Let $X$ and $Y$ be sets
$f: X \rightarrow Y$ 

A function $f$ assigns each element of $X$ to exactly one element of $Y$
$X$ - domain of $f$
$Y$ - codomain of $f$

$f$ maps *every* element of $X$ to some element of $Y$
This may be every element of $Y$ or it may be a subsection of $Y$
- This subsection is the *range* or *image*

Multiple elements of $X$ can map to the same element of $Y$
Multiple elements of $Y$ cannot map to the same element of $X$

#### Surjective
Every element of $Y$ has a corresponding element of $X$
range = codomain
$f: \mathbb{R} \rightarrow \mathbb{R}, f(x)=x^2$ is not surjective
$f: \mathbb{R} \rightarrow \mathbb{R}^+, f(x)=x^2$ is surjective

#### Injective
No two distinct elements of the domain have the same image
Every element of $X$ maps to a *unique* element of $Y$
$f: \mathbb{R} \rightarrow \mathbb{R}^+, f(x)=x^2$ is not injective
- -1, 1 have the same image
$f: \mathbb{R}^+ \rightarrow \mathbb{R}^+, f(x)=x^2$ is not injective


### Composition
Given 2 functions:
$f :  A \rightarrow B$
$g :  B \rightarrow C$
their composition is
$g \circ f = g(f(x))$ 
apply right side $f$ first, then left side $g$

### Identity Function
The *identity function* on $A$ is the function $i:A \rightarrow A, i(x)=x$

$f :  A \rightarrow B$
$g :  B \rightarrow A$
if $g \circ f : A \rightarrow A$ is the identity function on $A$ and
$f \circ g : B \rightarrow B$ is the identity function on $B$ 
then $f$ is the inverse of $g$ and vice-versa

If a function has an inverse it is *invertible*

#### Bijective
Both surjective and injective is *bijective*
If and only if a function is bijective, it is *invertible*



### Exercises
![[Exercises#1.6.1]]

![[Exercises#1.6.2]]

![[Exercises#1.6.3]]

