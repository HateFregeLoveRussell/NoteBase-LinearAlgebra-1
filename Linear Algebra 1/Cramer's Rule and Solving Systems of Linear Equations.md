---
type: Academic
tags:
alias: Lin-Alg-1-CramersRuleAndSolvingSystemsOfLinearEquations
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
  end-page: 20,
  type: "tbsection",
  class-alias: "Lin-Alg-1",
  start-page: 18,
  source-alias: "Lin-Alg-1-Ch1-Sec1-7",
  book-title: "Linear Algebra",
  section-name: "Cramer's Rule",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  }
}
relationship: {name: standard-relationship-obj, version: 1}
friends: 
status: {
  state: 'Completed',
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
#### Theorem 1.71: 
Given a [[Systems of Linear Equations#Definition (Systems of Linear Equations)|System of Linear Equations]] with an equal number of equations and unknowns. If the [[Determinants#Definition(Determinants)|determinant]] of the [[Systems of Linear Equations#Definition (Coefficient Matrix)|Coefficient Matrix]] is non-zero, and the system is [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|Compatible]] then it is also [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|Determinant]].
Furthermore, the (unique) solution of the system can be expressed using $$\large{c_j = \frac{D_j(b_j)}{D}}$$
Where $\large{D}$ represents the determinant of the coefficient matrix, and $\large{D_j(b_j)}$ represents an augmented determinant where the $\large{j\text{th}}$ column of $\large{D}$ is replaced by the [[Systems of Linear Equations#Definition (Systems of Linear Equations)|constant terms]] of the system.

##### Proof:
Suppose that $\large{D \ne 0}$ and that the system is [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|compatible]], then call the solution one of the solutions of the system $\large{c_1, c_2, \ldots, c_n }$. 
Since these terms are solutions to the system we know that $$
\large{
\begin{eqnarray}
a_{1,1}c_1 + a_{1,2}c_2 + \ldots + a_{1,n}c_n &=& b_1 \\
a_{2,1}c_1 + a_{2,2}c_2 + \ldots + a_{2,n}c_n &=& b_2 \\ 
\vdots \\
a_{n,1}c_1 + a_{n,2}c_2 + \ldots + a_{n,n}c_n &=& b_n
\end{eqnarray}
}
$$
Now multiply the first equation by the [[Cofactor of a Determinant#Definition(Cofactors)|cofactor]] of $\large{D}$, $\large{A_{1,1}}$.
Then multiply the second equation by $\large{A_{2,1}}$ and so on. 
Add all the resulting equalities to obtain: 
$$\large{
\begin{eqnarray}
&(a_{1,1}A_{1,1}&+ a_{2,1}A_{2,1} + \ldots + a_{n,1}A_{n,1})+  \\
	&(a_{1,2}A_{1,1}& + a_{2,2}A_{2,1} + \ldots + a_{n,2}A_{n,1})+ \\
	 &\ldots& +\\   
	 &(a_{1,n}A_{1,1}& + a_{2,n}A_{2,1} + \ldots + a_{n,n}A_{n,1})  =\\ 
	 &b_1A_{1,1}& + b_2A_{2,1}+ \ldots + b_n A_{n,1}
\end{eqnarray}
}$$

Through [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]] we recognise the right hand side of our equality as $\large{D_1(b_j)}$. Similarly through [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]] we recognise the first term of the left hand side as $\large{D}c_1$. Through [[Cofactor of a Determinant#Theorem 1.52|Theorem 1.52]] we recognise all other terms as $\large{0}$. 
So we finally get the equality $$\large{c_1D = D_1(b_j)}$$Since we know $\large{D \ne 0}$ we can rearrange to obtain: $$\large{c_1 = \frac{D_1(b_j)}{D}}$$
Without loss of generality we can utilise this method to obtain the general expression of the solution: 
$$\large{c_j = \frac{D_j(b_j)}{D}}$$
Since $\large{D}$ and $\large{D_1(b_j), D_2(b_j), \ldots , D_n(b_j)}$ are uniquely determined, we know that the solution $\large{c_1,c_2, \ldots, c_n}$ is unique and hence the system is [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|determinant.]] 

#### Theorem 1.72:
Given a [[Systems of Linear Equations#Definition (Systems of Linear Equations)|System of Linear Equations]] where the number of equations matches the number of unknowns, and also the [[Determinants#Definition(Determinants)|Determinant]] of the [[Systems of Linear Equations#Definition (Coefficient Matrix)|Coefficient Matrix]] is non-zero. The system is [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|compatible]].

##### Proof: 
Call the [[Determinants#Definition(Determinants)|determinant]] of the [[Systems of Linear Equations#Definition (Coefficient Matrix)|coefficient matrix]] $\large{D}$. 
Call an augmented version of $\large{D}$ where the $\large{j\text{th}}$ column is replaced with the [[Systems of Linear Equations#Definition (Systems of Linear Equations)|constant terms]] $\large{D_j(b)}$. 
Consider the proposed [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|solution]] $\large{c_1, c_2, \ldots, c_n}$ where $\large{c_j = \frac{D_j(b)}{D}}$. 
Substituting $\large{c_1,c_2, \ldots, c_n}$ for the [[Systems of Linear Equations#Definition (Systems of Linear Equations)|unknowns]] $\large{x_1,x_2,\ldots,x_n}$ in the $\large{k\text{th}}$ equation:
$$\large{
a_{k,1}c_1 + a_{k,2}c_2 + \ldots + a_{k,n}c_n = a_{k,1}\frac{D_1(b)}{D} + a_{k,2}\frac{D_2(b)}{D} + \ldots + a_{k,n}\frac{D_n(b)}{D}
}$$
Through repeated use of [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]] we can obtain the equality: 
$$\large{\begin{eqnarray}
a_{k,1}c_1 + a_{k,2}c_2 + \ldots + a_{k,n}c_n = \\ \frac{1}{D}[a_{k,1}(b_1A_{1,1} + b_2A_{2,1} + \ldots +  b_nA_{n,1})  &+&  \\ a_{k,2}(b_1A_{1,2} + b_2 A_{2,2} + \ldots b_nA_{n,2}) &+&  \\ 
\ldots &+& \\ a_{k,n}(b_1A_{1,n} + b_2A_{2,n} + \ldots + b_nA_{n,n})] 
\end{eqnarray}}$$
We can then rearrange terms to get: 
$$\large{\begin{eqnarray}
a_{k,1}c_1 + a_{k,2}c_2 + \ldots + a_{k,n}c_n &=& \\
\frac{1}{D}[b_1(a_{k,1} A_{1,1} + a_{k,2}A_{1,2} + \ldots + a_{k,n}A_{1,n}) &+&  \\ 
b_2(a_{k,1}A_{2,1} + a_{k,2}A_{2,2} + \ldots + a_{k,n}A_{2,n}) &+& \\
\ldots &+& \\
b_n(a_{k,1}A_{n,1} + a_{k,2}A_{n,2} + \ldots + a_{k,n}A_{n,n})]
\end{eqnarray}
}$$
By [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]] and [[Cofactor of a Determinant#Theorem 1.52|Theorem 1.52]] the term next to $\large{b_k}$ is equal to $\large{D}$ while all other terms are equal to $\large{0}$.
Hence, $\large{\frac{1}{D}b_k D = b_k}$ giving us an identity (since $\large{D \ne 0}$) in an arbitrary equation and hence showing that $\large{c_1,c_2, \ldots c_n}$ are an actual [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|solution]] to the system, making it [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|compatible]].

#### Theorem 1.73 (Cramer's Rule): 
Given a [[Systems of Linear Equations#Definition (Systems of Linear Equations)|System of Linear Equations]] where the number of equations match the number of unknowns, where the [[Determinants#Definition(Determinants)|Determinant]] of the [[Systems of Linear Equations#Definition (Coefficient Matrix)|Coefficient Matrix]] is non-zero. 
The system is both [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|compatible]] and [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|determinant]] and the formula of the unique solution of the system is: 
$$\large{c_j = \frac{D_j(b_j)}{D}}$$
Where $\large{D}$ represents the determinant of the coefficient matrix, and $\large{D_j(b_j)}$ represents an augmented determinant where the $\large{j\text{th}}$ column of $\large{D}$ is replaced by the [[Systems of Linear Equations#Definition (Systems of Linear Equations)|constant terms]] of the system.

##### Proof:
By [[Cramer's Rule and Solving Systems of Linear Equations#Theorem 1.72|Theorem 1.72]] the system is [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|compatible]]. By [[Cramer's Rule and Solving Systems of Linear Equations#Theorem 1.71|Theorem 1.71]] the system is [[Systems of Linear Equations#Definition (Solution to a System of Linear Equations)|determinant]]. 

