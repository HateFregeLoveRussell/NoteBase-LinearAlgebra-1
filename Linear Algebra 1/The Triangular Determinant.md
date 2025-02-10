---
type: Academic
tags:
alias: Lin-Alg-1-TheTriangularDeterminant
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
  class-alias: "Lin-Alg-1",
  section-name: "Cofactors And Minors",
  ISBN: "978-0-486-63518-7",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  },
  book-title: "Linear Algebra",
  start-page: 12,
  end-page: 16,
  source-alias: "Lin-Alg-1-Ch1-Sec1-5"
}
relationship: {name: standard-relationship-obj, version: 1}
friends: ["[[Minors of a Determinant]]", "[[Cofactor of a Determinant]]"]
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

#### Definition: 
[[Determinants#Definition(Determinants)|Determinants]] of the form: 
$$\large{D_n = 
\begin{vmatrix}
a_{1,1} & 0 & 0 & \ldots &0 \\
a_{2,1} & a_{2,2} & 0 & \ldots & 0  \\ 
a_{3,1} & a_{3,2} & a_{3,3} & \ldots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\ 
a_{n,1} & a_{n,2} & a_{n,3} & \ldots &a_{n,n}
\end{vmatrix}
}$$
are called **==Triangular==**.

##### Theorem 1.55b:
[[The Triangular Determinant#Definition|Triangular]] [[Determinants#Definition(Determinants)|determinants]] of order $\large{n}$ can be computed through the formula: 
$$\large{
D_n = a_{1,1}a_{2,2}\ldots a_{n,n} = \prod_{k=1}^n a_{k,k}
}$$
##### Proof:
Through repeated application of [[Minors of a Determinant#Theorem 1.54|Theorem 1.54]] we can see that:
$$\large{
\begin{eqnarray} 
D_n &=& a_{11}D_{n-1} \\ 
D_{n-1} &=& a_{22}D_{n-2} \\ 
&\vdots& \\
D_1 &=& a_{nn}
\end{eqnarray}
}$$
Substituting backwards we get the desired equality. 
