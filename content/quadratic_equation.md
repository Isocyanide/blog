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

 $$   \alpha = d + x, \ \beta = d - x$$

For some real number \\(x\\). Since \\(d\\) is a known value, the task boils down to finding \\(x\\). On employing the second condition, our answer is a single calculation away. 

 $$   \alpha*\beta = b $$
 $$   (d+x)(d-x) = b $$
 $$  d^2 - x^2 = b $$
 $$   x^2 = d^2 - b $$
 $$   x = \sqrt{d^2 - b}$$

And just like that, we were able to find the roots of the equation without any the aid of any formulas. Let's deploy our method to observe how it works out. 

**Q) Solve \\(x^2 - 6x + 25 = 0\\)**

We first compute \\(d = -\frac{a}{2} = -(-6/2) = 3\\). Hence our roots are \\(3+ x\\) and \\(3-x\\). 

$$(3+x)(3-x) = 25$$
$$x^2 = 9 -26$$
$$x^2 = -16$$
$$x = \pm 4i$$

Hence our roots are \\(3+4i\\) and \\(3-4i\\). 

