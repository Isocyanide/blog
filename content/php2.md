+++
title = "The Power of Pigeonhole Principle - 1"
date = "2020-03-30"
math = true
+++
 
In this post, I'll discuss a couple examples where Pigeonhole principle is employed. In case you don't know what the Pigeonhole principle is, you can read my post on it. [Here](https://isocyanide.github.io/php1/) is the link. 

### The Friendship Theorem

_Among six people, there are always three who know each other or three who are complete strangers._

How can one establish such a statement using mathematics? It almost sounds preposterous! Here we use another concept well known to us but appears to be unrelated - Geometry. Consider a hexagon where every vertex \\(A,B,C,D,E,F\\) denotes a person. Now we join all the vertices by either a red line or a blue line. Two points joined by a red line implies that the two people represented by the points are strangers while the blue line represents friends (or simply people who know each other). 

Lets start with person A. There are \\(5\\) lines leading away from A which can be either red or blue. This is where the Pigeonhole principle kicks in. Let 'red' and 'blue' be holes and the \\(5\\) lines be pigeons. Since \\(\frac{n}{k} = \frac{5}{3}\\) is not an integer, one of the holes has at least \\([\frac{n}{k}] + 1 = 3\\) lines. Without loss of generality, let the three lines be blue. 

![hexagon](/hexagon.jpg#center)

Now if any one of \\(CD\\) or \\(DE\\) or \\(CE\\) is blue, we have a blue triangle implying the existence of \\(3\\) people who know each other mutually. Otherwise if \\(CD\\), \\(DE\\) and \\(CE\\) are all red, we have a red triangle \\(CED\\) implying the existence of \\(3\\) people who are mutually strangers. The statement has been proved. 

### A Geometrical Problem

_If a disk of radius one contains seven points with mutual distance \\(\geq 1.\\) Prove that one of the points is the center of the disk._

You might be wondering - where are the holes? Well, we make our own holes! 

![circle](/circle.jpg#center)

Each one of the \\(6\\) partitions is a 'hole' while the \\(7\\) points are 'pigeons'. So one of the parition contains at least \\([\frac{7}{6}] + 1 = 2\\) points. However this is impossible. Let the two points be  \\(P\\) and \\(Q\\). Since they are inside the partition, the angle between them \\( \angle POQ < 60^{\degree}\\) and \\(OP\\) and \\(OQ \leq\\) radius \\(=1\\) (\\(O\\) being the centre of the cirlce). By the cosine rule, it is easy to verify \\(PQ < 1\\) which violates the given condition.
The only other alternative is to have one of the points as centre and indeed if we place the rest \\(6\\) points at a separation of \\(60^{\degree}\\) on the circumference, we are left with the situation described in the question. 

After a little experience, identifying questions which require the pigeonhole principle becomes quite easy. The idea of dividing a geometrical shape to accommodate the points is a powerful technique and the key to a lot of problems. 
