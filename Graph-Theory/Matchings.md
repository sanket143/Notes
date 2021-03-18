# Hall's Marriage Theorem

If there is a matching saturating k
vertices in L, how many vertices does it saturate in R?
-> k vertices

In a bipartite graph to have a perfect matching:
- |L| = |R|

For |L| < |R|,
Hall's theorem focuses on saturating L(smaller set).

#### Hall's Condition
For all X subset of L, |N(X)| >= |X|

*Theorem:* A bipartite graph (L, R) has a matching saturating
*L*, if and only if *L* satisfies Hall's condition.

Matching is maximum when there is not augmenting path.

L satisifies Hall's condition. We want to prove that there is a
matching saturating L.

*Proof by contradiction (Assume the largest matching does not
saturate L)*

Matching is maximal if and only if there no augmenting path of
length 1.

We are interested in finding a leaf at an odd level, we are
seeking saturated in odd level.
