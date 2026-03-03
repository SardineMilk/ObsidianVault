*Take any SOLHRR, with $A, B$ being real number constants*
$a_k = Aa_{k-1} + Ba_{k-2}$

*Assume the following:*
$a_k = t^k$
*Which would make the sequence*
$1, t, t^2, t^3, t^4, \dots$
*Substitute $t^k$ into the recurrence:*
$t^k = At^{k-1} + Bt^{k-2}$
*Look at the formula when $k=2$:*
$t^2 = At + B$
$t^2 -At - B = 0$
*This is a quadratic equation* 
*The values of $t$ that make it true can be found by factoring (or the quadratic formula if needed)*

*Now you have 2 separate values of $t$ that form sequences that satisfy the recurrence*
*How do you satisfy it for specific initial conditions?*
*Combine the 2 separate solutions after multiplying by constants*
$a_k = Ct_1^k + Dt_2^k$
*You know $t_1, t_2$ and two values of $a_k$ (initial conditions)*
*Solve for $C, D$, using simple linear equation maths*