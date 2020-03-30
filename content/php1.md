+++
title = "The Pigeonhole Principle"
date = "2020-03-29"
math = true
+++
 
**The Pigeonhole Principle (or the Box Principle)** looks obvious and straightforward on first glance but it has a very widespread application. It shows itself in the most unexpected of places and the proofs involving it are striking examples of mathematical elegance. \
So what is this principle? In this post, I'll write about a version of this principle which I find more intuitive. Here you have a certain number of pigeons which you must place inside a certain number of holes. 

**Statement - 1** : If there are \\(n\\) pigeons and \\(k\\) holes, where \\(n>k\\), then one hole must have at least 2 pigeons. 

**Statement - 2** : If there are \\(n\\) pigeons and \\(k\\) holes, then one hole must have at least \\([\frac{n}{k}]+1\\) pigeons if \\(n/k\\) is not an integer, other wise the number is simply \\([\frac{n}{k}]\\) 

(Note : here \\([.]\\) implies the greatest integer function)

Statement - 1 is rather obvious but it gives rise to Statement - 2, which might also be considered 'intuitive'. However intuition has no place in mathematics. We must formally prove it. 

**Proof** 

We prove it by the method of contradiction. We assume the contrary, that is, every hole has at most \\([\frac{n}{k}]\\) pigeons. 

Now the maximum number of pigeons = \\(k[\frac{n}{k}] \leq k(\frac{n}{k}) = n\\) \
This can be recast as : maximum number of pigeons \\(\leq n\\) 

However we must have \\(n\\) pigeons. Hence the equality must be true. We can see that the equality is true only under the special condition that  \\([\frac{n}{k}] = \frac{n}{k}\\), that is, \\(n/k \in \mathbb{Z}\\).  If we assume that \\(n/k\\) is not an integer (as specified in the first case of Statement -2), we reach a contradiction. Hence our initial assumption is wrong and one hole must contain at least \\([\frac{n}{k}]+1\\) pigeons 

The second case, \\(n/k = q\\) is an integer can be solved by assuming all holes have at most \\([\frac{n}{k}] -1\\) pigeons and reaching a contradiction. This follows a similar procedure and will not shown here. 

The Pigeonhole Principle has brilliant applications in various problems which I'll discuss in upcoming posts.


