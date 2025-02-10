---
type: Academic
tags:
alias: Lin-Alg-1-GeometricInterpretationOfTheDeterminant
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
  source-alias: "Lin-Alg-1-Ch1-Sec1-3",
  class-alias: "Lin-Alg-1",
  section-name: "Determinants of Order n",
  type: "tbsection",
  start-page: 5,
  template: {
    version: 1,
    name: "source-tbsection-obj",
    type: "object"
  },
  book-title: "Linear Algebra",
  ISBN: "978-0-486-63518-7",
  end-page: 8
}
relationship: {name: standard-relationship-obj, version: 1}
friends: "[[Determinants]]"
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

The [[Determinants#Definition(Determinants)|Determinant]] can be formulated slightly differently through a geometric view of the [[Square Matrices#Definition (Square Matrix)|Matrix]].

#### Positive and Negative Slopes:
For a pair of elements in a [[Square Matrices#Definition (Square Matrix)|Matrix]] called $\large{(a_{\alpha_1, \beta_1}, a_{\alpha_2, \beta_2})}$ and a line joining them we say that the line has a **==positive slope==** when $\large{a_{\alpha_2,\beta_2}}$ (the right endpoint) lies below $\large{a_{\alpha_1, \beta_1}}$ (the left endpoint). Similarly we say that the line has a **==negative slope==** when $\large{a_{\alpha_2 \beta_2}}$ (the left endpoint) lies on top of $\large{a_{\alpha_1, \beta_1}}$ (the right endpoint).

![[MatrixConncection1]]
##### Note: 
It is important to note that the notion of positive and negative slope described here is not the same as the one in Analytic Geometry.

#### The Role of Slope in Computing Determinants:
For a given [[Determinants#Definition(Determinants)|term in the Determinant]] $\large{D}$ denoted $\large{a_{\alpha_1 1} a_{\alpha_2 2} \ldots a_{\alpha_n n}}$ we associate a negative sign with term if the number of [[Geometric Interpretation of the Determinant#Positive and Negative Slopes|Negative Slopes]] between the elements of the term is odd. We associate a positive sign with the term when the number is even so $\large{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}$ is equivalent to the number of negative slopes in the term $\large{a_{\alpha_1 1}a_{\alpha_2 2}\ldots a_{\alpha_n n}}$.

##### Examples: 
![[MatrixSlopeExample1|800]]

So $\large{\text{det}||a_{ij}|| = a_{11}a_{22}a_{33} + a_{21}a_{32}a_{13} + a_{31}a_{12}a_{23} - a_{31}a_{22}a_{13} - a_{11}a_{22}a_{33} - a_{21}a_{12}a_{33}}$ 
##### Proof: 
Suppose that an [[Determinants#Construction of the Products of the Determinant|Inversion]] in a given sequence for the pair $\large{(a_{ij}, a_{kl})}$ by definition then  $\large{i > l}$ and $\large{j < k}$ but $\large{i > l}$ and $\large{j < k}$ $\large{\text{iff}}$ $\large{a_{ij}}$ is situated bottom-left of $\large{a_{lk}}$ so $\large{(a_{ij}, a_{lk})}$ has negative slope.