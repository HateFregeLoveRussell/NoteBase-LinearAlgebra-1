---
type: Academic
tags:
alias: Lin-Alg-1-LinearCombinationOfColumnsOfADeterminant
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
  source-alias: "Lin-Alg-1-Ch1-Sec1-9",
  type: "tbsection",
  section-name: "Linear Dependence Between Columns",
  ISBN: "978-0-486-63518-7",
  end-page: 28,
  book-title: "Linear Algebra",
  start-page: 23,
  template: {
    type: "object",
    version: 1,
    name: "source-tbsection-obj"
  },
  class-alias: "Lin-Alg-1"
}
relationship: {name: standard-relationship-obj, version: 1}
friends: 
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

#### Definition(Linear Combinations):
Consider a column of $\large{n}$ entries:  $\large{C = \begin{vmatrix}c_1 \\ c_2 \\ \vdots \\ c_n\end{vmatrix}}$. If this column is a result of summing the columns: $\large{A_1 = \begin{vmatrix} a_{1,1} \\ a_{2,1} \\ \vdots \\ a_{n,1}\end{vmatrix}, A_2 = \begin{vmatrix} a_{1,2} \\ a_{2,2} \\ \vdots \\ a_{n,2} \end{vmatrix}, \ldots, A_m = \begin{vmatrix} a_{1,m} \\ a_{2,m} \\ \vdots \\ a_{n,m} \end{vmatrix} }$ scaled by the [[Number Fields#Definition (Number Fields)|numbers]] $\large{\lambda_1, \lambda_2, \ldots, \lambda_m}$, or in other words if $$\large{
\lambda_1 A_1 + \lambda_2 A_2 + \ldots + \lambda_m A_m = C
}$$ we say that the column $\large{C}$ (which itself we treat as a non-square [[Square Matrices#Definition (Square Matrix)|Matrix]]) is a **==Linear Combination of==** the columns $\large{A_1,A_2,\ldots,A_m}$ and the numbers $\large{\lambda_1,\lambda_2, \ldots, \lambda_m}$.

##### Remark: 
Two special cases of the above relation is the **==sum==** of the columns $\large{A_1,A_2,\ldots,A_m}$ when $\large{\lambda_1 = 0, \lambda_2 = 0, \ldots, \lambda_m = 0 }$,
And the **==product==** of the column $\large{A_1}$ and the number $\large{\lambda_1}$ when $\large{m=1}$.

#### Theorem 1.91: 
If one of the columns of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of its other columns then $\large{D = 0}$.

##### Proof: 
Suppose that column $\large{q}$ in $\large{D}$ is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the remaining columns with the [[Number Fields#Definition (Number Fields)|numbers]] $\large{\lambda_1,\lambda_2, \ldots, \lambda_{q-1}, \lambda_{q+1}, \ldots \lambda_n}$ where $\large{n}$ denotes the [[Square Matrices#Definition (Square Matrix)|order]] of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$.
Then by the [[The Linearity Property of Determinants#Theorem 1.44b (Linearity Property of Multiple Variables in Columns)|linearity property of the determinant]] we can subtract from the column $\large{q}$ the sum of every other column scaled by the values $\large{\lambda_1,\lambda_2, \ldots, \lambda_{q-1}, \lambda_{q+1}, \ldots \lambda_n}$ respectively. This would naturally yield a column of zeros at the position $\large{q}$. 
Then by [[The Linearity Property of Determinants#Corollary 1.46|Corollary 1.46]] since the determinant $\large{D}$ contains a column of zeros its value is zero, hence $\large{D = 0}$.

#### Theorem 1.94: 
If a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ is equal to zero, then it has at least one column which is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the other columns of the determinant.

##### Proof: 
Consider the [[Matrix Rank#Definition (Matrix Rank)|rank]] of the [[Determinants#Definition(Determinants)|determinant]] $\large{r}$. If $\large{r = n}$ ($\large{n}$ being the [[Determinants#Definition(Determinants)|order]] of $\large{D}$) then $\large{D \ne 0}$ as $\large{D}$ is the only [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor of Order]] $\large{n}$ in $\large{D}$ and if $\large{r = n}$ this minor must be non-zero. 
So $\large{r \lt n}$. This means that after identifying the $\large{r}$ [[Matrix Rank#Definition (Matrix Rank)|Basis Columns]] of $\large{D}$ there must be at least one column which is not a basis column in $\large{D}$.
By the [[Matrix Rank#Theorem 1.93 (Basis Minor Theorem)|Basis Minor Theorem]] then, this remaining column must be a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the Basis Columns, which means it is a linear combination of all other columns in $\large{D}$ (we assign a weight of zero to columns which are not the basis column in the expression).

#### Theorem 1.94.1: 
The [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ is equal to zero if and only if one of its columns is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the others. 

##### Proof: 
(=>):
See [[Linear Combinations of Columns of a Determinant#Theorem 1.94|Theorem 1.94]].
(<=):
See [[Linear Combinations of Columns of a Determinant#Theorem 1.91|Theorem 1.91]].