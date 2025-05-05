---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q8
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
  source-alias: "Lin-Alg-1-Ch1-PP",
  section-name: "Chapter 1 Practice Problems",
  end-page: 30,
  book-title: "Linear Algebra",
  ISBN: "978-0-486-63518-7",
  class-alias: "Lin-Alg-1",
  type: "tbsection",
  template: {
    name: "source-tbsection-obj",
    type: "object",
    version: 1
  },
  start-page: 28
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
template: {name: class-textbook-practice-problem, version: 1}
---
### Problem Statement:
Compute the following [[Determinants#Definition(Determinants)|determinant]]: 
$$\large{
P(x) = \begin{vmatrix}1 & 1 & 2 & 3 \\ 1 & 2-x^2 & 2 & 3 \\ 2 & 3 & 1 & 5 \\ 2 & 3 & 1 & 9 - x^2 \end{vmatrix}
}$$
#### Solution: 
Subtracting the fourth row from the third row using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{P(x) = \begin{vmatrix}
1 & 1 & 2 & 3 \\ 
1 & 2-x^2 & 2 & 3 \\ 
0 & 0 & 0 & x^2 - 4 \\ 
2 & 3 & 1 & 9-x^2
\end{vmatrix}
}$$
Now using [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the third row of $\large{P(x)}$:
$$\large{P(x) = 
(4 - x^2)\begin{vmatrix}1 & 1 & 2 \\ 1 & 2-x^2 & 2 \\ 2 & 3 & 1 \end{vmatrix}
}$$
Subtract the second row from the first row using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{P(x) = (4-x^2) \begin{vmatrix}
0 & x^2 - 1& 0 \\ 1 & 2-x^2 & 2 \\ 2 & 3 & 1\end{vmatrix}}
$$
Now using [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] again on the first row: 
$$\large{P(x) = (4-x^2)(1-x^2) \begin{vmatrix}1 & 2 \\ 2 & 1\end{vmatrix}}$$
Now computing the remaining second order [[Determinants#Definition(Determinants)|determinant]] directly: 
$$\large{\begin{eqnarray} 
P(x) &=& (4-x^2)(1-x^2)(1 - 4) \\ 
&=& -3(x^2 - 4)(x^ 2 - 1) \\ 
&=& -3(x-2)(x+2)(x-1)(x+1)
\end{eqnarray}}$$
