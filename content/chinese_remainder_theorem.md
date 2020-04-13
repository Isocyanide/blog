+++
title = "The Chinese Remainder Theorem"
date = "2020-04-13"
math = true
+++

This is a famous theorem in elementary number theory which is suited to answer a specific type of question whose first appearance was seen in Chinese literature, and hence the name Chinese Remainder Theorem. The question asks - "Find the positive integers which give remainders \\(a_1, a_2, a_3, a_4\\) when divided by \\(n_1, n_2, n_3, n_4\\) respectively." We first derive the mathematical tools required to tackle the problem. 

### Linear Congruences
As the name suggests, we deal with congruences such as \\(ax \equiv b \\ (mod \\ n) \\). However it's just a fancy notation for \\(ax - b = ny\\) or \\(ax -ny = b\\) where \\(y\\) is an arbitrary integer. This reduces to a linear Diophantine equation, which has solutions in the form of an arithmetic progression. \
\\(x = x_0 + \frac{n}{d}t\\) where \\(x_0\\) is any solution, \\(d = gcd(a,n)\\) and \\(t\\) is an arbitrary integer. \
We are only interested in the solutions in-congruent to \\(n\\). For example, for n = 7, if \\(x=3\\) satisfies, that is, \\(3a \equiv b \\ (mod \\ 7)\\) that implies \\(x = 10 \equiv 3 \\ (mod \\ 7)\\) also satisfies the same. The point here is that \\(x=3, 10, 17, 24\\) etc are the same solution as \\(x \equiv 3\\). Hence all the solutions can be reduced to one of the residues modulo \\(n = (0,1,2..n-1)\\). 

We argue that there are exactly \\(d = gcd(a,n)\\) in-congruent solutions. Consider, 

$$ x_0, x_0 + \frac{n}{d}, x_0 + 2\frac{n}{d}...x_0 + (d-1)\frac{n}{d} $$

If any two of them were to be congruent, we would have, 
$$    x_0 + i\frac{n}{d} \equiv x_0 + j\frac{n}{d} \\ (mod \\ n) $$
$$    i\frac{n}{d} \equiv j\frac{n}{d} \\ (mod \\ n) $$
$$    i \equiv j \\ (mod \\ n/gcd(n,\frac{n}{d})) $$
$$    i \equiv j \\ (mod \\ d) $$

We know that the last statement is impossible. Now lets consider an arbitrary solution of \\(x\\) where \\(t = qd + r\\) and \\(r<d\\). We have

$$    x_0 + \frac{n}{d}t \equiv x_0 + \frac{n}{d}(qd+r)\equiv x_0 + nq + \frac{n}{d}r $$
$$  \equiv x_0 + \frac{n}{d}r $$

Where \\(r<d\\) which is one of our selected \\(d\\) solutions. So we have proved that \\(ax \equiv b \\ (mod \\ n)\\) has \\(d = gcd(a.n)\\) mutually in-congruent solutions. 

### Chinese Remainder Theorem

Let \\(n_1, n_2...n_r\\) be positive integers that \\(gcd(n_i, n_j) = 1\\) for \\(i \neq j\\). Then the system of linear congruences : \\(x \equiv a_1 \\ (mod \\ n_1), x \equiv a_2 \\ (mod \\ n_2).....x \equiv a_r \\ (mod \\ n_r)\\) admits a simultaneous solution, unique modulo to the integer \\(n = n_1n_2...n_r\\) 

We start by assigning \\(N_i = \frac{n}{n_i} = n_1..n_{i-1}n_{i+1}..n_r\\). Since all the \\(n\\)'s are relatively prime, \\(gcd(N_k, n_k) = 1\\). By the theory of linear congruences, we know that the congruence \\(N_kx \equiv 1 \\ (mod \\ 1)\\) admits \\(d=1\\), that is, a unique solution. Let's call it \\(x_k\\). Consider the integer:

$$  N = a_1N_1x_1 + a_2N_2x_2 + ... a_rN_rx_r $$

We argue that this integer is the required solution. Indeed, \\(N_k \equiv 0 \\ (mod \\ n_i)\\) for \\(k \neq i\\) as \\(N_k\\) contains a \\(n_i\\) factor. Hence we only need to consider \\(N \equiv a_kN_kx_k \\ (mod \\ n)\\). By our selection of \\(x_k\\) we know that \\(N_kx_k \equiv 1 \\ (mod \\ 1) \implies a_kN_kx_k \equiv a_k \equiv N \\ (mod \\ n_k)\\) which was to be proved. 

All that's left is to prove that it is unique modulo \\(n_1n_2...n_r\\). Let \\(x_1\\) and \\(x_2\\) be two simultaneous solutions. 
$$ x_1 \equiv a_1 \equiv x_2 \\ (mod \\ n_1) $$
$$    .   $$
    $$. $$
$$ x_1 \equiv a_r \equiv x_2 \\ (mod \\ n_r) $$
Putting all of them together yields \\(x_1 \equiv x_2 \\ (mod \\ n_1n_2...n_r)\\). Now we have proved both the aspects of the theorem and the job is done! 

Here a problem to solve using the theorem : When eggs in a basket are removed \\(2,3,4,5,6\\) at a time there remain, respectively \\(1,2,3,4,5\\) eggs. When they are taken out \\(7\\) at a time there are none left. Find the smallest number of eggs there could have been in the basket.
