+++
title = "A Theorem in Number Theory"
date = "2020-03-28"
math = true
+++
 
### For positive integers \\(a,b\\) where \\(gcd(a,b) = 1\\), the equation \\(ax + by = n\\) always has a solution in positive \\(x,y\\) for all \\(n \geq ab\\) 

**Proof**

Since \\(gcd(a,b) = 1\\), by the theory of linear Diophantine equations, we know that there always exists solutions (infinitely many of them) for \\(ax + by = n\\). However we are only interested in the ones where both \\(x\\) and \\(y\\) are positive.

\\(ax + by = n\\) \
Let \\(n = ak + r\\) where \\(r<a\\) \
\\(ax + by = ak + r\\) \
Set \\(x = k - t\\) where \\(t\\) takes integral values from \\(1\\) to \\(b\\) \
\\(\implies a(k - t) + by = ak + r\\) \
\\(\implies - at + by = r\\) \
Let \\(r = 0\\) \
\\(\implies by = at\\) \
\\(\implies b|at\\) \
\\(\implies b|t\\) (since \\(gcd(a,b) = 1\\) \
\\(\therefore t_{max} = b\\) 

Now lets consider the arbitrary case. We must prove that \\(-at + by = r\\) has a solution \\(t\\) in \\([1,b]\\)
Here we employ the theory of Diophantine equations. \
All the solutions to the above equation are \\((t_0 + (b)d, y_0 + (a)d)\\) where \\((t_0, y_0)\\) is an arbitrary solution of the same equation and \\(d\\) is any integer. \
We notice that the sequence of \\(t\\)'s follow an arithmetic progression with common difference b. Hence there always exists a \\(t\\) between \\(1\\) and \\(b\\).\
The corresponding \\(y\\) is also positive as \\(by = at + r\\).

However in order for \\(x\\) to be positive, the minimum value of \\(k-t\\) must be positive. \
\\(\implies k-b\geq 0\\)\
\\(\implies k\geq b\\)

Since \\(n = ak + r\\).\
For \\(n \geq ab\\) we always have a positive solution in \\(x,y\\). 

Remark : This has been proved for all \\(n > ab-a-b\\) but this proof is rather elementary compared to that and this result is still quite powerful.    
