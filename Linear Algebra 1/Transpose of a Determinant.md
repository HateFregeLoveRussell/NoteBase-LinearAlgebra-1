---
type: Academic
tags:
alias: Lin-Alg-1-TransposeOfADeterminant
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
  class-alias: "Lin-Alg-1",
  book-title: "Linear Algebra",
  source-alias: "Lin-Alg-1-Ch1-Sec1-4",
  type: "tbsection",
  ISBN: "978-0-486-63518-7",
  end-page: 12,
  section-name: "Properties of Determinants",
  template: {
    type: "object",
    version: 1,
    name: "source-tbsection-obj"
  },
  start-page: 8
}
relationship: {name: standard-relationship-obj, version: 1}
friends: "[[Transposition Property of the Determinant]]" 
status: {
  state: "Completed",
  template: {
    name: "status-obj",
    version: 1,
    type: "object"
  }
}
validity:  {
  state: True,
  template: {
    name: "validity-obj",
    version: 1,
    type: "object"
  }
}
template: {name: class-note-template, version: 1}
---
#### Definition 1.41 (Transposition): 
By the **==Transpose==** of a [[Determinants#Definition(Determinants)|Determinant]] we mean the Determinant in which the column and row indices of each entry are exchanged. 
$$\Large{
\begin{vmatrix}\begin{vmatrix} 
a_{11} & a_{12} & \ldots & a_{1n} \\
a_{21} & a_{22} & \ldots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \ldots & a_{nn}
\end{vmatrix}\end{vmatrix}
\ \ \underrightarrow{Transposition} \ \ 
\begin{vmatrix}\begin{vmatrix} 
a_{11} & a_{21} & \ldots & a_{n1} \\
a_{12} & a_{22} & \ldots & a_{n2} \\
\vdots & \vdots & \ddots & \vdots \\
a_{1n} & a_{2n} & \ldots & a_{nn}
\end{vmatrix}\end{vmatrix}
}
$$
##### Note: 
The Transposition of the Transposition of a Determinant is the Determinant itself
Additionally, 
An equivalent geometric notion of Transposition is rotating the determinant along the [[Square Matrices#Definition (Square Matrix)|Principal Diagonal]] for $\large{180 \degree}$.
![[MatrixGeometricTransposeExample |700]]
