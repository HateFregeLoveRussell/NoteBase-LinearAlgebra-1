---
type: Academic
tags:
alias: Lin-Alg-1-Determinants
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
  end-page: 8,
  type: "tbsection",
  template: {
    name: "source-tbsection-obj",
    version: 1,
    type: "object"
  },
  section-name: "Determinants of Order n",
  source-alias: "Lin-Alg-1-Ch1-Sec1-3",
  class-alias: "Lin-Alg-1",
  start-page: 5,
  ISBN: "978-0-486-63518-7",
  book-title: "Linear Algebra"
}
relationship: {name: standard-relationship-obj, version: 1}
friends: [[Problems of Interest for Systems of Linear Equations]]
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
#### Definition(Determinants): 
The **==Determinant==** $\large{D}$ of an order $\large{n}$ [[Square Matrices#Definition (Square Matrix)|Square Matrix]] is the algebraic sum of the $\large{n!}$ [[Determinants#Construction of the Products of the Determinant|Products of the Determinant]] where each such product denoted $\large{a_{\alpha_1 1} a_{\alpha_2 2} \ldots a_{\alpha_n n}}$ is scaled by $\large{(-1)^{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}}$. In other words the product is negative if $\large{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}$ is odd and positive otherwise. So: 
$$\large{
D = \sum (-1)^{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}a_{\alpha_1 1}a_{\alpha_2 2} \ldots a_{\alpha_n n}
}$$
The products in the sum above are called the **==terms==** of the Determinant $\large{D}$.
[[Square Matrices#Definition (Square Matrix)|Elements]] of a the Square Matrix from which the Determinant is calculated $\large{a_{ij}}$ are also called the **==elements==** of the Determinant $\large{D}$.
The [[Square Matrices#Definition (Square Matrix)|Order]] of the Square Matrix from which the Determinant is calculated from $\large{n}$ is also called the **==order==** of the Determinant $\large{D}$.
The Determinant $\large{D}$ can also be denoted explicitly through the notation:
$$\large{
D = 
\begin{vmatrix} 
a_{11} & a_{12} & \ldots & a_{1n} \\
a_{21} & a_{22} & \ldots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \ldots & a_{nn}
\end{vmatrix}
=
\det \left || a_{ij}\right || 
}
$$
##### Examples: 
$$\large
\begin{vmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{vmatrix} = a_{11}a_{22} - a_{12}a_{21} 
$$
and
$$
\large{
\begin{eqnarray}
\begin{vmatrix}
a_{11} & a_{12} & a_{13} \\ 
a_{21} & a_{22} & a_{23} \\ 
a_{31} & a_{32} & a_{33}
\end{vmatrix}
 = a_{11}a_{21}a_{33} + a_{21}a_{32}a_{13} + a_{31}a_{12}a_{23}  \\
  - a_{31}a_{22}a_{13} - a_{21}a_{12}a_{33} - a_{11}a_{32}a_{23}
 \end{eqnarray}
}
$$

##### Construction of the Products of the Determinant: 
Consider any product of $\large{n}$ elements of an order $\large{n}$ [[Square Matrices#Definition (Square Matrix)|Matrix]] each element where each term in the product appear in a different row and column. Call this product $\large{a_{\alpha_1 \beta_1}a_{\alpha_2 \beta_2} \ldots a_{\alpha_n \beta_n}}$. 

This product will naturally contain some term from the first column some term from the second column and so on.So we agree by convention to call $\large{\alpha_1}$ the row of the term in the first column, $\large{\alpha_2}$ the row of the second column and so on. With this convention our notation simplifies to $\large{a_{\alpha_1 1}a_{\alpha_2 2}\ldots a_{\alpha_n n}}$. 

Thus the product is fully characterised by the ordered list of indices $\large{(\alpha_1, \alpha_2, \ldots, \alpha_n)}$. Where each $\large{\alpha_i \in (\alpha_1, \alpha_2, \ldots, \alpha_n)}$ is distinct and the list is some 
permutation of the numbers $\large{1,2,\ldots,n}$. Its clear from this that the total number of such products is the total number of permutations of the numbers $\large{1,2,\ldots, n}$
being the familiar $\large{n!}$

By an **==Inversion==** on the product we mean a pair from $\large{\alpha_1, \alpha_2, \ldots, \alpha_n}$ denoted $\large{(\alpha_{k_1},\alpha_{k_2})}$ where $\large{\alpha_{k_1} > \alpha_{k_2}}$ but $\large{k_1 < k_2}$. The total number of inversions for a sequence $\large{\alpha_1, \alpha_2, \ldots, \alpha_n}$ is denoted $\large{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}$.

###### Example: 
$\large{N(2,1,4,3) = 2 = \left|\{(2,1), (4,3)\}\right| }$
and 
$\large{N(4,3,1,2) = 5 = \left | \{ (4,3),(4,1),(4,2),(3,1),(3,2)\} \right |}$ 

