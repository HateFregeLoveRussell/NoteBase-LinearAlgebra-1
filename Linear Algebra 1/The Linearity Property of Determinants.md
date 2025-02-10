---
type: Academic
tags:
alias: Lin-Alg-1-TheLinearityPropertyOfDeterminants
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
    version: 1,
    name: "source-tbsection-obj",
    type: "object"
  },
  start-page: 8,
  section-name: "Properties of Determinants",
  source-alias: "Lin-Alg-1-Ch1-Sec1-4",
  class-alias: "Lin-Alg-1",
  end-page: 12,
  type: "tbsection",
  book-title: "Linear Algebra"
}
relationship: {name: standard-relationship-obj, version: 1}
friends: ["[[Transposition Property of the Determinant]]","[[Anti-symmetry Property of the Determinant]]"]
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
#### Theorem 1.44a (Linearity Property of Determinants in Columns): 
If the $\large{j}$-th column of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ are a linear combination of two columns of numbers(which may or may not belong to the same determinant): 
$$\large{
a_{ij} =\lambda b_i + \mu c_i
}
$$
for every $\large{i = 1,2, \ldots, n}$ where $\large{n}$ is the [[Determinants#Definition(Determinants)|order]] of $\large{D}$ and $\large{\lambda, \mu \in K}$ for the [[Number Fields#Definition (Number Fields)|Field]] $\large{K}$.
Then $\large{D}$ is equivalent to the linear combination of two determinants:
$$\large{D = \lambda D_1 + \mu D_2}$$
Where $\large{D_1}$ and $\large{D_2}$ have the same columns as $\large{D}$ except for column $\large{j}$. In place of this column are the columns $\large{b_1,b_2,\ldots, b_n}$ and $\large{c_1,c_2, \ldots, c_n}$ respectively.
##### Proof: 
Take some arbitrary [[Determinants#Definition(Determinants)|term]] in $\large{D}$: $\large{a_{\alpha_1,1}a_{\alpha_2,2}\ldots a_{\alpha_n,n}}$. 
Then we know that:
$$\large{
\begin{eqnarray}
a_{\alpha_1,1}a_{\alpha_2,2}\ldots a_{\alpha_n,n} &=& a_{\alpha_1,1}a_{\alpha_2,2}\ldots (\lambda b_{\alpha_j} + \mu c_{\alpha_j})\ldots a_{\alpha_n,n} \\
&=& \lambda a_{\alpha_1,1}a_{\alpha_2,2}\ldots b_{\alpha_j}\ldots a_{\alpha_n,n} + \mu a_{\alpha_1,1}a_{\alpha_2,2}\ldots c_{\alpha_j}\ldots a_{\alpha_n,n}
\end{eqnarray}
}$$
Summing over every term in the determinant $\large{D}$ while using the signs present in the determinant we get the same terms as: $\large{\lambda D_1 + \mu D_2}$

##### Remark: 
An alternative, but convenient alternate notation for this statement: 
$$\large{
D_j(\lambda b_j + \mu c_j) = \lambda D_j(b_j) + \mu D_j(c_j)
 }
$$


#### Corollary 1.44a.1 (Linearity Property of Determinants in Rows): 
If the $\large{i}$-th row of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ are a linear combination of two rows of numbers(which may or may not belong to the same determinant):
$$\large{a_{ij} = \lambda b_j + \mu c_j}$$
for every $\large{j = 1,2,\ldots, n}$ where $\large{n}$ is the [[Determinants#Definition(Determinants)|order]] of $\large{D}$ and $\large{\lambda, \mu \in K}$ for the [[Fields and Ordered Fields#Definition 1.12|Field]] $\large{K}$. Then $\large{D}$ is equivalent to the linear combination of the two determinants:
$$\large{D = \lambda D_1 + \mu D_2}$$
Where $\large{D_1}$ and $\large{D_2}$ have the same rows as $\large{D}$ except for the row $\large{i}$. In place of this row are the rows $\large{b_1, b_2, \ldots, b_n}$ and $\large{c_1, c_2, \ldots, c_n}$ respectively.
##### Proof:
Take the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transposition]] of $\large{D}$ and apply [[#Theorem 1.44a (Linearity Property of Determinants in Columns)|Theorem 1.44a]] alongside [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Theorem 1.41]].


#### Theorem 1.44b (Linearity Property of Multiple Variables in Columns):
For a given [[Determinants#Definition(Determinants)|determinant]] $\large{D}$, if the column $\large{j}$ are a linear combination of $\large{m}$ columns of numbers(which may or may not be themselves members of $\large{D}$):
$$\large{
D_j(\lambda_1b_{1j} + \lambda_2c_{2j} + \ldots + \lambda_mf_{mj}) = \lambda _1D_j(b_{1j} ) + \lambda_2D_j(c_{2j}) + \ldots + \lambda_m D_j(f_{mj})
}$$
##### Proof: 
Induction on $\large{m}$:
Base Case $\large{m = 2}$: 
See [[The Linearity Property of Determinants#Theorem 1.44a (Linearity Property of Determinants in Columns)|Theorem 1.44a]].
Induction step, Suppose that: 
$\large{D_j(\lambda_1b_{1j} + \lambda_2c_{2j} + \ldots + \lambda_mf_{mj}) = \lambda _1D_j(b_{1j} ) + \lambda_2D_j(c_{2j}) + \ldots + \lambda_m D_j(f_{mj})}$ 
Now consider: 
$\large{D_j(\lambda_1b_{1j} + \lambda_2c_{2j} + \ldots + \lambda_mf_{mj} + \lambda_{(m+1)}g_{(m+1)j})}$
By [[The Linearity Property of Determinants#Theorem 1.44a (Linearity Property of Determinants in Columns)|Theorem 1.44a]], 

$$\large{\begin{eqnarray}
D_j(\lambda_1b_{1j} + \lambda_2c_{2j} + \ldots + \lambda_mf_{mj} + \lambda_{(m+1)}g_{(m+1)j}) = \\ \lambda_{(m+1)}D_j(g_{(m+1)j}) + D_j(\lambda_1b_{1j} + \lambda_2c_{2j} + \ldots + \lambda_mf_{mj}) 
\end{eqnarray}
}$$
Then by inductive hypothesis:
$$\large{\begin{eqnarray}
D_j(\lambda_1b_{1j} + \lambda_2c_{2j} + \ldots + \lambda_mf_{mj} + \lambda_{(m+1)}g_{(m+1)j}) = \\ \lambda_{(m+1)}D_j(g_{(m+1)j}) + \lambda _1D_j(b_{1j} ) + \lambda_2D_j(c_{2j}) + \ldots + \lambda_m D_j(f_{mj})
\end{eqnarray}
}$$



#### Corollary 1.44b.1 (Linearity Property of Multiple Variables in Rows):
For a given [[Determinants#Definition(Determinants)|determinant]] $\large{D}$, if the row $\large{j}$ are a linear combination of $\large{m}$ rows of numbers(which may or may not be themselves members of $\large{D}$):
$$\large{
D_j(\lambda_1b_{1j} + \lambda_2c_{2j} + \ldots + \lambda_mf_{mj}) = \lambda _1D_j(b_{1j} ) + \lambda_2D_j(c_{2j}) + \ldots + \lambda_m D_j(f_{mj})
}$$
##### Proof: 
Take the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transposition]] of $\large{D}$ and apply [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Theorem 1.41]] alongside [[The Linearity Property of Determinants#Theorem 1.44b (Linearity Property of Multiple Variables in Columns)|Theorem 1.44b]].


#### Corollary 1.45: 
Any common factor of a column of a [[Determinants#Definition(Determinants)|determinant]] can be factored out of the determinant. 
##### Proof:
If $\large{a_{i,j} = \lambda b_i}$ then $\large{D_j(a_{i,j}) = D_j(\lambda b_i)}$.Then by [[The Linearity Property of Determinants#Theorem 1.44a (Linearity Property of Determinants in Columns)|Theorem 1.44a]] $\large{D_j(\lambda b_i) = \lambda D_j(b_i)}$ so $\large{D_j(a_{i,j}) = \lambda D_j(b_i)}$.


#### Corollary 1.45.1: 
Any common factor of a row of a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ can be factored out of that determinant. 
##### Proof:
Consider the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transposition]] of $\large{D}$ called $\large{D^\prime}$.
If for a particular row $\large{i}$, $\large{a_{i,j} = \lambda b_j}$ then in $\large{D^\prime}$ through the application of [[The Linearity Property of Determinants#Corollary 1.45|Corollary 1.45]] $\large{D_j^\prime(a_{i,j}) = \lambda D_j^\prime(b_i)}$ but we know by [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Theorem 1.41]] $\large{D = D^\prime}$. So it stands that $\large{D_i(a_{i,j}) = \lambda D_i(b_j)}$ 


#### Corollary 1.46: 
If a column of a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ consists entirely of zeros then $\large{D = 0}$.
##### Proof:
By [[The Linearity Property of Determinants#Corollary 1.45|Corollary 1.45]] $\large{D_j(0) = D_j(0*1)= 0*D_j(1) = 0}$ 


#### Corollary 1.46.1
If a row of a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ consists entirely of zeros then $\large{D=0}$.
##### Proof:
By [[The Linearity Property of Determinants#Corollary 1.45.1|Corollary 1.45.1]] $\large{D_i(0) = D_i(0*1) = 0*D_i(1) = 0}$.

#### Theorem 1.47a:
The value of a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ does not change when the elements of one column multiplied by an arbitrary number is added to another column.
##### Proof:
Suppose that the elements of the $\large{j}$th column $\large{a_{i,j}}$ are multiplied by the number $\large{\lambda}$ and added to the elements of the $\large{k}$th column ($\large{j \ne k}$) $\large{b_{i,k}}$.
Then by [[The Linearity Property of Determinants#Theorem 1.44a (Linearity Property of Determinants in Columns)|Theorem 1.44a]]:
$\large{D_k(b_{i,k} + \lambda a_{i,j}) = D_k(b_{i,k}) + \lambda D_k(a_{i,j})}$ 
But the determinant $\large{D_k(a_{i,j})}$ contains two identical columns($\large{j}$ and $\large{k}$) so by [[Anti-symmetry Property of the Determinant#Corollary 1.43.1|Corollary 1.43.1]] $\large{D_k(b_{i,k} + \lambda a_{i,j})= D_k(b_{i,k})}$ as asserted.

#### Corollary 1.47a.1: 
The value of a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ does not change when the elements of one row multiplied by an arbitrary number is added to another row.
##### Proof:
Taking the [[Transpose of a Determinant#Definition 1.41 (Transposition)|transposition]] of $\large{D}$ and calling it $\large{D^\prime}$, by [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Theorem 1.41]] we know that $\large{D = D^\prime}$. The desired equality is found by applying [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]].

#### Theorem 1.47b: 
The value of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ does not change when the elements of one of its columns $\large{j}$ scaled by the number $\large{\lambda _j}$ along with the distinct column $\large{k}$ scaled by $\large{\lambda _ k}$ and so on until column $\large{p}$ scaled by the number $\large{\lambda _p}$ are added to the column $\large{m}$($\large{m\ne j, m \ne k, \ldots, m \ne p}$).
In other words: 
$\large{D_m(a_{i,m} + \lambda_j a_{i,j} + \lambda_k a_{i,k} + \ldots + \lambda_p a_{i,p}) = D_m(a_{i,m})}$
##### Proof: 
Consider $\large{D_m(a_{i,m} + \lambda_j a_{i,j} + \lambda_k a_{i,k} + \ldots + \lambda_p a_{i,p})}$.
By [[The Linearity Property of Determinants#Theorem 1.44b (Linearity Property of Multiple Variables in Columns)|Theorem 1.44b]]:
$\large{D_m(a_{i,m} + \lambda_j a_{i,j} + \lambda_k a_{i,k} + \ldots + \lambda_p a_{i,p}) = D_m(a_{i,m}) + \lambda_j D_m(a_{i,j}) + \lambda_k D_m(a_{i,k}) + \ldots + \lambda_p D_m(a_{i,p})}$
Note that since $\large{m \ne j, m \ne k, \ldots, m \ne p}$ all of $\large{D_m(a_{i,j}), D_m(a_{i,k}), \ldots, D_m(a_{i,p})}$ contain duplicate columns and by [[Anti-symmetry Property of the Determinant#Corollary 1.43.1|Corollary 1.43.1]]:
$\large{D_m(a_{i,m} + \lambda_j a_{i,j} + \lambda_k a_{i,k} + \ldots + \lambda_p a_{i,p}) = D_m(a_{i,m}) }$  

#### Corollary 1.47b.1: 
The value of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ does not change when the elements of one of its rows $\large{j}$ scaled by the number $\large{\lambda _j}$ along with the distinct row $\large{k}$ scaled by $\large{\lambda _ k}$ and so on until row $\large{p}$ scaled by the number $\large{\lambda _p}$ are added to the row $\large{m}$($\large{m\ne j, m \ne k, \ldots, m \ne p}$).
##### Proof:
Denote the [[Transpose of a Determinant#Definition 1.41 (Transposition)|transpose]] of the determinant $\large{D}$ as $\large{D^\prime}$. By [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Theorem 1.41]] we know that $\large{D = D^\prime}$. By [[The Linearity Property of Determinants#Theorem 1.47b|Theorem 1.47b]] 
$\large{D^\prime_m(a_{i,m} + \lambda_j a_{i,j} + \lambda_k a_{i,k} + \ldots + \lambda_p a_{i,p}) = D^\prime_m(a_{i,m})}$ giving us the desired result. 