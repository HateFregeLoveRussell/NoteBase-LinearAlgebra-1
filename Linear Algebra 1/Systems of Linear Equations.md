---
type: Academic
tags:
alias: Lin-Alg-1-SystemsOfLinearEquations
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
source: [{
	  section-name: "Problems of the Theory of Systems of Linear Equations",
	  start-page: 3,
	  type: "tbsection",
	  template: {
	    name: "source-tbsection-obj",
	    version: 1,
	    type: "object"
	  },
	  class-alias: "Lin-Alg-1",
	  source-alias: "Lin-Alg-1-Ch1-Sec1-2",
	  ISBN: "978-0-486-63518-7",
	  end-page: 5,
	  book-title: "Linear Algebra"},
	  
	  {
	  ISBN: "978-0-486-63518-7",
	  section-name: "Cramers Rule",
	  type: "tbsection",
	  class-alias: "Lin-Alg-1",
	  end-page: 20,
	  source-alias: "Lin-Alg-1-Ch1-Sec1-7",
	  template: {
	    type: "object",
	    name: "source-tbsection-obj",
	    version: 1},
		start-page: 18, 
		book-title: "Linear Algebra"
	}]  
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

#### Definition (Systems of Linear Equations):
By a **==System of Linear Equations==** we mean a set of equations of the form 
$$\large{
\begin{eqnarray}
a_{11}x_1 + a_{12}x_2 + \ldots + a_{1n}x_n &=& b_1 \\
a_{21}x_1 + a_{22}x_2  + \ldots + a_{2n}x_n &=& b_2 \\
  \ldots \\
a_{k1}x_1 + a_{k2}x_2 + \ldots + a_{kn}x_n &=& b_k
\end{eqnarray}
}
$$
Here $\large{x_1,x_2,\ldots, x_n \in K}$ for some [[Number Fields#Definition (Number Fields)|number field]] $\large{K}$ are called the **==unknowns==**.
There are $\large{n}$ unknowns and $\large{k}$ equations in a given system of linear equations.
The quantities $\large{a_{11}, a_{12}, \ldots , a_{kn} \in K }$ are called the **==coefficients==** of the system. 
The first number index of the coefficient designates which equation in the set it belongs to and the second index designates its unknown.
The quantities $\large{b_1, b_2, \ldots, b_k \in K}$ are called the **==constant terms==** of the system. And like the coefficients are assumed to be known.

#### Definition (Solution to a System of Linear Equations): 
For a given [[#Definition (Systems of Linear Equations)|System of Linear Equations]], we call the numbers $\large{c_1, c_2, \ldots, c_n \in K}$  for which when substituted in place of the system's unknowns all equations become identities a **==solution==** to the system. 
Not every system has a solution, and not every system has exactly one solution. 
When multiple solutions exist for a given system we distinguish between them through the following notation: $\large{c_1^{(1)},c_2^{(1)}, \ldots, c_n^{(1)}}$ , $\large{c_1^{(2)}, c_2^{(2)}, \ldots , c_n^{(2)}}$ and so on. 

We call systems which have at least one solution **==compatible==**.
When no solutions exist for a given system we call the system **==incompatible==**. 
When a compatible system has only a single unique solution we say the system is **==determinant==**.
When a compatible system has more than a single unique solution we say that the system is **==indeterminant==**.

##### Example - Compatible but Indeterminant System: 
Consider the [[#Definition (Systems of Linear Equations)|System of Linear Equations]] below: 
$$\large{ \begin{eqnarray}
2x_1 + 3x_2 &=& 0 \\
4x_1 + 6x_2 &=& 0
\end{eqnarray}
}
$$
The system is both Indeterminant and Compatible as it has the solutions: 
$\large{c_1^{(1)} = c_2^{(1)}= 0}$ and $\large{c_1^{(2)}=3}$ $\large{ c_2^{(2)}= -2}$.
There is also infinitely many other solutions to this system.

#### Definition (Coefficient Matrix):
When the number of equations match the number of unknowns, 
$$\large \begin{eqnarray} 
a_{1,1}x_1 + a_{1,2}x_2 + \ldots + a_{1,n}x_n &=& b_1 \\
a_{2,1}x_1 + a_{2,2}x_2 + \ldots + a_{2,n}x_n &=& b_2 \\
\vdots \\
a_{n,1}x_1 + a_{n,2}x_2 + \ldots + a_{n,n}x_n &=& b_n 
\end{eqnarray}$$
the [[Systems of Linear Equations#Definition (Systems of Linear Equations)|coefficients]] of the system can be organised into a [[Square Matrices#Definition (Square Matrix)|square matrix]] $$
\large{
\begin{vmatrix} \begin{vmatrix}
a_{1,1} & a_{1,2} & \ldots & a_{1,n} \\
a_{2,1} & a_{2,2} & \ldots & a_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\ 
a_{n,1} & a_{n,2} & \ldots & a_{n,n}
\end{vmatrix}\end{vmatrix}
}$$
This matrix is called the **==coefficient matrix==** of the system. 
