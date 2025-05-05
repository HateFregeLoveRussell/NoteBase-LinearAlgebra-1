---
type: Academic
tags:
alias: Lin-Alg-1-LaplacesTheorem
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
  end-page: 23,
  ISBN: "978-0-486-63518-7",
  source-alias: "Lin-Alg-1-Ch1-Sec1-8",
  section-name: "Minors of Arbitrary Order, Laplaces Theorem",
  start-page: 20,
  type: "tbsection",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  },
  class-alias: "Lin-Alg-1",
  book-title: "Linear Algebra"
}
relationship: {name: standard-relationship-obj, version: 1}
friends: "[[Minors of Arbitrary Order]]"
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
template: {name: class-note-template, version: 1}
---

### Theorem 1.81(Laplace's Theorem in Rows):
Given a [[Determinants#Definition(Determinants)|Determinant]] $\large{D}$ of order $\large{n}$ and a fixed set of rows $\large{i_1,i_2,\ldots,i_k}$ (where $\large{k \le n}$), 
$$\large{D = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n} M_{j_1,j_2,\ldots,j_k}^{i_1,i_2, \ldots, i_k}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$$ where $\large{M}$ represents a [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor]] of order $\large{k}$ and $\large{\overline{A}}$ the **==Cofactor of the minor==** $\large{M}$.
$\large{\overline{A}_{j_1,j_2, \ldots, j_k}^{i_1,i_2,\ldots, i_k} = (-1)^{i + j}\overline{M}_{j_1, j_1, \ldots, j_k}^{i_1, i_2, \ldots, i_k}}$ 
Where $\large{\overline{M}}$ denotes the [[Minors of Arbitrary Order#Definition (Compliment of a Minor of Order k)|Complement]] of the Minor $\large{M}$ and 
$$\large{\begin{eqnarray} 
i &=& \sum_{p=1}^k i_p \ \ \ \ 
j &=& \sum_{p=1}^k j_p
\end{eqnarray}}$$
#### Introduction: 
This theorem is a generalisation of [[Cofactor of a Determinant#Theorem 1.51|Cofactor Expansion]] that is made with [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minors of Arbitrary Order]] instead of [[Minors of a Determinant#Definition(Minors)|Traditional Minors]]. 
Abstractly,this will be proven through first showing that an arbitrary [[Determinants#Definition(Determinants)|determinant]] can be partitioned into groups of terms and then that each of these groups equals an arbitrary minor multiplied to its respective cofactor. 

#### Partitioning of Terms: 
##### Introduction: 
Since every term in a [[Determinants#Definition(Determinants)|determinant]] is unique, showing that the sum can be grouped in a particular way reduces to showing that the set of terms for each group, constitute a valid partitioning of the set of all terms in the determinant. 

We consider a partitioning of a set $\large{S}$ by a (non-empty) family of sets $\large{\mathscr F}$ valid if it fulfils two properties:
Coverage:
$$\large{\bigcup \mathscr F = S}$$
and Disjointedness: 
$$\large{A \in \mathscr F \land B\in \mathscr F \land A \ne B \implies A \cap B = \emptyset}$$
##### Notation: 
We will say that a term $\large{(-1)^{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}a_{\alpha_1,1}a_{\alpha_2,2}\ldots a_{\alpha_k,k}\ldots a_{\alpha_n,n}}$  "fits" in a [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor of Order]] $\large{k \le n}$, $\large{M_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$, if the elements of the term at the specified rows (or columns) of the minor $\large{a_{i_1,\beta_{i_1}}a_{i_2,\beta_{i_2}}\ldots a_{i_k,\beta_{i_k}}}$ have columns(or rows) that are also in the set specified by the minor. In other words, every element in the term appears either in the minor $\large{M_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$ or its [[Minors of Arbitrary Order#Definition (Compliment of a Minor of Order k)|complement]] $\large{\overline{M}_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$.

We will call the set of all terms in a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ which "fit" in a minor $\large{M_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$, $\large{D_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$.

We will call the sum of every term in $\large{D_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$ (with the appropriate signs) $\large{\widetilde{D}_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$.

We will call the set of all terms in a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$, $\large{\mathscr D}$.

##### Claim:
For a fixed $\large{i_1,i_2, \ldots, i_k}$ the family $\large{\mathscr F = \{D_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}| 1 \le j_1 < j_2 < \ldots < j_k \le n \}}$ constitutes a valid partitioning of $\large{\mathscr D}$.

###### Proof of Coverage:
(=>):
Suppose that $\large{x \in \bigcup \mathscr F}$. By [[Laplace's Theorem#Claim|definition]] this would mean that there is some $\large{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n}$ such that $\large{x \in D_{i_1,i_2,\ldots,i_k}^{j_1,j_2,\ldots,j_k}}$. Since $\large{x \in D_{i_1,i_2,\ldots,i_k}^{j_1,j_2,\ldots,j_k}}$ then $\large{x \in \mathscr D}$ by [[Laplace's Theorem#Notation|definition]]. 
So $\large{\bigcup \mathscr F \subset \mathscr D}$.

(<=):
Suppose that $\large{x \in \mathscr D}$. This would mean $\large{x = (-1)^{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}a_{\alpha_1,1}a_{\alpha_2,2}\ldots a_{\alpha_k,k}\ldots a_{\alpha_n,n}}$.
Since the elements of any term in a [[Determinants#Definition(Determinants)|determinant]] must scan all rows it stands that these exists the elements $\large{a_{\alpha_{j_1},j_1}, a_{\alpha_{j_2},j_2}, \ldots, a_{\alpha_{j_k},j_k}}$ in $\large{x}$ where $\large{\alpha_{j_1} = i_1, \alpha_{j_2} = i_2, \ldots, \alpha_{j_k} = i_k}$.
Let $\large{\widetilde{j_1}}$ be the smallest of $\large{\{j_1,j_2,\ldots,j_k\}}$, $\large{\widetilde{j_2}}$ the second smallest and so on. 
Consider an arbitrary element from the collection above $\large{a_{\alpha_j,j}}$ where $\large{j \in \{\widetilde{j_1}, \widetilde{j_2}, \ldots, \widetilde{j_k}\}}$. From the construction of such an element we know that $\large{\alpha_j}$ equals one of $\large{\{i_1,i_2,\ldots, i_k\}}$. From this we know that the term $\large{x}$ "fits" in the [[Minors of Arbitrary Order#Definition (Minor of Order k)|minor]] $\large{M_{\widetilde{j_1},\widetilde{j_2},\ldots, \widetilde{j_k}}^{i_1,i_2,\ldots,i_k}}$, $\large{1 \le \widetilde{j_1} < \widetilde{j_2} < \ldots < \widetilde{j_k} \le n}$. This would then mean that $\large{x \in D_{\widetilde{j_1}, \widetilde{j_2}, \ldots, \widetilde{j_k}}^{i_1,i_2, \ldots, i_k}}$, and hence $\large{x \in \bigcup \mathscr F}$. 
So $\large{\mathscr D \subset \bigcup \mathscr F}$,

Hence, 
$\large{\mathscr D = \bigcup \mathscr F}$.

###### Proof of Pair-Wise Disjointedness:
Suppose that $\large{D_1 \in \mathscr F}$ and $\large{D_2 \in \mathscr F}$, $\large{D_1 \ne D_2}$.
Lets denote $\large{D_1 = D_{j_1,j_2, \ldots, j_k}^{i_1,i_2,\ldots,i_k}}$  and $\large{D_2 = D_{\widetilde{j_1}, \widetilde{j_2}, \ldots, \widetilde{j_k}}^{i_1,i_2,\ldots,i_k}}$ from the [[Laplace's Theorem#Claim|definition]] of $\large{\mathscr F}$.
Since $\large{D_1 \ne D_2}$ it stands that there is at least one column in which the sets $\large{\{j_1,j_2, \ldots, j_k\}}$ and $\large{\{\widetilde{j_1}, \widetilde{j_2}, \ldots, \widetilde{j_k}\}}$ disagree. Call this element column $\large{j}$. Without Loss of Generality we can assume $\large{j \in \{j_1,j_2, \ldots, j_k\}}$ $\large{j \not \in \{\widetilde{j_1}, \widetilde{j_2}, \ldots, \widetilde{j_k}\}}$.
Suppose for the sake of contradiction that $\large{D_1}$ and $\large{D_2}$ do share some [[Determinants#Definition(Determinants)|term]], call it $\large{a}$. 
Since $\large{a \in D_1}$ and $\large{j \in \{j_1, j_2, \ldots, j_k\}}$ there must be some element in $\large{a}$ such that its column is $\large{j}$, we will call the row of that element $\large{\alpha_j}$ and hence denote the element as a whole as $\large{a_{\alpha_j,j}}$. Additionally we know by [[Laplace's Theorem#Notation|definition]] that $\large{\alpha_j}$ is one of $\large{\{i_1,i_2,\ldots, i_k\}}$

Since $\large{a \in D_2}$ it stands that there must be some element of $\large{a}$ such that its row is $\large{\alpha_j}$, but then the corresponding column of such an element would be $\large{j}$ and we know that $\large{j \not \in \{\widetilde{j_1}, \widetilde{j_2}, \ldots, \widetilde{j_k}\}}$ leading to the desired contradiction. 

Hence $\large{D_1 \cap D_2 = \emptyset}$. And so the family $\large{\mathscr F}$ is pair-wise disjoint.

##### Conclusion: 
For a fixed $\large{i_1,i_2, \ldots, i_k}$, since $\large{\mathscr F}$ is a valid partitioning of $\large{\mathscr D}$ we can group the [[Determinants#Definition(Determinants)|terms]] of $\large{D}$ based on a series [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minors]] of order $\large{k}$.
$$\large{ \begin{eqnarray}
D &=& \sum (-1)^{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}a_{\alpha_1 1}a_{\alpha_2 2} \ldots a_{\alpha_n n} \\ 
&=&\sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n}  \widetilde{D}_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}
\end{eqnarray}
}$$

#### Evaluation of Groups:
##### Introduction: 
Now we will show that $\large{\widetilde{D}_{j_1,j_2, \ldots, j_k}^{i_1, i_2, \ldots, i_k} = M_{j_1,j_2, \ldots, j_k}^{i_1,i_2, \ldots, i_k}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots, i_k}}$. We will start by first proving the statement for $\large{\widetilde{D}_{1,2,\ldots, k}^{1,2,\ldots, k}}$ and then generalising for an arbitrary selection of rows and columns (assuming no repeating columns or rows). 
For the proof of $\large{\widetilde{D}_{1,2,\ldots,k}^{1,2,\ldots, k}}$ we will take advantage of the fact that every term in $\large{D_{1,2,\ldots,k}^{1,2,\ldots, k}}$ is distinct (since $\large{D_{1,2,\ldots,k}^{1,2,\ldots, k} \subset \mathscr D}$) and simply show that the set of terms on both side of the equality are equal. 
In other words we will first show that if $\large{x}$ is a term in $\large{{\widetilde{D}_{1,2,\ldots,k}^{1,2,\ldots, k}}}$ then $\large{x}$ is a product of one term in $\large{M_{1,2,\ldots, k}^{1,2,\ldots, k}}$ and another in $\large{\overline{A}_{1,2,\ldots,k}^{1,2,\ldots,k} = \overline{M}_{1,2,\ldots,k}^{1,2,\ldots,k}}$ (Note that these terms are necessarily unique as $\large{M}$ and $\large{\overline{M}}$ are both [[Determinants#Definition(Determinants)|determinants]]). Then secondly we will show that if $\large{x}$ is a term in $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}\overline{M}_{1,2,\ldots, k}^{1,2,\ldots, k}}$ then it is a term in $\large{\widetilde{D}_{1,2,\ldots,k}^{1,2,\ldots, k}}$.

##### Evaluation of the Simple Minor:
Consider $\large{\widetilde{D}_{1,2,\ldots,k}^{1,2,\ldots,k}}$ being the grouping of terms in the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ [[Laplace's Theorem#Notation|here]]. Additionally consider $\large{M_{1,2,\ldots, k}^{1,2,\ldots, k}}$ being a [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor of order]] $\large{k}$ of $\large{D}$ and also $\large{\overline{M}_{1,2,\ldots,k}^{1,2,\ldots,k}}$ being the [[Minors of Arbitrary Order#Definition (Compliment of a Minor of Order k)|compliment]] of that minor.  
We will show that $\large{\widetilde{D}_{1,2,\ldots,k}^{1,2,\ldots,k}= M_{1,2,\ldots,k}^{1,2,\ldots,k}\overline{M}_{1,2,\ldots,k}^{1,2,\ldots,k}}$.
(=>):
Suppose that $\large{c}$ is a term in $\large{\widetilde{D}_{1,2,\ldots,k}^{1,2,\ldots,k}}$ then by [[Laplace's Theorem#Notation|definition]] the first $\large{k}$ elements of the term (ordered on columns or rows) belong to the minor $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}}$ and the remaining $\large{n-k}$ elements of the term ($\large{n}$ being the [[Square Matrices#Definition (Square Matrix)|order]] of $\large{D}$) belonging to the complimentary minor $\large{\overline{M}_{1,2,\ldots,k}^{1,2,\ldots,k}}$.
Call the first $\large{k}$ elements of $\large{c}$ (ordered on rows or columns) $\large{c_1}$ and the remaining elements $\large{c_2}$.
We will call the sign with which the term $\large{c}$ appears in $\large{D}$ with $\large{(-1)^N}$.
We will call the sign with which the term $\large{c_1}$ appears with in $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}}$, $\large{(-1)^{N_1}}$ and similarly we will call the sign with which the term $\large{c_2}$ appears with in $\large{\overline{M}_{1,2,\ldots,k}^{1,2,\ldots,k}}$, $\large{(-1)^{N_2}}$. 
Its clear that $\large{c_1c_2}$ is composed of exactly the same elements as $\large{c}$ (by construction). 
So all that remains to be shown is that $\large{c}$ and $\large{c_1c_2}$ have precisely the same sign, or in other words that $\large{(-1)^N = (-1)^{N_1}(-1)^{N_2} = (-1)^{(N_1 + N_2)}}$.
Note that there are no [[Geometric Interpretation of the Determinant#Positive and Negative Slopes|segment of negative slope]] connecting any element of $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}}$ to any element of $\large{\overline M_{1,2,\ldots,k}^{1,2,\ldots,k} = M_{k+1,k+2,\ldots,n}^{k+1,k+2,\ldots,n}}$. This would mean that it is necessarily the case that $\large{(-1)^N = (-1)^{N_1 + N_2}}$.
And so if $\large{c}$ is a term in $\large{\widetilde{D}_{1,2,\ldots,k}^{1,2,\ldots,k}}$ then it is a product of one term from $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}}$ and another from its compliment $\large{\overline{M}_{1,2,\ldots,k}^{1,2,\ldots,k}}$.

(<=):
Suppose that $\large{c_1}$ is a term in $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}}$ and $\large{c_2}$ is a term in $\large{\overline M_{1,2,\ldots,k}^{1,2,\ldots,k}}$.
Note that $\large{c_1}$ is composed of $\large{k}$ elements from unique rows and columns in $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}}$ and $\large{c_2}$ is similarly composed of $\large{n-k}$ elements from unique rows and columns in $\large{M_{k+1,k+2, \ldots, n}^{k+1,k+2,\ldots,n}}$. This would mean that $\large{c_1c_2}$ would be composed of $\large{n}$ elements from unique rows and columns scanning across every row and column of $\large{D}$. In other words $\large{c_1c_2}$ has the exact same elements as some [[Determinants#Definition(Determinants)|term]] in $\large{\widetilde D_{1,2,\ldots,k}^{1,2,\ldots,k}}$ call it $\large{c}$. 
From the reasoning in the previous part of this proof we know that $\large{c}$ and $\large{c_1c_2}$ have the same sign so it stands to say $\large{c_1c_2 = c}$.
Therefore if we have two terms from $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}}$ and $\large{\overline{M}_{1,2,\ldots,k}^{1,2,\ldots,k}}$ then their product form some term in $\large{\widetilde D_{1,2,\ldots,k}^{1,2,\ldots,k}}$. 

Hence $\large{\widetilde{D}_{1,2,\ldots,k}^{1,2,\ldots,k} = M_{1,2,\ldots,k}^{1,2,\ldots,k}\overline M_{1,2,\ldots,k}^{1,2,\ldots,k}}$ .

##### Evaluation of a General Minor:
Now we will show that $\large{\widetilde{D}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k} = (-1)^{\sum_{p=1}^k i_p + j_p}M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}\overline M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$ .
Consider some arbitrary selection of $\large{k}$ rows and $\large{k}$ columns $\large{i_1,i_2,\ldots, i_k, j_1, j_2,\ldots, j_k}$.
This selection would naturally form a [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor of Order]] $\large{k}$ and its [[Minors of Arbitrary Order#Definition (Compliment of a Minor of Order k)|compliment]] denoted $\large{M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$ and $\large{\overline M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$ respectively.
Now suppose that we move this minor $\large{M}$ to the top left corner of the original [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ (and subsequently its compliment $\large{\overline M}$ to the bottom right corner) through successively interchanging $\large{i_1 -1, i_2 -2, \ldots, i_k -k }$ rows and $\large{j_1 -1 ,j_2 -2 ,\ldots,j_k -k}$ columns. This would form an augmented determinant we will call $\large{D^\prime}$. Note that $\large{M^{i_1,i_2,\ldots,i_k}_{j_1,j_2,\ldots,j_k} = M^{\prime 1,2,\ldots,k}_{1,2,\ldots,k}}$. And that by [[Anti-symmetry Property of the Determinant#Theorem 1.42 (The Anti-Symmetry Property in Columns)|The Anti-Symmetry Property of the Determinant in Columns]] $\large{D^\prime = (-1)^{\sum_{p= 1}^k (i_p - p)+\sum_{p = 1}^k{(j_p - p)}} D = (-1)^{\sum_{p=1}^k{i_p} + \sum{p=1}^k j_p- 2\sum_{p=1}^{k}p} D  = (-1)^{\sum_{p=1}^{k}(i_p + j_p)}D}$ 
Since we know that $\large{D = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n}  \widetilde{D}_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$  and $\large{D ^\prime = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n}  \widetilde{D^\prime}_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k}}$ it stands that $\large{\widetilde{D^\prime}^{1,2,\ldots,k}_{1,2,\ldots,k} = (-1)^{\sum_{p=1}^k(i_p + j_ p)}\widetilde{D}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots, i_k}}$.
We already know that $\large{\widetilde{D^\prime}_{1,2,\ldots,k}^{1,2,\ldots,k} = M_{1,2,\ldots,k}^{\prime1,2,\ldots,k} \overline{M}^{\prime 1,2,\ldots,k}_{1,2,\ldots,k} = M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}\overline M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$ 
So $\large{M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}\overline M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k} = (-1)^{\sum_{p=1}^k (i_p + j_p)}\widetilde D_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$. Diving the sign term from both sides yields the desired result of $\large{\widetilde{D}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k} =(-1)^{\sum_{p=1}^k (i_p + j_p)} M_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k} \overline{M}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$.

#### Conclusion: 
We know from the [[Laplace's Theorem#Partitioning of Terms|partitioning step]] that:
$$\large{D = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n} \widetilde{D}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$$
Additionally from the [[Laplace's Theorem#Evaluation of Groups|evaluation step]] we know that: 
$$\large{ \begin{eqnarray}
\widetilde{D}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k} &=& M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}\overline{A}_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k} \\
&=& (-1)^{i+j}M_{j_1,j_2 \ldots,j_k}^{i_1,i_2,\ldots, i_k}\overline M_{j_1,j_2, \ldots, j_k}^{i_1, i_2, \ldots, i_k}
\end{eqnarray}
}$$
where:
$$\large{\begin{eqnarray}
i &=& \sum_{p=1}^k i_k \\ 
j &=& \sum_{p=1}^k j_k
\end{eqnarray}}$$

Through simple substitution we find that given a set of unique fixed rows $\large{i_1,i_2,\ldots,i_k}$ the following equation for the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ holds:
$$\large{
D = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n} (-1)^{i + j} M_{j_1,j_2, \ldots, j_k}^{i_1,i_2, \ldots, i_k} \overline A_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}
}$$
### Corollary 1.81.1 (Laplace's Theorem in Columns):
Given a [[Determinants#Definition(Determinants)|Determinant]] $\large{D}$ of order $\large{n}$ and a fixed set of columns $\large{j_1,j_2,\ldots,j_k}$ (where $\large{k \le n}$), 
$$\large{D = \sum_{1 \le i_1 \lt i_2 \lt \ldots \lt i_k \le n} M_{j_1,j_2,\ldots,j_k}^{i_1,i_2, \ldots, i_k}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$$ where $\large{M}$ represents a [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor]] of order $\large{k}$ and $\large{\overline{A}}$ the **==Cofactor of the minor==** $\large{M}$.
$\large{\overline{A}_{j_1,j_2, \ldots, j_k}^{i_1,i_2,\ldots, i_k} = (-1)^{i + j}\overline{M}_{j_1, j_1, \ldots, j_k}^{i_1, i_2, \ldots, i_k}}$ 
Where $\large{\overline{M}}$ denotes the [[Minors of Arbitrary Order#Definition (Compliment of a Minor of Order k)|Complement]] of the Minor $\large{M}$ and 
$$\large{\begin{eqnarray} 
i &=& \sum_{p=1}^k i_p \ \ \ \ 
j &=& \sum_{p=1}^k j_p
\end{eqnarray}}$$
#### Proof:
Take the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ and the selection of columns $\large{j_1,j_2, \ldots, j_k}$. Now take the [[Transpose of a Determinant#Definition 1.41 (Transposition)|transpose]] of $\large{D}$ to produce the determinant $\large{D^\prime}$. From [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|The Transposition Property]] we know that $\large{D = D^\prime}$. 
Use [[Laplace's Theorem#Theorem 1.81(Laplace's Theorem in Rows)|Laplace's Theorem in Rows]] on $\large{D^\prime}$ using $\large{i^\prime_1 = j_1, i^\prime_2 = j_2, \ldots, i^\prime_k = j_k}$.
From this we get the expression: 
$$\large{D^\prime = \sum_{1 \le j^\prime_1 \lt j^\prime_2 \lt \ldots \lt j^\prime_k \le n} M_{j^\prime_1,j^\prime_2,\ldots,j^\prime_k}^{i^\prime_1,i^\prime_2,\ldots,i^\prime_k}\overline{A}_{j^\prime_1,j^\prime_2,\ldots,j^\prime_k}^{i^\prime_1,i^\prime_2,\ldots,i^\prime_k}}$$
We additionally note that whatever column chosen in $\large{D^\prime}$, $\large{j^\prime_p}$ is just some row in $\large{D}$, $\large{i_p}$, Using this and the previous substitution of the rows in $\large{D^\prime}$ we can re-write the expression as: 
$$\large{D^\prime = \sum_{1 \le i_1 \lt i_2 \lt \ldots \lt i_k \le n} M_{i_1,i_2,\ldots,i_k}^{j_1,j_2,\ldots,j_k}\overline{A}_{i_1,i_2,\ldots,i_k}^{j_1,j_2,\ldots,j_k}}$$
Now we note that $\large{M_{i_1,i_2,\ldots,i_k}^{j_1,j_2,\ldots,j_k}}$ is simply the [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor]] $\large{M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$ but with the columns and rows switched. In other words $\large{M_{i_1,i_2,\ldots,i_k}^{j_1,j_2,\ldots,j_k}}$ is the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transpose]] $\large{M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$ and hence since Minors are themselves Determinants, by [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|The Transposition Property]]: 
$$\large{M_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k} = M_{i_1,i_2,\ldots,i_k}^{j_1,j_2,\ldots,j_k}}$$
From this we also know that:
$$\large{\overline{A}_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots,i_k} = \overline A_{i_1,i_2,\ldots,i_k}^{j_1,j_2,\ldots,j_k}}$$
Then by substitution we get the desired relationship: 
$$\large{D = \sum_{1 \le i_1 \lt i_2 \lt \ldots \lt i_k \le n} M_{j_1,j_2,\ldots,j_k}^{i_1,i_2, \ldots, i_k}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$$


### Remark: 
[[Laplace's Theorem#Theorem 1.81(Laplace's Theorem in Rows)|Laplace's Theorem]] is remarkably useful in the simplification of [[The Quasi-Triangular Determinant#Definition (Quasi-Triangular Determinant)|Quasi-Triangular Determinants]]. See [[The Quasi-Triangular Determinant#Theorem 1.82|Theorem 1.82]].