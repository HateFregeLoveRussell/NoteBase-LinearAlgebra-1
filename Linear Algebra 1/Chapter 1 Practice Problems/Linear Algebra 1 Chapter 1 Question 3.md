---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q3
class: {
  class-name: "Linear Algebra 1",
  author: "Georgi E. Shilov",
  medium: "Textbook",
  class-alias: "Lin-Alg-1",
  title: "Linear Algebra",
  edition: "Dover Books on Mathematics",
  publisher: "Dover Publications",
  ISBN: "978-0-486-63518-7",
  length: 377,
  template: {
    name: "class-textbook-obj",
    version: 1,
    type: "object"
  }
}
source: {
  source-alias: "Lin-Alg-1-Ch1-PP",
  class-alias: "Lin-Alg-1",
  book-title: "Linear Algebra",
  end-page: 30,
  ISBN: "978-0-486-63518-7",
  section-name: "Chapter 1 Practice Problems",
  start-page: 28,
  type: "tbsection",
  template: {
    name: "source-tbsection-obj",
    type: "object",
    version: 1
  }
}
status: {
  state: "Completed",
  template: {
    name: "status-obj",
    version: 1,
    type: "object"
  }
}
validity:  {
  state: true,
  template: {
    name: "validity-obj",
    version: 1,
    type: "object"
  }
}
template: {name: class-textbook-practice-problem, version: 1}
---
### Problem Statement:
With what sign does the term $\large{a_{1,n}a_{2,{n-1}} \ldots a_{n,1}}$ appear in a [[Determinants#Definition(Determinants)|determinant]] of order $\large{n}$?
#### Solution:
The term $\large{a_{1,n}a_{2,{n-1}} \ldots a_{n,1}}$ appears with a negative sign in a [[Determinants#Definition(Determinants)|determinant]] of order $\large{n}$ if and only if $\large{n \operatorname{mod} 4 \ne 0}$ and $\large{n \operatorname{mod} 4 \ne 1}$ 
##### Proof: 
Rearranging the elements of the term we get the equivalent term $\large{a_{n,1}a_{{n-1},2}\ldots a_{1,n}}$.So the sign of the term is equivalent to $\large{N(n,n-1,\ldots,1)}$ as outlined [[Determinants#Definition(Determinants)|here]].

Now we will show that $\large{N(n,n-1,\ldots,1) = \frac{n(n-1)}{2}}$ by induction:
###### Base Case: n=2
Consider $\large{N(2,1) = 1 + 0 = 1 = \frac{2*1}{2}}$ 

###### Induction Step:
Suppose that $\large{N(n,n-1,\ldots,1) = \frac{n(n-1)}{2}}$, Now consider $\large{N(n+1,n,n-1, \ldots, 1)}$. The inclusion of the term $\large{n+1}$ introduces $\large{n}$ [[Determinants#Definition(Determinants)|inversions]] to the series as $\large{n+1 \gt n,n-1,\ldots, 1}$, so 
$$\large{\begin{eqnarray} 
N(n+1,n,n-1,\ldots,1) &=& n + N(n,n-1,\ldots,1) \\
&=& n + \frac{n(n-1)}{2} \\ 
&=& \frac{2n + n(n-1)}{2} \\
&=& \frac{n^2 +n}{2} \\
&=& \frac{(n+1)n}{2}
\end{eqnarray}}$$

Now we will show that $\large{\frac{n(n-1)}{2}}$ is odd if and only if $\large{n(n-1)\not{|} \ 4}$:
###### (=>):
Suppose that $\large{\frac{n(n-1)}{2}}$ is odd, then $\large{\frac{n(n-1)}{2} = 2m + 1}$ where $\large{m}$ is some integer. This condition is equivalent to $\large{n(n-1)=4m + 2}$.
Suppose for sake of contradiction that $\large{n(n-1) | 4}$ so for some natural number $\large{c}$, $\large{4c = 4m + 2}$ which means $\large{c = m+ \frac{1}{2}}$ which is impossible as $\large{m}$ and $\large{c}$ are whole numbers. 
So if $\large{\frac{n(n-1)}{2}}$ is odd then $\large{n(n-1) \not{|} \ 4}$.

###### (<=):
Suppose that $\large{n(n-1)\not{|} \ 4}$ So for every natural $\large{c}$ $\large{n(n-1) \ne 4c}$.
Suppose for the sake of contradiction that $\large{\frac{n(n-1)}{2}}$ is even so $\large{\frac{n(n-1)}{2} = 2m}$ for some integer $\large{m}$, this condition is equivalent to $\large{n(n-1) = 4m}$, which means that $\large{n(n-1) | 4}$ contradicting our earlier assumption.
Hence if $\large{n(n-1) \not{|} \ 4}$ then $\large{\frac{n(n-1)}{2}}$ is odd.

Hence: 
$\large{\frac{n(n-1)}{2}}$ is odd if and only if $\large{n(n-1) \not{|} \ 4}$.

Now we will show $\large{n(n-1) \not{|} \ 4}$ if and only if $\large{n \operatorname{mod} 4 \ne 0}$ and $\large{n \operatorname{mod} 4 \ne 1}$.
###### (=>):
Suppose that $\large{n(n-1) \not{|} \ 4}$ so for every natural $\large{c}$ $\large{n(n-1) \ne 4c}$. 
Suppose for the sake of contradiction that either $\large{n \operatorname{mod} 4 = 0}$ or $\large{n \operatorname{mod} 4 = 1}$.
**Case I:** $\large{n \operatorname{mod} 4 = 1}$
hence, $\large{n = 4k + 1}$ for some natural $\large{k}$, this condition is equivalent to $\large{n-1 = 4k}$ this would mean that $\large{n-1 | 4}$ which means that $\large{n(n-1) | 4}$ contradicting our earlier assumption.

**Case II:** $\large{n \operatorname{mod} 4 = 0}$
hence, $\large{n= 4k}$ for some natural $\large{k}$, so $\large{n | 4}$ meaning that $\large{n(n-1)|4}$ contradicting our earlier assumption.
So by contradiction $\large{n \operatorname{mod} 4 \ne 0}$ and $\large{n \operatorname{mod} 4 \ne 1}$.

###### (<=):
Suppose that $\large{n \operatorname{mod} 4 \ne 0}$ and $\large{n \operatorname{mod} 4 \ne 1}$. 
Suppose for the sake of contradiction that $\large{n(n-1) | 4}$. 
If $\large{n(n-1) | 4}$ then $\large{n | 4}$ or $\large{n-1 | 4}$ or $\large{n  | 2}$ and $\large{n-1 | 2}$.
**Case I:** $\large{n | 4}$
Then there is some natural $\large{k}$ such that $\large{n = 4k}$, but then $\large{n \operatorname{mod} 4 =0}$ contradicting our earlier assumption.
**Case II:** $\large{n-1 | 4}$
Then there is some natural $\large{k}$ such that $\large{n = 4k + 1}$, but then $\large{n \operatorname{mod} 4 = 1}$ contradicting our earlier assumption.
**Case III**: $\large{n | 2}$ and $\large{n-1 | 2}$
But if $\large{n}$ is even then $\large{n-1}$ is odd contradicting $\large{n-1}$.

So if $\large{n \operatorname{mod} 4 \ne 1}$ and $\large{n \operatorname{mod} 4 \ne 0}$ then $\large{n(n-1) \not{|} \ 4}$

Hence the sign of the term is odd if and only if $\large{n \operatorname{mod} 4 \ne 1}$ and $\large{n \operatorname{mod} 4 \ne 0}$.