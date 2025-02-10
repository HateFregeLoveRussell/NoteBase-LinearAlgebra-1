---
type: Academic
tags:
alias: Lin-Alg-1-CofactorsOfADeterminant
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
  end-page: 16,
  type: "tbsection",
  start-page: 12,
  source-alias: "Lin-Alg-1-Ch1-Sec1-5",
  class-alias: "Lin-Alg-1",
  section-name: "Cofactors And Minors",
  ISBN: "978-0-486-63518-7",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  },
  book-title: "Linear Algebra"
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

#### Definition(Cofactors):
Consider a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$. We know that by definition $$\large{
D = \sum (-1)^{N(\alpha_1, \alpha_2, \ldots, \alpha_n)}a_{\alpha_1 1}a_{\alpha_2 2} \ldots a_{\alpha_n n}
}$$
Now consider some element in $\large{D}$ called $\large{a_{i,j}}$. Naturally some terms in $\large{D}$ will contain $\large{a_{i,j}}$ as a factor, group all such terms together and factor out $\large{a_{i,j}}$. Call the remaining sum $\large{A_{i,j}}$. This sum is called a **==cofactor==** of $\large{a_{i,j}}$ of the determinant $\large{D}$.

#### Theorem 1.51:
The sum of all the products of any column(or row) of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ with the corresponding [[Cofactor of a Determinant#Definition(Cofactors)|cofactors]] is equal to the determinant $\large{D}$ itself. These formulas are called the **==Cofactor Expansions==** of the determinant $\large{D}$.
##### Proof:
Note that if a [[Determinants#Definition(Determinants)|term]] in $\large{D}$ contains $\large{a_{i,j}}$ then it cannot contain another term from the row $\large{i}$ or the column $\large{j}$. For this reason we can group together all terms containing the elements of the row(or column) of $\large{a_{i,j}}$ in $\large{D}$ and then factor out said elements. In other words,
$$\large{
\begin{eqnarray}
D &=& a_{1,j} A_{1,j}  + a_{2,j}A_{2,j} + \ldots + a_{n,j}A_{n,j} \\
 &=& \sum_{i=1}^n a_{i,j}A_{i,j} \\ 
 &\text{and}& \\ 
  D &=& a_{i,1}A_{1,i} + a_{i,2}A_{2,i} + \ldots + a_{i,n}A_{n,i} \\ 
  &=& \sum_{j=1}^n a_{i,j}A_{i,j}
\end{eqnarray}
} 
$$
#### Theorem 1.52:
The sum of all the products of the elements of a column(or row) of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ with the [[Cofactor of a Determinant#Definition(Cofactors)|cofactors]] of another column(or row) is equal to zero.
##### Proof:
From [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]] we know that: $\large{D = \sum_{i=0}^n a_{i,j}A_{i,j}}$  and $\large{D = \sum_{j=0}^n a_{i,j}A_{i,j}}$.

For the first expression consider some column $\large{k}$($\large{k \ne j}$) in the determinant $\large{D}$ and replace the elements $\large{a_{i,j}}$ with $\large{a_{i,k}}$. Note that this replacement does not change any of the cofactors $\large{A_{i,j}}$ in the expression. On the left hand side of the equality however the replacement would involve the introduction of a duplicate column in $\large{D}$ which by [[Anti-symmetry Property of the Determinant#Corollary 1.43.1|Corollary 1.43.1]] means that $\large{D = 0}$. Hence $\large{\sum_{i=0}^n a_{i,k}A_{i,j} = 0}$.

Similarly we can make a replacement using row $\large{l}$($\large{l \ne i}$) in the determinant $\large{D}$ for the second expression. Replacing all $\large{a_{i,j}}$ with $\large{a_{l,j}}$, this replacement similarly does not change the cofactors but does introduce a duplicate row into $\large{D}$, which by [[Anti-symmetry Property of the Determinant#Corollary 1.43.2|Corollary 1.43.2]] means that $\large{\sum_{j=0}^n a_{l,i}A_{i,j} = 0 }$
