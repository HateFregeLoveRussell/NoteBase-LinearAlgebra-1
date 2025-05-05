---
type: Academic
tags:
alias: Lin-Alg-1-TheQuasiTriangularDeterminant
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
friends: "[[Laplace's Theorem]]" 
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
#### Definition (Quasi-Triangular Determinant): 
We call [[Determinants#Definition(Determinants)|Determinants]] of the form: 
$$\large{D =
\begin{vmatrix}
a_{1,1} & \ldots  & a_{1,k} & 0 & \ldots &  0 \\
a_{2,1} & \ldots & a_{2,k} & 0 & \ldots & 0 \\ 
\vdots & \ddots & \vdots  & \vdots & \ddots & \vdots \\ 
a_{k,1} & \ldots & a_{k,k} & 0 & \ldots & 0 \\
a_{k+1,1} &\ldots & a_{k+1, k} & a_{k+1,k+1} & \ldots & a_{k+1, n} \\
\vdots & \ddots & \vdots & \vdots &\ddots & \vdots \\ 
a_{n,1} & \ldots & a_{n,k} & a_{n,k+1} & \ldots &a_{n,n}  
\end{vmatrix}
}$$
**==Quasi-Triangular==**.

#### Theorem 1.82: 
The [[The Quasi-Triangular Determinant#Definition (Quasi-Triangular Determinant)|Quasi-Triangular]] matrix of order $\large{n}$, denoted $\large{D}$ can be computed through the formula: 
$$\large{
D = 
\begin{vmatrix}
a_{1,1} & \ldots & a_{1,k} \\ 
\vdots & \ddots & \vdots  \\ 
a_{k,1} & \ldots & a_{k,k}
\end{vmatrix} 
.
\begin{vmatrix}
a_{k+1, k+1} & \ldots & a_{k+1, n} \\
\vdots & \ddots & \vdots \\ 
a_{k+1, n} & \ldots & a_{n,n}
\end{vmatrix}
}$$
##### Proof:
This formula can be found through the use of [[Laplace's Theorem#Theorem 1.81(Laplace's Theorem in Rows)|Laplace's Theorem]] on the rows $\large{1,2,\ldots, k}$ according to which: 
$$\large{D = \sum_{1 \le j_1 \lt j_2 \lt \ldots \lt j_k \le n} M_{j_1,j_2,\ldots,j_k}^{1,2, \ldots, k}\overline{A}_{j_1,j_2,\ldots,j_k}^{1,2,\ldots,k}}$$
We note that any selection of the columns $\large{j_1,j_2,\ldots,j_k}$ that is not $\large{1,2,\ldots,k}$ will necessarily contain a column which is composed of zeros for the first $\large{k}$ rows. 
This would mean that any [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor]] of order $\large{k}$, $\large{M_{j_1,j_2,\ldots,j_k}^{1,2,\ldots,k}}$ that is not equal to $\large{M_{1,2,\ldots,k}^{1,2,\ldots,k}}$ is equal to zero by [[The Linearity Property of Determinants#Corollary 1.46|Corollary 1.46]]. Hence the sum reduces to the expression: $$\large{ \begin{eqnarray}
D &=& M_{1,2,\ldots,k}^{1,2,\ldots,k}\overline A^{1,2,\ldots,k}_{1,2,\ldots,k} \\
&=& M_{1,2,\ldots,k}^{1,2,\ldots,k} \overline M^{1,2,\ldots,k}_{1,2,\ldots,k} \\
&=&
\begin{vmatrix}
a_{1,1} & \ldots & a_{1,k} \\ 
\vdots & \ddots & \vdots  \\ 
a_{k,1} & \ldots & a_{k,k}
\end{vmatrix} 
.
\begin{vmatrix}
a_{k+1, k+1} & \ldots & a_{k+1, n} \\
\vdots & \ddots & \vdots \\ 
a_{k+1, n} & \ldots & a_{n,n}
\end{vmatrix}
\end{eqnarray}
}
$$

