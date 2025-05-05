---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q13
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
Construct four [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Independent Columns]] of four numbers each

#### Solution: 
$$\large{
\begin{matrix} 
x_1 = \begin{vmatrix}1 \\0\\ 0 \\0 \end{vmatrix} & 
x_2 = \begin{vmatrix}0 \\ 1 \\ 0 \\ 0 \end{vmatrix} & 
x_3 = \begin{vmatrix}0 \\ 0 \\ 1 \\ 0 \end{vmatrix} & 
x_4 = \begin{vmatrix}0 \\ 0 \\ 0 \\ 1 \end{vmatrix}
\end{matrix}
}$$
By contrapositive of [[Linear Dependence Between Columns of a Determinant#Theorem 1.96|Theorem 1.96]] we know to prove this assertion it is sufficient to show that the [[Determinants#Definition(Determinants)|determinant]]:
$$\large{D = \begin{vmatrix}1 & 0 &0 & 0 \\ 
0 & 1  &0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1\end{vmatrix}}$$
is non-zero. 

We recognise $\large{D}$ as a [[The Triangular Determinant#Definition|Triangular Determinant]] so by [[The Triangular Determinant#Theorem 1.55b|Theorem 1.55b]]: 
$$\large{D = 1 \cdot 1 \cdot 1 \cdot 1 = 1 \ne 0}$$
So $\large{x_1,x_2,\ldots,x_4}$ constitute four [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Independent Columns]] of four numbers each as asserted.