+++
title = "A Fun Question - 1"
date = "2020-05-10"
math = true
+++

**Consider the squares of an 8 × 8 chessboard filled with the numbers 1
to 64 as in the figure below. If we choose 8 squares with the property
that there is exactly one from each row and exactly one from each
column, and add up the numbers in the chosen squares, show that the
sum obtained is always 260.**

![table](/number_table.jpg#center)

So the first thing we do is break down the columns and rows to look for patterns we can exploit. What is common in all the elements of the first column? All the numbers in the first column give a remainder of 1 on division with 8. Indeed, all the numbers in the \\(n^{th}\\) column leave a remainder of \\(n\\) when divided by 8 (Note that a remainder of 0 and 8 is synonymous). This naturally leads to the standard notation of expressing the numbers in the \\(r^{th}\\) column as \\(8k+r\\) for some integer \\(k\\). 

We cracked the columns but what about the rows? The answer is simple. Each row  merely fixes the \\(k\\) value. For example, in the first row, the value of \\(k\\) is set to \\(0\\). Similarly, the value of \\(k\\) in the \\(n^{th}\\) row is \\(n-1\\). 

Now we possess both, the meanings of the rows and columns. Only thing that remains is to bring it all together. The condition given to us is that no two numbers can share the same row or column. In other words, no two numbers have the same \\(k\\) or remainder value associated with them. 

Let the numbers selected be \\(n_1, n_2...n_8\\).
$$n_1 + n_2 ... n_8 = (8k_1 + r_1) + (8k_2 + r_2) ... (8k_8 + r_8) = 8(k_1 + k_2 ... k_8) + (r_1+r_2...r_8)$$
Since all the \\(k\\) values are unique, they are \\(0,1...7\\) in some order. Similarly all the \\(r\\) values are \\({1,2...8}\\) in some order. This fixes both their sums and the answer lies a simple computation away! 

