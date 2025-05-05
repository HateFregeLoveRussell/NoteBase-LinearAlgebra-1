---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q12
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
  type: "tbsection",
  source-alias: "Lin-Alg-1-Ch1-PP",
  book-title: "Linear Algebra",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  },
  start-page: 28,
  class-alias: "Lin-Alg-1",
  end-page: 30,
  section-name: "Chapter 1 Practice Problems",
  ISBN: "978-0-486-63518-7"
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
template: {name: class-note-template, version: 1}
---
### Problem Statement: 
Prove the theorem which bears the same relation to [[Laplace's Theorem#Theorem 1.81(Laplace's Theorem in Rows)|Laplace's Theorem]] as [[Cofactor of a Determinant#Theorem 1.52|Theorem 1.52]] bears to [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]]
#### Solution: 
Suppose we have two distinct sets of rows of size $\large{k}$ for the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$, call them $\large{I_1}$ and $\large{I_2}$, $\large{I_1 \ne I_2}$.
Suppose that $\large{i_1,i_2,\ldots,i_k \in I_1}$ and $\large{i_1^\prime, i_2^\prime, \ldots, i_k^\prime \in I_2}$. 
Then $$\large{
\sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n} M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k} \overline{A}_{j_1,j_2,\ldots,j_k}^{i_1^\prime,i_2^\prime,\ldots,i_k^\prime} = 0
}$$
where $\large{M}$ represents a [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor]] of order $\large{k}$ and $\large{\overline{A}}$ the Cofactor of the minor $\large{M}$.
$\large{\overline{A}_{j_1,j_2, \ldots, j_k}^{i_1,i_2,\ldots, i_k} = (-1)^{i + j}\overline{M}_{j_1, j_1, \ldots, j_k}^{i_1, i_2, \ldots, i_k}}$ 

##### Proof:
Since $\large{I_1 \ne I_2}$ and both $\large{I_1}$ and $\large{I_2}$ contain the same number of elements there must exist the elements $\large{c_1}$ and $\large{c_2}$ such that: $\large{c_1 \in I_1, c_1\not \in I_2, c_2\in I_2, c_2 \not \in I_1}$.

From [[Laplace's Theorem#Theorem 1.81(Laplace's Theorem in Rows)|Laplace's Theorem]] we know that: 
$$\large{D = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n} M_{j_1,j_2,\ldots,j_k}^{i_1,i_2, \ldots, i_k}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$$
Replacing the term $\large{M_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$ with the term $\large{M_{j_1,j_2,\ldots,j_k}^{i_1^\prime, i_2^\prime, \ldots, i_k^\prime}}$ we get the equality:
$$\large{D^\prime = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n} M_{j_1,j_2,\ldots,j_k}^{i_1^\prime,i_2^\prime, \ldots, i_k^\prime}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$$
where $\large{D^\prime}$ represents some augmented [[Determinants#Definition(Determinants)|determinant]].

Consider an arbitrary term from the above sum: $\large{M_{j_1,j_2,\ldots,j_k}^{i_1^\prime,i_2^\prime, \ldots, i_k^\prime}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$:
Note that the elements $\large{a_{c_2, j_1}, a_{c_2,j_2}, \ldots, a_{c_2,j_k}}$ belong to both $\large{M_{j_1,j_2,\ldots,j_k}^{i_1^\prime,i_2^\prime, \ldots, i_k^\prime}}$ and $\large{\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$, meaning that if the term was computed from some determinant $\large{D^\prime}$ then the elements $\large{a_{c_2,j_1},a_{c_2,j_2},\ldots, a_{c_2,j_k}}$ would appear in two distinct rows.
Since $\large{M_{j_1,j_2,\ldots,j_k}^{i_1^\prime,i_2^\prime, \ldots, i_k^\prime}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$ was chosen arbitrarily this property holds for all $\large{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n}$.
Since the set of all $\large{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n}$ scans across all the columns of the determinant $\large{1,2,\ldots ,n}$ it stands that $\large{D^\prime}$ must contain a duplicate set of rows so by [[Anti-symmetry Property of the Determinant#Corollary 1.43.2|Corollary 1.43.2]] $\large{D^\prime = 0}$ 
Substituting this we find that: 
$$\large{0 = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n} M_{j_1,j_2,\ldots,j_k}^{i_1^\prime,i_2^\prime, \ldots, i_k^\prime}\overline{A}_{j_1,j_2,\ldots,j_k}^{i_1,i_2,\ldots,i_k}}$$
as asserted. 
