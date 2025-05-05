---
type: Academic
tags:
alias: Lin-Alg-1-MinorsOfArbitraryOrder
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
  type: "tbsection",
  section-name: "Minors of Arbitrary Order, Laplaces Theorem",
  class-alias: "Lin-Alg-1",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  },
  book-title: "Linear Algebra",
  start-page: 20
}
relationship: {name: standard-relationship-obj, version: 1}
friends: "[[Minors of a Determinant]]"
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
#### Definition (Minor of Order k): 
Consider some [[Square Matrices#Definition (Square Matrix)|square matrix]] of order $\large{n}$. Specify some positive natural number $\large{k \le n}$, and pick $\large{k}$ rows and $\large{k}$ columns in the matrix. The elements appearing in the intersection of these rows and columns form another square matrix of order $\large{k}$. We call the [[Determinants#Definition(Determinants)|determinant]] of this sub-matrix a **==Minor of Order ==** $\large{k}$ of both the [[Determinants#Definition(Determinants)|determinant]] of the original matrix and the matrix itself.

We denote this minor with: 
$$\large{M = M_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots, i_k}}$$
Where $\large{i_1,i_2,\ldots. i_k}$ represents the $\large{k}$ rows of the original determinant and $\large{j_1,j_2,\ldots,j_k}$ represents the $\large{k}$ columns of the original determinant.  

#### Definition (Compliment of a Minor of Order k):
Given a [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor of Order]] $\large{k}$, $\large{M = M_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots, i_k}}$ of some [[Square Matrices#Definition (Square Matrix)|square matrix]] of order $\large{n}$, if we instead delete the rows $\large{i_1,i_2,\ldots, i_k}$ and $\large{j_1,j_2, \ldots, j_k}$ from the original matrix we obtain another square matrix of order $\large{n-k}$. The determinant of this resultant matrix is called the **==Complimentary Minor of==** $\large{M}$ denoted:
$$\large{
\overline{M} = \overline{M}_{j_1,j_2,\ldots, j_k}^{i_1,i_2,\ldots, i_k}
}$$
##### Remark: 
Note that the minors in [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]], $\large{M_{i,j}}$ are themselves [[Minors of Arbitrary Order#Definition (Compliment of a Minor of Order k)|Complementary Minors]] of order $\large{n-1}$ obtained from [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minors]] of order $\large{1}$, i.e. the elements $\large{a_{i,j}}$.