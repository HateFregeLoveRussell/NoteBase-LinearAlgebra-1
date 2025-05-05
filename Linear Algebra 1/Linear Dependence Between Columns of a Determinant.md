---
type: Academic
tags:
alias: Lin-Alg-1-LinearDependenceBetweenColumnsOfADeterminant
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
  section-name: "Linear Dependence Between Columns",
  ISBN: "978-0-486-63518-7",
  source-alias: "Lin-Alg-1-Ch1-Sec1-9",
  class-alias: "Lin-Alg-1",
  end-page: 28,
  book-title: "Linear Algebra",
  template: {
    type: "object",
    version: 1,
    name: "source-tbsection-obj"
  },
  start-page: 23
}
relationship: {name: standard-relationship-obj, version: 1}
friends: [[Linear Combinations of Columns of a Determinant]]
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
#### Definition (Linear Dependence): 
If a column, entirely composed of zeros (called the **==zero-column==**) is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of $\large{m}$ columns $\large{A_1,A_2,\ldots,A_m}$ in such a way that not every number in the combination $\large{\lambda_1,\lambda_2,\ldots, \lambda_m}$ is equal to zero. The columns $\large{A_1,A_2,\ldots,A_m}$ are said to be **==Linearly Dependent==**.
In other words the columns $\large{A_1,A_2,\ldots,A_m}$ are said to be linearly dependent if 
$$\large{
\lambda_1A_1 + \lambda_2A_2 + \ldots + \lambda_m A_m = 0
}$$
Where the zero on the right hand side denotes the zero-column.

##### Example: 
Consider: 
$$\large{
A_1 = \begin{vmatrix} 1 \\ 2 \\ 3 \\ 4\end{vmatrix}, \\
A_2 = \begin{vmatrix} 2 \\ 4 \\ 6 \\ 8\end{vmatrix}, \\
A_3 = \begin{vmatrix} 1 \\ 1 \\ 1 \\ 1\end{vmatrix} \\
}$$
These columns are [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Dependent]] as: 
$$\large{
2A_1 - 1A_2 + 0A_3 = 0
}
$$

#### Theorem 1.95: 
The columns $\large{A_1,A_2,\ldots,A_m}$ are [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Dependent]] if and only if one of the columns is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the others. 
##### Proof: 
(=>)
Suppose that one of the columns $\large{A_1,A_2,\ldots,A_m}$ is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|linear combination]] of the others. Say $\large{A_m}$. In other words: 
$$\large{
A_m = \lambda_1A_1 +\lambda_2A_2 + \ldots + \lambda_mA_m
}
$$
Then, rearranging the equality, we arrive at the equivalent equality: 
$$\large{
\lambda_1 A_1 + \lambda_2 A_2 + \ldots + \lambda_{m-1}A_{m-1} - A_m = 0
}
$$
Since one of the coefficients in the expression is $\large{-1 \ne 0}$ we know that $\large{A_1,A_2,\ldots,A_m}$ are [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Dependent]].
(<=)
Suppose that $\large{A_1,A_2,\ldots,A_m}$ are [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Dependent]] then, 
$$\large{\lambda_1 A_1 + \lambda_2 A_2 + \ldots + \lambda_{m}A_{m} = 0}$$where at least one of $\large{\lambda_1,\lambda_2, \ldots, \lambda_m}$ are non-zero (Say $\large{\lambda_m}$).
Then divide both sides of the equality by $\large{\lambda_m}$ and rearranging we see that: 
$$\large{A_m = \frac{-\lambda_1}{\lambda_m}A_1 + \frac{-\lambda_2}{\lambda_m}A_2 + \ldots + \frac{-\lambda_{m-1}}{\lambda_m}A_{m-1}}$$
In other words one of the columns in $\large{A_1,A_2,\ldots,A_m}$ is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the others. 

#### Theorem 1.96: 
The [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ is equal to zero, if and only if there is a [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|linear dependence]] between the columns of $\large{D}$.

##### Proof: 
From [[Linear Combinations of Columns of a Determinant#Theorem 1.94.1|Theorem 1.94.1]] we know that $\large{D = 0}$ is equivalent to saying one of its columns is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the others. From [[Linear Dependence Between Columns of a Determinant#Theorem 1.95|Theorem 1.95]] we know that one of the columns in $\large{D}$ is a linear combination of the others is equivalent to the columns of $\large{D}$ being [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Dependent]]. So $\large{D= 0}$ iff the columns of $\large{D}$ are Linearly Dependent.  

#### Corollary 1.96.1: 
The [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ is equal to zero if and only if there is a [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linear Dependence]] between the rows of $\large{D}$. 

##### Proof:
Take the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transpose]] of $\large{D}$ and call it $\large{D^\prime}$. From [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Theorem 1.41]] we know that $\large{D = D^\prime}$. Note that the columns in $\large{D}$ are rows in $\large{D^\prime}$. So by [[Linear Dependence Between Columns of a Determinant#Theorem 1.96|Theorem 1.96]] $\large{D^\prime = 0}$ if and only if its rows are [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Dependent]], but $\large{D = D^\prime}$ giving us the desired result.