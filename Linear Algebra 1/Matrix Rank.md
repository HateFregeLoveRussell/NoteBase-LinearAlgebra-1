---
type: Academic
tags:
alias: Lin-ALg-1-MatrixRank
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
#### Definition (Matrix Rank): 
Suppose that we  have a (not necessarily square) [[Square Matrices#Definition (Square Matrix)|matrix]] $$\large{A =\begin{vmatrix}\begin{vmatrix}
a_{1,1} & a_{1,2} & \ldots & a_{1,m} \\ 
a_{2,1} & a_{2,2} & \ldots & a_{2,m} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
a_{n,1} & a_{n,2} & \ldots & a_{n,m}
\end{vmatrix}\end{vmatrix}}$$
with $\large{n}$ rows and $\large{m}$ columns. 

We assign to such a matrix an integer $\large{r}$ called the matrix **==rank==** based on the following rules: 

If $\large{A}$ is entirely composed of zeros we say that $\large{r = 0}$
Otherwise we assign $\large{r}$ as follows: 
$\large{r}$ is the positive integer $\large{r \le \min(n,m)}$ for which there exists a [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor of order ]]$\large{r}$ in $\large{A}$ which is non-zero but any Minor of order $\large{r+1}$ in $\large{A}$ (if existing) is zero.

This minor of order $\large{r}$ in the matrix $\large{A}$(If existing) is called the **==Basis Minor==** of the matrix, a matrix $\large{A}$ can have multiple basis minors.If no suitable minor exists it matrix is said to have no basis minor.

The columns which define the basis minor are called the **==Basis Columns==** of the matrix $\large{A}$. 

