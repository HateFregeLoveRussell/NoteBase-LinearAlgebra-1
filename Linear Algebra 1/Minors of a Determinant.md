---
type: Academic
tags:
alias: Lin-Alg-1-MinorsOfADeterminant
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
relationship: {name: standard-relationship-obj, version: 1}
friends: "[[Cofactor of a Determinant]]"
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
#### Definition(Minors): 
Suppose we have a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ of order $\large{n}$. If we delete a row $\large{i}$ and a column $\large{j}$ from $\large{D}$ we obtain another determinant of order $\large{n-1}$. Determinants created in this way are called **==Minors==** of the determinant $\large{D}$ denoted as $\large{M_{i,j}}$ or $\large{M_{i,j}(D)}$.

#### Theorem 1.53:
Given the [[Cofactor of a Determinant#Definition(Cofactors)|Cofactor]] $\large{A_{i,j}}$ and the [[Minors of a Determinant#Definition(Minors)|Minor]] $\large{M_{i,j}}$ of the [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ the following relationship holds:
$$\large{A_{i,j}= (-1)^{i+j}M_{i,j}}$$
##### Proof: 
First we will show that $\large{A_{1,1} = M_{1,1}}$:

Consider some term in the [[Cofactor of a Determinant#Definition(Cofactors)|Cofactor]] $\large{A_{1,1}}$, call it $\large{c}$. It is clear from the definition of the cofactor that $\large{c}$ is composed of $\large{n-1}$ elements of $\large{D}$ from unique columns and rows. This means that some term in $\large{M_{1,1}}$ is composed of the same elements as $\large{c}$. Additionally, there cannot be a segment of [[Geometric Interpretation of the Determinant#Positive and Negative Slopes|negative slope]] connecting $\large{c}$ with $\large{a_{1,1}}$ meaning that the sign ascribed to $\large{c}$ is the same as the sign ascribed to the analogous term in $\large{M_{1,1}}$. 
So if $\large{c}$ is a term in $\large{A_{1,1}}$ then it also must be a term in $\large{M_{1,1}}$. 

Now consider some term in the [[Minors of a Determinant#Definition(Minors)|Minor]] $\large{M_{1,1}}$ called $\large{d}$. By definition, $\large{d = (-1)^{N(\beta_1,\beta_2,\ldots,\beta_{n-1})}a_{\beta_1,2}a_{\beta_2,3}\ldots a_{\beta_{n-1},n}}$ where $\large{\beta_1, \beta_2, \ldots, \beta_{n-1}}$ are selected so their corresponding elements are from unique column and rows. Since a [[Determinants#Definition(Determinants)|determinant]] by definition contains all such combinations of terms it stands that their is some term composed of the elements $\large{a_{1,1}, a_{\beta_1,2}, \ldots, a_{\beta_{n-1}n}}$ in the determinant $\large{D}$. Furthermore we know that the inclusion of the element $\large{a_{1,1}}$ cannot change the sign of this term from the one in $\large{d}$ as it does not introduce any segments with [[Geometric Interpretation of the Determinant#Positive and Negative Slopes|negative slope]]. So the term $\large{a_{1,1}d}$ must exist in $\large{D}$. Additionally, since this term contains the element $\large{a_{1,1}}$ we know that the term $\large{d}$ exists in $\large{A_{1,1}}$. 
So if $\large{c}$ is a term in $\large{M_{1,1}}$ then it also must be a term in $\large{A_{1,1}}$.

so $\large{c}$ is a term in $\large{M_{1,1}}$ if and only if it is a term in $\large{A_{1,1}}$. Which implies that $\large{M_{1,1}}$ and $\large{A_{1,1}}$ consists of the sum of precisely the same terms. Or in other words $\large{A_{1,1} = M_{1,1}}$. 

Now we will show the equality for a general row $\large{i}$ and column $\large{j}$.
Consider the [[Cofactor of a Determinant#Definition(Cofactors)|Cofactor]] and [[Minors of a Determinant#Definition(Minors)|Minor]] $\large{A_{i,j}}$ and $\large{M_{i,j}}$ of the determinant $\large{D}$. 
We will first augment the determinant $\large{D}$ through successive interchanging of columns and rows until column $\large{j}$ and row $\large{i}$ are situated in the position $\large{1,1}$ in the augmented matrix $\large{D^\prime}$. This will require exactly $\large{i-1}$ interchanges of rows and $\large{j-1}$ interchanges of columns, resulting in $\large{i + j -2}$ total interchanges. 
A consequence of this augmentation is that $\large{M_{i,j}(D) = M_{1,1}(D^\prime)}$. We have previously shown that $\large{M_{1,1} = A_{1,1}}$ so it stands that $\large{M_{i,j}(D) = A_{1,1}^\prime}$ where $\large{A_{1,1}^\prime}$ represents the cofactor of the element $\large{a_{1,1}^\prime = a_{i,j}}$ in $\large{D^\prime}$. 
Using [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]] we know that $\large{D^\prime = \sum_{k=1}^n a_{k,j}^\prime A_{k,j}^\prime}$. Replacing $\large{A_{1,1}^\prime}$ and $\large{a_{1,1}^\prime}$ with $\large{M_{i,j}}$ and $\large{a_{i,j}}$ respectively we get the expression $\large{D^\prime = a_{i,j}M_{i,j} + \sum_{k=2}^n a_{k,j}^\prime A_{k,j}^\prime}$. Furthermore we know from [[Anti-symmetry Property of the Determinant#Lemma 1.42.1 (Anti-Symmetry Property In Consecutive Columns)|Theorem 1.42.1]] and [[Anti-symmetry Property of the Determinant#Corollary 1.42.2 (The Anti-Symmetry Property in Rows)|Theorem 1.42.2]] that $\large{D^\prime = (-1)^{i + j -2}D = (-1)^{i + j}D}$. Combining the equalities we see that  
$$\large{D = (-1)^{i+j}a_{i,j}M_{i,j} + (-1)^{i+j}\sum_{k=2}^n a_{k,j}^\prime A_{k,j}^\prime}$$
By [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]] we know that $\large{D = \sum_{k=1}^n a_{k,j}A_{k,j}}$. Matching on the variables $\large{a_{k,j}}$ between the equalities yields $\large{a_{i,j}A_{i,j} = (-1)^{i+j}a_{i,j}M_{i,j}}$ which then reduces to $\large{A_{i,j} = (-1)^{i+j}M_{i,j}}$ as required. 

###### Comment: 
Interestingly enough the branch where $\large{a_{i,j} = 0}$ is excluded from the proof in the book. 
#TODO Resolve this 


#### Theorem 1.54: 
For a [[Determinants#Definition(Determinants)|determinant]] $\large{D}$ the following equalities hold: 
$$\large{
\begin{eqnarray}
D &=& \sum_{i=1}^n (-1)^{i+j}a_{i,j}M_{i,j} \\ 
D &=& \sum_{j=1}^n (-1)^{i+j} a_{i,j}M_{i,j}
\end{eqnarray}
}$$
where $\large{i,j}$ are some row and column in $\large{D}$, $\large{a_{i,j}}$ is the corresponding element of the determinant at index $\large{i,j}$, and $\large{M_{i,j}}$ represents the [[Minors of a Determinant#Definition(Minors)|Minor]] of the determinant at row $\large{i}$ and column $\large{j}$. 
##### Proof:
From [[Cofactor of a Determinant#Theorem 1.51|Theorem 1.51]] we know that $\large{D= \sum_{i=1}^n a_{i,j}A_{i,j}}$ and $\large{D = \sum^n_{j=1}a_{i,j}A_{i,j}}$. 
Substituting the equality in [[Minors of a Determinant#Theorem 1.53|Theorem 1.53]] we get the desired equalities. 

##### Example: 
We can apply [[Minors of a Determinant#Theorem 1.54|Theorem 1.54]] to an arbitrary 3 by 3 determinant to get the equality: 

$$\large{
D = 
\begin{vmatrix} 
a_{1,1} & a_{1,2} & a_{1,3} \\
a_{2,1} & a_{2,2} & a_{2,3} \\
a_{3,1} & a_{3,2} & a_{3,3}
\end{vmatrix}
=
a_{1,1} \begin{vmatrix} a_{2,2} & a_{2,3} \\ a_{3,2} & a_{3,3}\end{vmatrix}  - 
a_{2,1} \begin{vmatrix} a_{1,2} & a_{1,3} \\ a_{3,2} & a_{3,3}\end{vmatrix} + 
a_{3,1} \begin{vmatrix} a_{1,2} & a_{1,3} \\ a_{2,2} & a_{2,3}\end{vmatrix}
}
$$
