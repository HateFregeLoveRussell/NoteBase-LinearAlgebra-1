---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q5
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
Use the [[The Linearity Property of Determinants|Linearity Property]] of the Determinant to compute 
$$\large{
\Delta = 
\begin{vmatrix} 
am + bp & an + bq \\ 
cm + dp & cn+ dq
\end{vmatrix}
}$$

#### Solution
The first column of $\large{\Delta}$ can be decomposed into: 
$$\large{
\begin{vmatrix} am+bp \\ cm+dq \end{vmatrix} = 
m \begin{vmatrix}a \\ c\end{vmatrix} + p \begin{vmatrix} b \\ d\end{vmatrix} 
}$$
Hence by the use of the [[The Linearity Property of Determinants#Theorem 1.44a (Linearity Property of Determinants in Columns)|Linearity Property of the Determinant in Columns (Theorem 1.44a)]]:
$$\large{\Delta = 
m\begin{vmatrix}
a & an+bq \\ 
c & cn+dq
\end{vmatrix} + 
p\begin{vmatrix}b & an+ bq \\
d  & cn+dq\end{vmatrix}}$$
We note that the second column of $\large{\Delta}$ in both its terms can be decomposed into:
$$\large{
\begin{vmatrix}an+ bq \\ cn + dq\end{vmatrix} = n\begin{vmatrix}a \\c\end{vmatrix} + q\begin{vmatrix}b \\ d \end{vmatrix}
}$$
Hence by the use of [[The Linearity Property of Determinants#Theorem 1.44a (Linearity Property of Determinants in Columns)|Theorem 1.44a]] again: 
$$\large{
\Delta = m( n\begin{vmatrix} a & c \\ a & c\end{vmatrix} + q \begin{vmatrix}a & b \\ c & d \end{vmatrix}) + p(n\begin{vmatrix}b & a \\ d & c \end{vmatrix} + q\begin{vmatrix} b & b \\ d & d \end{vmatrix})
}$$
Now we can use [[Anti-symmetry Property of the Determinant#Corollary 1.43.1|Corollary 1.43.1]] to eliminate the [[Determinants#Definition(Determinants)|determinants]] with duplicate columns in $\large{\Delta}$: 
$$\large{
\Delta= m(n*0  + q\begin{vmatrix}a & b \\ c & d \end{vmatrix}) + p(n \begin{vmatrix} b & a \\ d & c \end{vmatrix}  + q*0) 
}$$
Which then simplifies to:
$$\large{\Delta = mq\begin{vmatrix}a & b \\ c & d \end{vmatrix} + pn\begin{vmatrix} b & a \\ d & c\end{vmatrix}}$$
We now use [[Anti-symmetry Property of the Determinant#Lemma 1.42.1 (Anti-Symmetry Property In Consecutive Columns)|Lemma 1.42.1]] to switch the columns of the second term: 
$$\large{
\Delta = mq\begin{vmatrix}a & b \\ c & d \end{vmatrix} - pn \begin{vmatrix} a & b \\ c & d \end{vmatrix}
}$$
We can then collect like terms: 
$$\large{\Delta = (mq- pn)\begin{vmatrix}a & b \\ c & d\end{vmatrix}}$$
Evaluating the determinant: 
$$\large{\Delta = (mq-pn)(ad- bc)}$$
