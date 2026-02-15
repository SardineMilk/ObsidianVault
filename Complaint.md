Section 3.3 of the lecture notes for Discrete Mathematics (F17SC) explain the process for solving a linear nonhomogeneous recurrence relation.

The stated process is:
1. Find a particular solution 
2. Find the general solution for the homogeneous part
3. Combine them
4. Use the initial conditions to find the final solution

If the chosen particular solution overlaps with the homogeneous solution (duplicating a term),
it must be adjusted by multiplying by $n$ until it no longer overlaps.
I don't think this process is adequately explained in the lecture notes:
![[Pasted image 20260215191220.png]]
The notes simply state "this doesn't work for this relation, multiply it by $n$", without explaining why or how. I had to do my own research to learn this concept.

Additionally, the order of finding a particular solution and then finding the general solution of the homogeneous part mean it is impossible to know if there is a duplicated term until later in the process.
This would force you to restart the question, adjusting the particular solution.

Is there any reason why it is done in this order, and not
1.  Find the general solution for the homogeneous part
2. Find a particular solution (adjusting if needed)
3. Combine them
4. Use the initial conditions to find the final solution

Please let me know if I'm missing or misunderstanding something.

Thanks, 
Thomas Prowse

