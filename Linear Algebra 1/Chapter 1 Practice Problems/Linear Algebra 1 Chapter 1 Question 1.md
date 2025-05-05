---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q1
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
Determine the sign with which the terms $\large{a_{2,3}a_{3,1}a_{4,2}a_{5,6}a_{1,4}a_{6,5}}$ and $\large{a_{3,2}a_{4,3}a_{1,4}a_{5,1}a_{6,6}a_{2,5}}$ appear in a [[Determinants#Definition(Determinants)|determinant]] of order $\large{6}$

#### Solution:
The term $\large{a_{2,3}a_{3,1}a_{4,2}a_{5,6}a_{1,4}a_{6,5}}$ appears in a [[Determinants#Definition(Determinants)|determinant]] of order $\large{6}$ with the sign $\large{(-1)^{N(3,4,2,1,6,5)}}$ (first order the terms according to column).
Evaluating this term: 
$$\large{N(3,4,2,1,6,5) = 2 + 2 + 1 + 1 + 0+0= 6}$$ which is even. Hence the sign of the term is $\large{+}$.
Similarly the term $\large{a_{3,2}a_{4,3}a_{1,4}a_{5,1}a_{6,6}a_{2,5}}$ appears in the determinant of order $\large{6}$ with the sign $\large{(-1)^{N(5,3,4,1,2,6)}}$. 
Evaluating the term we get: 
$$\large{
N(5,3,4,1,2,6) = 4 + 2 + 2+0+0+0 = 8
}$$
which is also even so the sign of the term is $\large{+}$.