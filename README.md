# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

1. The probability that only choose the first element to be a good pivot is $P_{first}=\frac{(\frac{3n}{4})-(\frac{n}{4})}{n}=\frac{1}{2}=50$%

2. In the Median-of-three method, there are 3 elements, and each element will have equal chance to be median, so the probability density is $f_m(p)=6p(1-p)$, calculate the probability $P=\int_{1/4}^{3/4}6p(1-p)dp=68.75$%

   Explian for the probability density function $f_m(p)=6p(1-p)$: suppose there are elements $x_1$, $x_2$, $x_3$, and each of them have the equal chance to be the median, for example, if select $x_2$ to be the median, there are two conditions: $x_1<x_2<x_3$ and $x_3<x_2<x_1$, for the first condition supose the probability that $x_1<x_2$ is $p$, then $x_2<x_3$ is $(1-p)$, and combine them together, the probability for $x_1<x_2<x_3$ is $p(1-p)$. As for the another condition $x_3<x_2<x_1$, the probability is the same as the last one, which is $p(1-p)$. since there are 3 $x$, and each of them could have 2 conditions, so the probability density is $3\times2\times(1-p)=6p(1-p)$

Therefore, use the Median-of-three method is more likely to pick a good pivot compared to simply choose the first element to be a good pivot, becuase the probability of the Median-of-three method is 68.75%, which is greater than simply choose the first element (50%).
