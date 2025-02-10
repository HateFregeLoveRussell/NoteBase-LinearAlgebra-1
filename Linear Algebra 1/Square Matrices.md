---
type: Academic
tags:
alias: Lin-Alg-1-SquareMatrices
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
#### Definition (Square Matrix): 
By a **==Square Matrix==** of size $\large n$ we mean the array of $\large{n^2}$ [[Number Fields#Definition (Number Fields)|numbers]] denoted $\large{a_{ij}}$ where each of $\large{i}$ and $\large{j}$ can be any natural number between $\large{1}$ and $\large{n}$. The array itself is of the form: 
$$\large{

\begin{vmatrix}\begin{vmatrix} 
a_{11} & a_{12} & \ldots & a_{1n} \\
a_{21} & a_{22} & \ldots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \ldots & a_{nn}
\end{vmatrix}\end{vmatrix}
}$$
The number $\large{n}$ being the number of both rows and columns in the matrix is called the **==order==** of the matrix.
The numbers $\large{a_{ij}}$ are called the **==elements==** of the matrix. The index $\large{i}$ indicates the row of the element and $\large{j}$ indicates the column number.

The elements $\large{a_{11}, a_{22}, \ldots, a_{nn}}$ of a matrix of order $\large{n}$ are called the **==principal diagonal==** of the matrix