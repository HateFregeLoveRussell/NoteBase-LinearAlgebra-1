---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q2
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
  class-alias: "Lin-Alg-1",
  book-title: "Linear Algebra",
  end-page: 30,
  ISBN: "978-0-486-63518-7",
  section-name: "Chapter 1 Practice Problems",
  start-page: 28,
  type: "tbsection",
  template: {
    name: "source-tbsection-obj",
    type: "object",
    version: 1
  }
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
Find all the terms appearing in the [[Determinants#Definition(Determinants)|determinant]] of order $\large{4}$ which have a minus sign and contain the factor $\large{a_{2,3}}$.

#### Solution: 
In a [[Determinants#Definition(Determinants)|determinant]] of order $\large{4}$ all the terms containing the element $\large{a_{2,3}}$ are contained in the expression $\large{a_{2,3}A_{2,3}}$ where $\large{A_{2,3}}$ denotes a [[Cofactor of a Determinant#Definition(Cofactors)|Cofactor]] of the determinant at row $\large{2}$ and column $\large{3}$ by [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]].
According to [[Minors of a Determinant#Theorem 1.53|Theorem 1.53]] $\large{A_{2,3} = -M_{2,3}}$ where 
$$\large{
M_{2,3} = \begin{vmatrix}
a_{1,1} & a_{1,3} & a_{1,4} \\
a_{2,1} & a_{2,3} & a_{2,4} \\ 
a_{4,1} & a_{4,3} & a_{4,4}
\end{vmatrix}
}$$
We know that 
$\large{M_{2,3} = a_{1,1}a_{3,2}a_{4,4} - a_{1,1}a_{4,2}a_{3,4} - a_{3,1}a_{1,2}a_{4,4} + a_{3,1}a_{4,2}a_{1,4} - a_{4,1}a_{3,2}a_{1,4} + a_{4,2}a_{1,2}a_{3,4}}$
So 
$\large{A_{2,3} =  a_{1,1}a_{4,2}a_{3,4}- a_{1,1}a_{3,2}a_{4,4} + a_{3,1}a_{1,2}a_{4,4} - a_{3,1}a_{4,2}a_{1,4} + a_{4,1}a_{3,2}a_{1,4} - a_{4,2}a_{1,2}a_{3,4}}$
Hence the terms appearing in a determinant of order $\large{4}$ with negative sign and containing the element $\large{a_{2,3}}$ are:
$$\large{\{a_{2,3}a_{1,1}a_{3,2}a_{4,4}, a_{2,3}a_{3,1}a_{4,2}a_{1,4} , a_{2,3}a_{4,2}a_{1,2}a_{3,4}\}}$$
