---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q6
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
  template: {
    version: 1,
    type: "object",
    name: "source-tbsection-obj"
  },
  end-page: 30,
  type: "tbsection",
  ISBN: "978-0-486-63518-7",
  class-alias: "Lin-Alg-1",
  start-page: 28,
  source-alias: "Lin-Alg-1-Ch1-PP",
  book-title: "Linear Algebra",
  section-name: "Chapter 1 Practice Problems"
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

### Problem Statement
Knowing that each of $\large{20604, 53227, 25755, 20927, 78421}$ are divisible by $\large{17}$, show that the following [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ is divisible by $\large{17}$.
$$\large{D = \begin{vmatrix}
2 & 0 & 6 & 0 & 4 \\
5 & 3 & 2 & 2 & 7 \\ 
2 & 5 & 7 & 5 & 5 \\ 
2 & 0 & 9 & 2 & 7 \\ 
7 & 8 & 4 & 2 & 1\end{vmatrix}}$$

#### Solution: 
Multiplying the first column by $\large{10^4}$, the second column by $\large{10^3}$ the third column by $\large{10^2}$ and the fourth column by $\large{10^2}$ using [[The Linearity Property of Determinants#Corollary 1.45|Corollary 1.45]] we get the relationship: 
$$\large{
D* 10^{4+3+2+1} = 10^{10}D =
\begin{vmatrix} 
2*10^4 & 0 & 6 *10^2 & 0 & 4 \\ 
5*10^4 & 3*10^3 & 2*10^2 & 2*10 & 7 \\ 
2*10^4 & 5*10^3 & 7*10^2 & 5*10 & 5 \\ 
2*10^4 & 0 & 9*10^2 & 2*10 & 7 \\
7*10^4 & 8*10^3 & 4*10^2 & 2*10 & 1
\end{vmatrix}}$$
Now we add all the columns to column $\large{5}$ using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{
10^{10}D =
\begin{vmatrix} 
2*10^4 & 0 & 6 *10^2 & 0 & 20604 \\ 
5*10^4 & 3*10^3 & 2*10^2 & 2*10 & 53227 \\ 
2*10^4 & 5*10^3 & 7*10^2 & 5*10 & 25755 \\ 
2*10^4 & 0 & 9*10^2 & 2*10 & 20927 \\
7*10^4 & 8*10^3 & 4*10^2 & 2*10 & 78421
\end{vmatrix}
}$$
Now using [[Cofactor of a Determinant#Theorem 1.51|Cofactor Expansion]] on the fifth Column: 
$$\large{10^{10}D = 20604A_{1,5} -53227A_{2,5} + 25755 A_{3,5} - 20927A_{4,5} + 78421A_{5,5}}$$
Since we know all such factors are divisible by 17 we know that $\large{10^{10}D}$ is divisible by 17. Since we know $\large{10^{10}}$ is not divisible by 17 we know that $\large{D}$ is divisible by 17, completing the proof. 
