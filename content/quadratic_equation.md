+++
title = "A Different Approach to Quadratic Equations"
date = "2020-04-20"
math = true
+++

In this post, I'll discuss a cool and innovative approach to quadratic equations. I'm sure all of you are familiar with the dreadful quadratic equation. I'm sure most of you remember it as well but of course, it's a pain in the arse. Have you ever wished there was an easier way without all the memorisation? Well, your wish has come true!

Consider a quadratic equation : 

$$    x^2 + ax + b = 0$$

Let \\(\alpha\\) and \\(\beta\\) be the roots. We know that \\(\alpha + \beta = -a\\) and \\(\alpha\*\beta = b\\) 
Now assign :

$$    d = \frac{\alpha + \beta}{2} = -\frac{a}{2}$$

\\(d\\) is the average of both of the roots and hence the roots are equidistant from this value. In other words, 

 $$   \alpha = d + k, \ \beta = d - k$$

For some real number \\(k\\). Since \\(d\\) is a known value, the task boils down to finding \\(k\\). On employing the second condition, our answer is a single calculation away. 

 $$   \alpha*\beta = b $$
 $$   (d+k)(d-k) = b $$
 $$  d^2 - k^2 = b $$
 $$   k^2 = d^2 - b $$
 $$   k = \sqrt{d^2 - b}$$

And just like that, we were able to find the roots of the equation without any the aid of any formulas. Let's deploy our method to observe how it works out. 

**Q) Solve \\(x^2 - 6x + 25 = 0\\)**

We first compute \\(d = -\frac{a}{2} = -(-6/2) = 3\\). Hence our roots are \\(3+ k\\) and \\(3-k\\). 

$$(3+k)(3-k) = 25$$
$$k^2 = 9 -26$$
$$k^2 = -16$$
$$k = \pm 4i$$

Hence our roots are \\(3+4i\\) and \\(3-4i\\). 