#### Theorem 1.93 (Basis Minor Theorem): 
Any column of a (not necessarily square) [[Square Matrices#Definition (Square Matrix)|Matrix]] $\large{A}$ is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|linear combination]] of its [[Matrix Rank#Definition (Matrix Rank)|Basis Columns]].

##### Proof:
###### Case I: $\large{r = 0}$
Suppose that the [[Matrix Rank#Definition (Matrix Rank)|rank]] of $\large{A}$ is zero. Then every column, is equal to any other column, meaning that every column is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the remaining columns.

###### Case II: $\large{r \gt 0}$
Denote the [[Matrix Rank#Definition (Matrix Rank)|Basis Minor]] of $\large{A}$ as: 
$$\large{M_B = M_{j_1,j_2,\ldots,j_r}^{i_1,i_2,\ldots,i_r}= \begin{vmatrix}
a_{1,1} & a_{1,2} & \ldots & a_{1,r} \\
a_{2,1} & a_{2,2} & \ldots & a_{2,r} \\ 
\vdots & \vdots & \ddots & \vdots \\
a_{r,1} & a_{r,2} & \ldots & a_{r,r} 
\end{vmatrix}}$$
Suppose that $\large{s}$ is some integer such that $\large{1 \le s \le m}$ with $\large{m}$ being the number of columns in $\large{A}$ 
Suppose that $\large{k}$ is some integer such that $\large{1 \le k \le n}$ with $\large{n}$ being the number of rows in $\large{A}$.
Henceforth when elements of the form $\large{a_{i,s}}$ appear, if $\large{i = 1,2,\ldots,r}$ we assume they are referencing the row in $\large{M_B}$, otherwise we assume the row is in reference to $\large{A}$. The column in $\large{a_{i,s}}$ follows the same rules. 
Similarly when elements of the form $\large{a_{k,j}}$ appear, if $\large{j =1,2,\ldots,r}$ we assume the column is in $\large{M_B}$ coordinates otherwise we say they are in reference to $\large{A}$. The row in $\large{a_{k,j}}$ follow the same rules.
So $\large{a_{3,s}}$ is $\large{a_{i_3, j_3}}$ if $\large{s = 3}$ and $\large{a_{i_3, 12}}$ if $\large{s=12 \not \in \{j_1,j_2,\ldots,j_r\}}$

Now consider the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ constructed as thus: 
$$\large{
D= \begin{vmatrix} 
a_{1,1} & a_{1,2} & \ldots & a_{1,r} & a_{1,s} \\
a_{2,1} & a_{2,2} & \ldots & a_{2,r} & a_{2,s} \\
\vdots  & \vdots & \ddots & \vdots & \vdots \\ 
a_{r,1} & a_{r,2} & \ldots & a_{r,r} & a_{r,s} \\ 
a_{k,1} & a_{k,2} & \ldots & a_{k,r} & a_{k,s}
 \end{vmatrix}
}$$
In other words $\large{D = M_{j_1,j_2,\ldots,j_r,s}^{i_1,i_2,\ldots,i_r,k}}$.
Now we will show that $\large{D = 0}$.
If $\large{k \in \{i_1,i_2,\ldots, i_r\}}$ or $\large{s \in \{j_1,j_2,\ldots,j_r\}}$ then $\large{D =0 }$ as by the [[Anti-symmetry Property of the Determinant#Corollary 1.43.1|Anti Symmetry Property of Determinants in Columns]] and the [[Anti-symmetry Property of the Determinant#Corollary 1.43.2|The Anti-Symmetry Property of Determinants in Rows]] respectively a determinant with two identical columns or rows is equal to zero. 
if $\large{k \not \in \{i_1,i_2,\ldots,i_r\}}$ and $\large{s \not \in \{j_1,j_2,\ldots,j_r\}}$ then $\large{D = 0}$ as then the determinant $\large{D}$ would be some [[Minors of Arbitrary Order#Definition (Minor of Order k)|Minor of order]] $\large{r+1}$ in $\large{D}$ and by the definition of [[Matrix Rank#Definition (Matrix Rank)|Matrix Rank]] $\large{D}$ would have to be equal to zero.
So $\large{D = 0}$ for whatever value of $\large{s}$ and $\large{k}$.
Now preform [[Cofactor of a Determinant#Theorem 1.51|Cofactor Expansion]] on the determinant $\large{D}$ with respect to the last row: 
$$\large{
D = a_{k,1}A_{k,1}(D) + a_{k,2}A_{k,2}(D) + \ldots + a_{k,r}A_{k,r}(D) + a_{k,s}A_{k,s}(D) = 0 
}$$
Where $\large{A_{k,1}(D), A_{k,2}(D), \ldots, A_{k,r}(D) , A_{k,s}(D)}$ represent the respective [[Cofactor of a Determinant#Definition(Cofactors)|Cofactors]] of $\large{D}$
Note that $\large{A_{k,1}(D), A_{k,2}(D), \ldots, A_{k,r}(D) , A_{k,s}(D)}$ do not depend on the variable $\large{k}$ so we will denote them using:
$\large{A_{k,1}(D) = c_1, A_{k,2} = c_2, \ldots, A_{k,r} =c_r , A_{k,s} = c_s}$ 
Setting $\large{k = 1,2,\ldots, n}$ we obtain a [[Systems of Linear Equations#Definition (Systems of Linear Equations)|system of ]]$\large{n}$ identities:
$$\large{ \begin{eqnarray}
c_1a_{1,1} + c_2a_{1,2} + &\ldots& + c_ra_{1,r}+ c_sa_{1,s} = 0 \\
c_2a_{2,1} + c_2a_{2,2} + &\ldots& + c_r a_{2,r} + c_s a_{2,s} = 0 \\
&\vdots& \\ 
c_1 a_{n,1} + c_2a_{n,2} + &\ldots& + c_ra_{n,r} + c_sa_{n,s} = 0 
\end{eqnarray}
}$$
we note that $\large{c_s = A_{k,s}(D) \ne 0}$ as $\large{A_{k,s}(D) = M_B}$, the Basis Minor of $\large{A}$.
Then, dividing by $\large{c_s}$ from both sides of each identity, and then substituting: $\large{\lambda_j = \frac{-c_j}{c_s}}$ and then rearranging we get the system: 
$$\large{\begin{eqnarray}
a_{1,s} = \lambda_{1}a_{1,1} + \lambda_2a_{1,2} + &\ldots& + \lambda_r a_{1,r} \\
a_{2,s} = \lambda_1a_{2,1} + \lambda_2a_{2,2} + &\ldots& + \lambda_ra_{2,r} \\
&\vdots& \\ 
a_{n,s} = \lambda_1a_{n,1} + \lambda_2a_{n,2} + &\ldots& + \lambda_ra_{n,r}
\end{eqnarray}}$$
or in other words an arbitrary column (indexed by $\large{s}$) of $\large{A}$ is a [[Linear Combinations of Columns of a Determinant#Definition(Linear Combinations)|Linear Combination]] of the basis columns of $\large{A}$ and the numbers $\large{\lambda_1, \lambda_2, \ldots, \lambda_r}$.