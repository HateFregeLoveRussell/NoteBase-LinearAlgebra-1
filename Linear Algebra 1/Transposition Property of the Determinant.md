---
type: Academic
tags: 
alias: Lin-Alg-1-TranspositionPropertyOfTheDeterminant
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
  source-alias: "Lin-Alg-1-Ch1-Sec1-4",
  book-title: "Linear Algebra",
  section-name: "Properties of Determinants",
  type: "tbsection",
  start-page: 8,
  ISBN: "978-0-486-63518-7",
  end-page: 12,
  template: {
    type: "object",
    version: 1,
    name: "source-tbsection-obj"
  }
}
relationship: {name: standard-relationship-obj, version: 1}
parent: "[[Determinants]]"
status: {
  state: "Completed",
  template: {
    name: "status-obj",
    version: 1,
    type: "object"
  }
}
validity: {
  state: true,
  template: {
    name: "validity-obj",
    version: 1,
    type: "object"
  }
}
template: {name: class-note-template, version: 1}
---
#### Theorem 1.41 (The Transposition Property):
Given a [[Determinants#Definition(Determinants)|Determinant]] $\large{D}$. The [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transpose]] of $\large{D}$ has the same value as $\large{D}$ itself.

##### Proof: 
Call $\large{D^\prime}$ the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transpose]] of the [[Determinants#Definition(Determinants)|Determinant]] $\large{D}$. It is clear that both $\large{D}$ and $\large{D^\prime}$ consist of the same terms. We know that the Transposition operation is equivalent to [[Transpose of a Determinant#Note|rotating along the principal diagonal by 180 degrees.]] 

Suppose that there is a segment with [[Geometric Interpretation of the Determinant#Positive and Negative Slopes|Negative Slope]]. Then this segment would form an acute angle $\large{\alpha \lt 90\degree}$ with the rows of $\large{D}$. Rotating this segment by 180 degrees along the principal diagonal will result in a segment which makes an angle of $\large{\alpha \lt 90 \degree}$ with the columns of $\large{D^\prime}$. This means that the segment now makes an angle of $\large{90\degree - \alpha \lt 90 \degree }$ with the rows of $\large{D^\prime}$.

This means that the total number of segments with [[Geometric Interpretation of the Determinant#Positive and Negative Slopes|Negative Slope]] does not change between $\large{D}$ and $\large{D^\prime}$, and so the sign of the terms in $\large{D}$ and $\large{D^\prime}$ [[Geometric Interpretation of the Determinant|does not change]], meaning that $\large{D = D^\prime}$ 

![[TranspositionPropertyFigure1|800]]

##### Note:
With this theorem we can essentially turn any theorem pertaining to the columns of the determinant to a dual theorem about the rows of a determinant.