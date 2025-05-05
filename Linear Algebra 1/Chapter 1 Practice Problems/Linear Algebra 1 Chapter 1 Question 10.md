---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q10
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
  ISBN: "978-0-486-63518-7",
  template: {
    name: "source-tbsection-obj",
    version: 1,
    type: "object"
  },
  class-alias: "Lin-Alg-1",
  source-alias: "Lin-Alg-1-Ch1-PP",
  book-title: "Linear Algebra",
  end-page: 30,
  type: "tbsection",
  section-name: "Chapter 1 Practice Problems",
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
Prove that: 
$$\large{
\begin{vmatrix}
1 & 1 & \ldots & 1 \\
x_1 & x_ 2 & \ldots & x_n \\ 
x_1^2 & x_2^2 & \ldots & x_n^2\\
\vdots & \vdots & \ddots & \vdots \\ 
x_1^{n-2} & x_2^{n-2} & \ldots & x_n^{n-2} \\
x_1^n & x_2^n & \ldots & x_n^n 
\end{vmatrix} 
= 
\begin{vmatrix}
1 & 1 & \ldots & 1 \\ 
x_1 & x_2 & \ldots & x_n \\ 
x_1^2 & x_2^2 & \ldots & x_n^2 \\ 
\vdots & \vdots & \ddots & \vdots \\ 
x_1^{n-2} & x_2^{n-2} & \ldots & x_n^{n-2} \\
x_1^{n-1} & x_2^{n-1} & \ldots & x_n^{n-1}
\end{vmatrix} 
\sum_{k=1}^n x_n
}$$
#### Solution: 
Call the Left Hand Side of the asserted equality $\large{A_n}$ 
Call the [[Determinants#Definition(Determinants)|determinant]] in the Right Hand Side of the asserted equality(The [[Vandermonde Determinants#Definition(Vandermonde Determinant)|Vandermonde Determinant]] in the variables $\large{x_1,x_2,\ldots,x_n}$) $\large{V_n}$

We note that all the elements of $\large{A_n}$ are polynomials in $\large{x_1,x_2,\ldots,x_n}$. By the definition of the [[Determinants#Definition(Determinants)|determinant]]:
$$\large{A_n = \sum(-1)^{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}a_{\alpha_1,1}a_{\alpha_2,2}\ldots a_{\alpha_n,n}}$$
So $\large{A_n}$ is a sum of products of polynomials in $\large{x_1,x_2,\ldots,x_n}$ so $\large{A_n}$ is a polynomial in $\large{x_1,x_2,\ldots,x_n}$. 
We also note that the highest degree elements in $\large{A_n}$ are the elements $\large{x_1^n, x_2^n,\ldots, x_n^n}$. Since each term in the sum of the determinant contains exactly one element from each column, it stands that $\large{A_n}$ is of degree $\large{n}$ in each of $\large{x_1,x_2,\ldots,x_n}$.
If each of $\large{x_1,x_2,\ldots,x_{n-1}}$ are set to equal $\large{x_n}$, $\large{A_n=0}$ by [[Anti-symmetry Property of the Determinant#Corollary 1.43.1|Corollary 1.43.1]] since the determinant would contain duplicate columns. 
Since $\large{A_n}$ is a polynomial of degree $\large{n}$ in each of $\large{x_1,x_2,\ldots,x_n}$ It stands that $\large{A_n}$ is of the following form: 
$$\large{
A_n = [\alpha(x_1,x_2,\ldots,x_{n-1})+ x_n\beta(x_1,x_2,\ldots,x_{n-1})]\prod_{k=1}^{n-1}(x_n - x_k)
}$$
Where $\large{\alpha, \beta}$ are polynomials in the variables $\large{x_1,x_2,\ldots,x_{n-1}}$ 
Next we preform [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the $\large{n}$th column of $\large{A_n}$:
$$\large{
A_n = (-1)^{n+1}M_{1,n} + (-1)^{2+n}x_nM_{2,n} + \ldots + (-1)^{2n-1}M_{n-1,n}x_n^{n-2} + (-1)^{2n}M_{n,n}x_n^n
}$$
Where $\large{M_{i,j}}$ represents the [[Minors of a Determinant#Definition(Minors)|Minor]] of $\large{A_n}$ at row $\large{i}$ and column $\large{j}$.
Let $\large{\hat {M}_{i,j}}$ represent the Minor of $\large{V_n}$ at row $\large{i}$ and column $\large{j}$
It is clear that $\large{\hat M_{n,n} = M_{n,n} = V_{n-1}}$  
Expanding $\large{\prod_{k=1}^{n-1}(x_n - x_k)}$ we see that the coefficient of $\large{x_n^{n-1}}$ is $\large{1}$, in other words, $\large{\prod_{k=1}^{n-1} (x_n - x_k)}$ is monic so:
$$\large{\prod_{k=1}^{n-1} (x_n - x_k) = x_n^{n-1} + a_{n-2}x_n^{n-2} + \ldots + a_1x_n + a_0}$$
By applying Vieta's Formula on $\large{a_{n-2}}$ we see that: 
$$\large{
\frac{a_{n-2}}{a_{n-1}} = a_{n-2} = -\sum_{k=1}^{n-1}x_k
}$$
Let $\large{a_{n-3}x_n^{n-3} + \ldots + a_1x_n + a_0}$ be denoted as $\large{\delta(x_1,x_2,\ldots,x_n)}$, then: 
$$\large{\prod_{k=1}^{n-1}(x_n - x_k) = x_n^{n-1} -x_n^{n-2}\sum_{k=1}^{n-1}x_k  + \delta(x_1,x_2,\ldots,x_n)}$$
Substituting this expansion into our previous equation:
$$\large{
\begin{eqnarray}
A_n &=& (\alpha + x_n\beta)(x_n^{n-1} - x_n^{n-2}\sum_{k=1}^{n-1}x_k + \delta) \\
 &=& \alpha x_n^{n-1} -\alpha x_n^{n-2}\sum_{k=1}^{n-1}x_k + \delta\alpha + x_n^n\beta -x_n^{n-1}\beta\sum_{k=1}^{n-1}x_k + x_n\beta\delta
\end{eqnarray}
}$$
We recognise that: 
$\large{\alpha x_n^{n-1}}$ is of degree $\large{n-1}$ in $\large{x_n}$,
$-\alpha x_n^{n-2}\sum_{k=1}^{n-1}x_k$ is of degree $\large{\lt n - 1}$ in $\large{x_n}$
$\large{\alpha\delta}$ is of degree $\large{\lt n-1}$ in $\large{x_n}$ (as $\large{\delta}$ is degree $\large{n-3}$)
$\large{x_n^n\beta}$ is of degree $\large{n}$ in $\large{x_n}$ 
$\large{-x_n^{n-1}\beta \sum_{k=1}^{n-1}x_k}$ is of degree $\large{n-1}$ on $\large{x_n}$
and $\large{x_n\delta\beta}$ is of degree $\large{\lt n-1}$ in $\large{x_n}$

More specifically:
$\large{x_n^n \beta}$ expresses every degree $\large{n}$ term in $\large{x_n}$ in $\large{A_n}$
$\large{x_n^{n-1}\alpha -x_n^{n-1}\beta \sum_{k=1}^{n-1}x_k}$ consists of every degree $\large{n-1}$ term in $\large{x_n}$ in $\large{A_n}$ 

Matching powers with the cofactor expansion form of $\large{A_n}$:
$$\large{\begin{eqnarray}
x_n^n\beta = (-1)^{2n}M_{n,n}x_n^n \\
\alpha x_n^{n-1} -x_n^{n-1}\beta\sum_{k=1}^{n-1} = 0
\end{eqnarray}
}$$

If $\large{x_n^n = 0}$ then $\large{A_n = 0}$ and $\large{V_n = 0}$ so the asserted equality would trivially hold.
Suppose $\large{x_n^n \ne 0 }$, then: 
$$\large{\beta(x_1,x_2,\ldots,x_{n-1}) = M_{n,n}(-1)^{2n} = \hat M_{n,n} = V_{n-1}}$$
Substituting this into the other equality: 
$$\large{
\begin{eqnarray}
x_n^{n-1}\alpha(x_1,x_2,\ldots,x_{n-1}) - x_n^{n-1}V_{n-1}\sum_{k=1}^{n-1}x_k = 0 \\ 
\alpha(x_1,x_2,\ldots,x_{n-1})  =V_{n-1}\sum_{k=0}^{n-1}x_k
\end{eqnarray}
}$$
Substituting these findings into our original equation for $\large{A_n}$:
$$\large{
\begin{eqnarray}
A_n &=& [V_{n-1}(\sum_{k=1}^{n-1}x_k) + x_nV_{n-1}]\prod_{k=1}^{n-1}(x_n - x_k) \\ 
&=& V_{n-1}[\sum_{k=1}^{n-1}x_k + x_n]\prod_{k=1}^{n-1}(x_n - x_k) \\ 
&=& V_{n-1}\prod_{k=1}^{n-1}(x_n - x_k)(\sum_{k=1}^nx_k) \\ 
&=& V_n\sum_{k=1}^nx_k
\end{eqnarray}
}$$
As Asserted, with the last step following from the recursive definition of the [[Vandermonde Determinants#Proof|Vandermonde Determinant]].

#### Alternative Solution: 
Call the Left Hand Side of the asserted equality $\large{A_n}$ 
Call the [[Determinants#Definition(Determinants)|determinant]] in the Right Hand Side of the asserted equality(The [[Vandermonde Determinants#Definition(Vandermonde Determinant)|Vandermonde Determinant]] in the variables $\large{x_1,x_2,\ldots,x_n}$) $\large{V_n}$
We note that all the elements of $\large{A_n}$ are polynomials in $\large{x_1,x_2,\ldots,x_n}$. By the definition of the [[Determinants#Definition(Determinants)|determinant]]:
$$\large{A_n = \sum(-1)^{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}a_{\alpha_1,1}a_{\alpha_2,2}\ldots a_{\alpha_n,n}}$$
So $\large{A_n}$ is a sum of products of polynomials in $\large{x_1,x_2,\ldots,x_n}$ so $\large{A_n}$ is a polynomial in $\large{x_1,x_2,\ldots,x_n}$. 

Swapping the columns $\large{i, j, i\ne j}$ in $\large{A_n(x_1,x_2,\ldots,x_i,x_j,\ldots, x_n)}$ results in $\large{-A_n(x_1,x_2,\ldots,x_j,x_i,\ldots,x_n)}$ by [[Anti-symmetry Property of the Determinant#Theorem 1.42 (The Anti-Symmetry Property in Columns)|The Anti Symmetry Property]]. Since we know $\large{A_n}$ is a polynomial in $\large{x_1,x_2,\ldots,x_n}$ this would mean that $\large{A_n}$ is alternating. 
Since $\large{A_n}$ is an alternating polynomial we know that the [[Vandermonde Determinants#Theorem 1.55c|Vandermonde Polynomial]] is a common factor of $\large{A_n}$: 
$$\large{A_n = \alpha(x_1,x_2,\ldots,x_n)V_n}$$
Where $\large{\alpha({x_1,x_2,\ldots,x_n})}$ is some polynomial. 
Since the product of $\large{\alpha}$ and $\large{V_n}$ is alternating, and $\large{V_n}$ is alternating this would mean that $\large{\alpha}$ must be symmetric. 

We note that the highest degree elements in $\large{A_n}$ are the elements $\large{x_1^n, x_2^n,\ldots, x_n^n}$. Since each term in the sum of the determinant contains exactly one element from each column, it stands that $\large{A_n}$ is of degree $\large{n}$ in each of $\large{x_1,x_2,\ldots,x_n}$.
Since $\large{V_{n-1}}$ is a degree $\large{n-1}$ polynomial in each of $\large{x_1,x_2,\ldots,x_n}$ and $\large{A_n}$ is a degree $\large{n}$ polynomial in each of $\large{x_1,x_2,\ldots,x_n}$ we know that $\large{\alpha}(x_1,x_2,\ldots,x_n)$ is of degree $\large{1}$ in each of $\large{x_1,x_2,\ldots,x_n}$.
The only symmetric polynomial of degree $\large{1}$ in each of $\large{x_1,x_2,\ldots,x_n}$ is of the form 
$$\large{
\begin{eqnarray}
\alpha &=& C(x_1 + x_2 + \ldots + x_n) \\ 
&=& C\sum_{k=1}^{n}x_n
\end{eqnarray}
}
$$
Where $\large{C}$ is some constant invariant to $\large{x_1,x_2,\ldots,x_n}$.
So: 
$$\large{
A_n = C(\sum_{k=1}^{n}x_k)V_n
}$$

Next we preform [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the $\large{n}$th column of $\large{A_n}$:
$$\large{
A_n = (-1)^{n+1}M_{1,n} + (-1)^{2+n}x_nM_{2,n} + \ldots + (-1)^{2n-1}M_{n-1,n}x_n^{n-2} + (-1)^{2n}M_{n,n}x_n^n
}$$
Where $\large{M_{i,j}}$ represents the [[Minors of a Determinant#Definition(Minors)|Minor]] of $\large{A_n}$ at row $\large{i}$ and column $\large{j}$.
Let $\large{\hat {M}_{i,j}}$ represent the Minor of $\large{V_n}$ at row $\large{i}$ and column $\large{j}$
It is clear that $\large{\hat M_{n,n} = M_{n,n} = V_{n-1}}$
We note that the term $\large{(-1)^{2n}M_{n,n}x_n^n = V_{n-1}x_n^n}$ contains all terms of degree $\large{n}$ in $\large{x_n}$

From the [[Vandermonde Determinants#Proof|Recursive Definition of the Vandermonde Determinant]]:
$$\large{V_n = V_{n-1}\prod^{n-1}_{k=1}(x_n - x_k)}$$
Expanding $\large{\prod_{k=1}^{n-1}(x_n - x_k)}$ we see that the coefficient of $\large{x_n^{n-1}}$ is $\large{1}$, in other words, $\large{\prod_{k=1}^{n-1} (x_n - x_k)}$ is monic so:
$$\large{\prod_{k=1}^{n-1}(x_n - x_k) = x_n^{n-1}  + \delta(x_1,x_2,\ldots,x_n)}$$
where $\large{\delta}$ is some polynomial in $\large{x_1,x_2,\ldots,x_n}$ which is of degree $\large{n-2}$ in $\large{x_n}$.
Substituting this form: 
$$\large{
\begin{eqnarray}
A_n &=& C(\sum_{k=1}^{n}x_k)V_{n-1}(x_n^{n-1} + \delta) \\ 
&=&Cx_nV_{n-1}x_{n}^{n-1} + C(\sum_{k=1}^{n-1}x_k)V_{n-1}\delta
\end{eqnarray}
}$$
Note that $\large{Cx_nV_{n-1}x_n^{n-1} = Cx_n^nV_{n-1}}$ contains all degree $\large{n}$ terms in $\large{x_n}$. 
Matching powers with the form of $\large{A_n}$ obtained through cofactor expansion: 
$$\large{
Cx_n^nV_{n-1}= V_{n-1}x_n^n
}$$
Recognising that in the case of $\large{V_{n-1} = 0}$ and $\large{x_n^n = 0}$ the equality asserted trivially holds this condition reduces to: 
$$\large{C= 1}$$
Meaning that: 
$$\large{
A_n = V_n\sum_{k=1}^nx_k
}$$
as asserted. 