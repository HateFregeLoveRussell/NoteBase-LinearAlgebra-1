---
type: Academic
tags:
alias: Lin-Alg-1-Vandermonde-Determinants
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
  class-alias: "Lin-Alg-1",
  section-name: "Cofactors And Minors",
  ISBN: "978-0-486-63518-7",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  },
  book-title: "Linear Algebra",
  start-page: 12,
  end-page: 16,
  source-alias: "Lin-Alg-1-Ch1-Sec1-5"
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
#### Definition(Vandermonde Determinant):
The **==Vandermonde Determinant==** of the variables $\large{x_1, x_2, \ldots x_n}$ where $\large{n}$ denotes the order of the [[Determinants#Definition(Determinants)|determinant]], is denoted as $\large{W(x_1,x_2,\ldots,x_n)}$ and has the form: 
$$\large{
W(x_1,x_2,\ldots,x_n) = 
\begin{vmatrix}
1 & 1 & 1 & \ldots & 1 \\
x_1 & x_2 & x_3  & \ldots & x_n \\ 
x_1^2 & x_2^2 & x_3^2 &\ldots & x_n^2 \\ 
\vdots & \vdots & \vdots & \ddots & \vdots \\
x_1^{n-1} & x_2^{n-1} & x_3^{n-1} & \ldots & x_n^{n-1}
\end{vmatrix}
}
$$

#### Theorem 1.55c:
The [[Vandermonde Determinants#Definition(Vandermonde Determinant)|Vandermonde Determinant]] of the variables $\large{x_1,x_2,\ldots, x_n}$ can be computed through the formula: 
$$\large{W(x_1,x_2, \ldots , x_n) = 
\prod_{1 \le i \lt m \le n}(x_m - x_i)}$$
##### Proof: 
First we note that the [[Determinants#Definition(Determinants)|determinant]] is a polynomial of the variables $\large{x_1,x_2,\ldots, x_n}$. As by definition it is the sum of products of different powers of the variables $\large{x_1,x_2,\ldots,x_n}$. 
Additionally we can see that this polynomial is of degree $\large{n-1}$ in $\large{x_n}$ because of the inclusion of the term $\large{x_n^{n-1}}$. 
Secondly we note that if any of the variables $\large{x_1, x_2, \ldots, x_{n-1}}$ are set to equal $\large{x_n}$ the determinant is equal to zero. This is because then it would contain 2 duplicate columns and so by [[Anti-symmetry Property of the Determinant#Corollary 1.43.1|Corollary 1.43.1]] $\large{W(x_1,x_2, \ldots x_n) = 0}$. 
This would mean that the polynomial in question would have $\large{n-1}$ factors im $\large{x_n}$ of $\large{x_1, x_2, \ldots x_{n-1}}$ respectively. 
So, 
$$\large{W(x_1, x_2, \ldots x_n) = a(x_1,x_2,\ldots, x_{n-1})\prod_{k=1}^{n-1}(x_n -x_k)}$$
Where $\large{a(x_1,x_2,\ldots x_{n-1})}$ represents some polynomial in the variables $\large{x_1,x_2, \ldots , x_{n-1}}$. Note that it is not a polynomial in $\large{x_n}$ as we know $\large{W}$ is only a degree $\large{n-1}$ polynomial in $\large{x_n}$ and $\large{\prod_{k=1}^{n-1}(x_n - x_k)}$ is a polynomial of degree $\large{n-1}$ in $\large{x_n}$.
Since $\large{\prod_{k=1}^{n-1}(x_n - x_k)}$ is a polynomial in $\large{x_n}$ of degree $\large{n-1}$ it can be represented through the formula: 
$$\large{\prod_{k=1}^{n-1}(x_n - x_k) = \alpha_{n-1}x_n^{n-1} + \alpha_{n-2}x_n^{n-2} + \ldots + \alpha_1x_n + \alpha_0 }$$
Note that since every term $\large{x_n - x_k}$ is monic then we know $\large{\alpha_{n-1} = 1}$. 
So $$\large{W(x_1,x_2, \ldots x_n ) = ax_n^{n-1} + a\alpha_{n-2}x_n^{n-2} + \ldots + a\alpha_1x_n + a\alpha_0}$$.
Using [[Minors of a Determinant#Theorem 1.53|Theorem 1.53]] we can expand $\large{W(x_1, x_2, \ldots, x_n )}$ with respect to its last column in order to find an alternative representation of the determinant. 
This would yield the equality: 
$$\large{ \begin{eqnarray}
W(x_1,x_2, \ldots, x_n)  &=& M_{1,n} - x_nM_{2,n} + \ldots + (-1)^{2n}x_n^{n-1}M_{n,n} \\ 
&=& M_{1,n} - x_nM_{2,n} + \ldots + x_n^{n-1}M_{n,n}
\end{eqnarray}}$$
We note that the [[Minors of a Determinant#Definition(Minors)|Minor]] $\large{M_{n,n}}$ is identical to $\large{W(x_1,x_2, \ldots, x_{n-1})}$
combining this fact with the latter most equality we get: 
$$\large{
W(x_1,x_2,\ldots,x_n)= M_{1,n} - x_nM_{2,n} + \ldots + x_n^{n-1}W(x_1,x_2,\ldots, x_{n-1})
}$$
Matching powers with our previous expression for $\large{W}$ we see that: 
$$\large{a(x_1,x_2,\ldots,x_{n-1})x_n^{n-1} = x_n^{n-1}W(x_1,x_2, \ldots ,x_{n-1})}$$
or in other words $\large{a(x_1,x_2,\ldots,x_{n-1}) = W(x_1,x_2,\ldots, x_{n-1})}$ 
Back-substituting this result we see that:
$$\large{
\begin{eqnarray}
W(x_1,x_2, \ldots, x_{n}) &=& W(x_1,x_2,\ldots,x_{n-1})\prod_{k=1}^{n-1}(x_n - x_k) \\
W(x_1,x_2,\ldots, x_{n-1}) &=& W(x_1,x_2, \ldots, x_{n-2})\prod_{k=1}^{n-2} (x_{n-1} - x_k) \\
&\vdots& \\ 
W(x_1,x_2) &=& W(x_1)(x_2 - x_1) 
\end{eqnarray}
}$$
Trivially, we see that $\large{W(x_1) = 1}$ so back-substituting the above equalities we get: 
$$\large{W(x_1,x_2, \ldots x_n) = \prod_{1 \le i \lt m \le n}(x_m - x_i)}$$
#### Corollary 1.55.c.1: 
If all of the variables $\large{x_1,x_2,\ldots,x_n}$ are distinct then the [[Vandermonde Determinants#Definition(Vandermonde Determinant)|Vandermonde Determinant]] of the variables cannot be zero. 
$$\large{W(x_1,x_2, \ldots, x_n) \ne 0}$$
##### Proof: 
From [[Vandermonde Determinants#Theorem 1.55c|Theorem 1.55c]] we see that $\large{W(x_1,x_2,\ldots, x_n) = \prod_{1 \le i \lt m \le n}(x_m - x_i)}$. So the determinant can only be equal to zero if and only if $\large{\prod_{1 \le i \lt m \le n} (x_m - x_i) = 0 }$ which is true if and only if there exists some pair of variables in $\large{x_1,x_2, \ldots, x_n}$ which are not distinct. By contrapositive the desired result is found. 
