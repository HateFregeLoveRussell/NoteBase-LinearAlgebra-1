---
type: Academic
tags:
alias: Lin-Alg-1-AsymmetryPropertyOfTheDeterminant
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
  class-alias: "Lin-Alg-1",
  book-title: "Linear Algebra",
  source-alias: "Lin-Alg-1-Ch1-Sec1-4",
  type: "tbsection",
  ISBN: "978-0-486-63518-7",
  end-page: 12,
  section-name: "Properties of Determinants",
  template: {
    type: "object",
    version: 1,
    name: "source-tbsection-obj"
  },
  start-page: 8
}
relationship: {name: standard-relationship-obj, version: 1}
friends: "[[Transposition Property of the Determinant]]"
status: {
  state: "Completed",
  template: {
    name: "status-obj",
    version: 1,
    type: "object"
  }
}
validity:  {
  state: True,
  template: {
    name: "validity-obj",
    version: 1,
    type: "object"
  }
}
template: {name: class-note-template, version: 1}
---
#### Lemma 1.42.1 (Anti-Symmetry Property In Consecutive Columns):
Interchanging 2 consecutive columns in a [[Determinants#Definition(Determinants)|Determinant]] changes the determinant's sign. 

##### Proof: 
Suppose the columns in question are called $\large{j}$ and $\large{j+1}$. Call the original determinant $\large{D}$ and the augmented determinant $\large{D^\prime}$.
Clearly both $\large{D}$ and $\large{D^\prime}$ consist of the same [[Determinants#Definition(Determinants)|terms]].
Consider some arbitrary term in both $\large{D}$ and $\large{D^\prime}$: $\large{a_{\alpha_1,1 }a_{\alpha_2,2}\ldots a_{\alpha_n,n}}$ where the integer $\large{n}$ denotes the [[Determinants#Definition(Determinants)|Order]] of both determinants. 
This term by definition must contain some element from the column $\large{j}$ and another distinct element from the column $\large{j+1}$. Call these elements $\large{a_{\alpha_j,j}}$ and $\large{a_{\alpha_{j+1},j+1}}$.
Note that in $\large{D}$, $\large{j \lt j+1}$.
Suppose $\large{a_{\alpha_j,j}}$ and $\large{a_{\alpha_{j+1},j+1}}$ have a negative [[Geometric Interpretation of the Determinant#Positive and Negative Slopes|slope]] in $\large{D}$, so $\large{\alpha_j > \alpha_{j+1}}$, then after the inversion $\large{j \not \lt {j+1}}$ meaning the slope is positive in $\large{D^\prime}$.
Similarly suppose $\large{a_{\alpha_j,j}}$ and $\large{a_{\alpha_{j+1},j+1}}$ have a positive [[Geometric Interpretation of the Determinant#Positive and Negative Slopes|slope]] in $\large{D}$, so $\large{\alpha_{j} \lt \alpha_{j+1}}$. Then after the inversion the slope is negative. 
![[Lemma 1.42.1 Proof Asset|600]]
For pairs in $\large{a_{\alpha_1,1 }a_{\alpha_2,2}\ldots a_{\alpha_n,n}}$ which are not $\large{a_{\alpha_j,j}}$ and $\large{a_{\alpha_{j+1},j+1}}$, the sign of the slope does not change. 
So for every given term in the determinants $\large{D}$ there is exactly one extra [[Geometric Interpretation of the Determinant#The Role of Slope in Computing Determinants|Inversion]] in $\large{D^\prime}$. This means that every term in $\large{D^\prime}$ is the negative of every term in $\large{D}$, factoring out this $\large{-1}$ factor from the [[Determinants#Definition(Determinants)|sum]] we see that: $\large{D = -D^\prime}$ 

#### Theorem 1.42 (The Anti-Symmetry Property in Columns): 
Suppose two columns are interchanged in the [[Determinants#Definition(Determinants)|Determinant]] $\large{D}$, then the resulting determinant $\large{D^\prime = -D}$.

##### Proof: 
If the Columns in question are consecutive than by [[Anti-symmetry Property of the Determinant#Lemma 1.42.1 (Anti-Symmetry Property In Consecutive Columns)|Lemma 1.42.1]] $\large{D^\prime = -D}$.
Suppose the columns in question are not consecutive. Denote the columns $\large{j}$ and $\large{k}$ ($\large{j \lt k}$). 
Then there are $\large{m = k - j - 1}$ columns between $\large{j}$ and $\large{k}$.
Interchanging these two columns can be achieved by the successive interchanging of consecutive columns: 
$\large{j}$ and $\large{j+1}$, $\large{j+1}$ and $\large{j+2}$, $\large{\ldots}$, $\large{j + m}$ and $\large{k}$, $\large{k}$ and $\large{k-1}$, $\large{\ldots}$, $\large{k -1}$ and $\large{k-2}$, $\large{\ldots}$, $\large{k-m}$ and $\large{k-m-1}$.
There are $\large{m+m+1 = 2m + 1}$ interchanges in this sequence so $\large{D^\prime = (-1)^{2m+1} D}$ 
But as $\large{m}$ is some natural number $\large{2m + 1}$ is necessarily an odd number meaning that $\large{D^\prime = -D}$.

#### Corollary 1.42.2 (The Anti-Symmetry Property in Rows): 
Suppose two rows are interchanged in the [[Determinants#Definition(Determinants)|Determinant]] $\large{D}$, then the resulting determinant $\large{D^\prime = -D}$.

##### Proof:
Taking the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transposition]] of $\large{D}$ and $\large{D^\prime}$ and then using [[Anti-symmetry Property of the Determinant#Theorem 1.42 (The Anti-Symmetry Property in Columns)|Theorem 1.42]] alongside [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Theorem 1.41]] we find that $\large{D = -D^\prime}$.

#### Corollary 1.43.1 : 
A [[Determinants#Definition(Determinants)|Determinant]] $\large{D}$ with two identical columns is equal to zero.

##### Proof: 
Interchange the identical columns in $\large{D}$ to obtain $\large{D^\prime}$. Then $\large{D = D^\prime}$ as both $\large{D}$ and $\large{D^\prime}$ consist of exactly the same elements. But then by [[Anti-symmetry Property of the Determinant#Theorem 1.42 (The Anti-Symmetry Property in Columns)|Theorem 1.42]] $\large{D = -D^\prime}$. The only number for which $\large{D = D^\prime}$ and $\large{D = -D^\prime}$ is zero. 

#### Corollary 1.43.2:
A [[Determinants#Definition(Determinants)|Determinant]] $\large{D}$ with two identical rows is equal to zero.

##### Proof: 
Taking the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transposition]] of $\large{D}$ and using [[Anti-symmetry Property of the Determinant#Corollary 1.43.1|Corollary 1.43.1]] alongside [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Theorem 1.41]] we see that $\large{D = 0}$.

