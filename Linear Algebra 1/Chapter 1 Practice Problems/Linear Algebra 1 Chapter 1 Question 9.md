---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q9
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
Calculate the following $\large{n}$th order [[Determinants#Definition(Determinants)|determinant]]: 
$$\large{
\Delta_n = \begin{vmatrix}x & a & a & \ldots & a& a \\
a & x & a&  \ldots & a & a \\ 
a& a & x & \ldots &a & a \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\ 
a & a & a & \ldots & x & a \\
a& a& a & \ldots & a & x\end{vmatrix} 
}$$
#### Solution 1:
We know that $\large{\Delta_n = \sum (-1)^{N(\alpha_1,\alpha_2,\ldots, \alpha_n)}a_{\alpha_1,1}a_{\alpha_2,2}\ldots a_{\alpha_n,n}}$ By the [[Determinants#Definition(Determinants)|Definition of the Determinant]]. Since every element of $\large{\Delta_n}$ is a polynomial in $\large{a}$ and $\large{x}$ it stands that $\large{\Delta_n}$, being a sum of products of such elements, is itself a polynomial in $\large{x}$ and $\large{a}$.
Subtracting consecutive columns starting at the first column and ending at the column $\large{n-1}$. 
$$\large{
\Delta_n = \begin{vmatrix}
x - a & 0 & 0 & \ldots & 0 &  a \\
a-x & x-a & 0 & \ldots & 0 & a \\
0 & a - x & x-a & \ldots & 0 & a \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & 0 & \ldots & x-a & a \\
0 & 0 & 0 & \ldots & a-x & x
\end{vmatrix}
}$$
If $\large{x = a}$ then clearly $\large{\Delta_n = 0}$ by [[The Linearity Property of Determinants#Corollary 1.46|Corollary 1.46]]. 
Since $\large{\Delta_n}$ is a polynomial this would mean that $\large{\Delta_n}$ is divisible by the factor $\large{x-a}$. 
Then by [[The Linearity Property of Determinants#Theorem 1.44a (Linearity Property of Determinants in Columns)|Theorem 1.44a(The Linearity Property)]]: 
$$\large{\frac{\Delta_n}{x-a} = 
\begin{vmatrix} 
1 & 0 & 0 & \ldots & 0 & a \\
-1 & x-a & 0 & \ldots & 0 & a \\
0 & a-x & x-a & \ldots & 0 & a \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\ 
0 & 0 & 0 & \ldots & x-a & a \\ 
0 & 0& 0 & \ldots & a-x & x
\end{vmatrix}}$$
Repeating this procedure for the remaining $\large{n-2}$ columns we see that:
$$\large{
\frac{\Delta_n}{(x-a)^{n-1}} = \begin{vmatrix}
1 & 0 & 0 & \ldots & 0 & a \\
-1 & 1 & 0  & \ldots & 0 & a \\
0 & -1 & 1 & \ldots & 0 & a \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\ 
0 & 0 & 0 & \ldots & 1 & a \\
0 & 0 & 0 & \ldots & -1 & x
\end{vmatrix}
}$$
Now summing every row from the second row to the $\large{n}$th row to the first row through [[The Linearity Property of Determinants#Theorem 1.47b|Theorem 1.47b]]: 
$$\large{
\frac{\Delta_n}{(x-a)^{n-1}} = 
\begin{vmatrix}
0 & 0 & 0 & \ldots & 0 & x + (n-1)a \\
-1 & 1 & 0 & \ldots & 0 & a \\
0 & -1 & 1 & \ldots & 0 & a \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\ 
0 & 0 & 0 & \ldots & 1 & a \\
0 & 0& 0 & \ldots & -1 & x
\end{vmatrix}
}$$
Using [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the first row: 
$$\large{\Delta_n  = (x-a)^{n-1}(x+ (n-1)a)(-1)^{n+1} 
\begin{vmatrix}
-1 & 1 & 0 & \ldots & 0 \\
0 & -1 & 1 & \ldots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \ldots & 1  \\
0 & 0 & 0 & \ldots & -1
\end{vmatrix}}$$
We recognise the remaining determinant as [[The Triangular Determinant#Definition|Triangular]] and so by [[The Triangular Determinant#Theorem 1.55b|Theorem 1.55b]]: 
$$\large{\begin{eqnarray} 
\Delta_n &=& (x + (n-1)a)(x-a)^{n-1}(-1)^{n+1}(-1)^{n-1} \\ 
&=&(x + (n-1)a)(x-a)^{n-1} (-1)^{2n} \\ 
&=& (x+ (n-1)a)(x-a)^{n-1}
\end{eqnarray}}$$
#### Solution 2: 
Sum all columns from column one to column $\large{n-1}$, to column $\large{n}$ using [[The Linearity Property of Determinants#Theorem 1.47a|Throem 1.47a]]
$$\large{\Delta_n = \begin{vmatrix}
x & a & a & \ldots & a & x+ (n-1)a \\ 
a & x & a & \ldots & a & x + (n-1)a \\ 
a & a & x & \ldots & a & x+ (n-1)a \\ 
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\ 
a & a & a & \ldots & x & x+ (n-1)a \\ 
a& a& a& \ldots & a & x+ (n-1)a
\end{vmatrix}}$$
Subtract consecutive rows from the first row up to row $\large{n-1}$ using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{
\Delta_n = 
\begin{vmatrix} 
x -a & a-x & 0 & \ldots & 0 & 0 \\
0 & x-a & a-x & \ldots & 0 & 0 \\
0 & 0 & x-a & \ldots & 0 & 0 \\ 
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & 0 & \ldots & x-a & 0 \\
a & a & a & \ldots & a & x+(n-1)a
\end{vmatrix}
}$$
Using [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the $\large{n}$th column: 
$$\large{\Delta_n = 
(x + (n-1)a)(-1)^{2n}
\begin{vmatrix}
x- a & a-x & 0 & \ldots&0 \\
0 & x-a & a-x & \ldots & 0 \\ 
0 & 0 & x-a & \ldots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\ 
0 & 0 & 0 & \ldots & x-a 
\end{vmatrix}}$$
We recognise this form of $\large{\Delta_n}$ as [[The Triangular Determinant#Definition|Triangular]] and using [[The Triangular Determinant#Theorem 1.55b|Theorem 1.55b]]: 
$$\large{\begin{eqnarray}
\Delta_n &=& (x+(n-1)a)(-1)^{2n} (x-a)^{n-1} \\ 
&=& (x+ (n-1)a)(x-a)^{n-1}
\end{eqnarray}}$$
