---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q4
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
### Problem Statement: 
Prove that of the $\large{n!}$ terms in a [[Determinants#Definition(Determinants)|determinant]] of order $\large{n}$, exactly $\large{\frac{n!}{2}}$ of them have positive sign while the remaining $\large{\frac{n!}{2}}$ have negative sign. 

#### Solution: 
Proof by induction on $\large{n}$

##### Base Case $\large{n=2}$:
The terms of a second order determinant are: $\large{a_{1,1}a_{2,2}- a_{1,2}a_{2,1}}$, as we can verify visually, $\large{1 = \frac{2!}{2}}$ of them is positive and the other negative. 

##### Induction Step: 
Presume that for a [[Determinants#Definition(Determinants)|determinant]] of order $\large{n}$ exactly $\large{\frac{n!}{2}}$ of them are positive and the remaining $\large{\frac{n!}{2}}$ of them are negative. 
Consider a determinant $\large{D}$ of order $\large{n+1}$. 
By [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]]: 
$$\large{
D = (-1)^{i + 1}a_{i,1}M_{i,1} + (-1)^{i+2}a_{i,2}M_{i,2} + \ldots + (-1)^{i+n}a_{i,n}M_{i,n}
}$$
where $\large{1 \le i \le n}$ is some row number. 
We note that each [[Minors of a Determinant#Definition(Minors)|Minor]] in this expression $\large{M_{i,j}}$ where $\large{j=1,2,\ldots,n}$ is itself a determinant of order $\large{n}$, so by inductive hypothesis they each have exactly $\large{\frac{n!}{2}}$ positive terms and $\large{\frac{n!}{2}}$ negative terms. 
The terms $\large{(-1)^{i,j}a_{i,j}}$ where $\large{j=1,2,\ldots,n}$ are either negative or positive. In either case $\large{(-1)^{i,j}a_{i,j}M_{i,j}}$ consist exactly of $\large{\frac{n!}{2}}$ positive terms and $\large{\frac{n!}{2}}$ negative terms. There are $\large{n}$ such terms in the sum, therefore overall, there are $\large{n\frac{n!}{2} = \frac{(n+1)!}{2}}$ negative terms and $\large{\frac{(n+1)!}{2}}$ positive terms in $\large{D}$ completing the induction. 
