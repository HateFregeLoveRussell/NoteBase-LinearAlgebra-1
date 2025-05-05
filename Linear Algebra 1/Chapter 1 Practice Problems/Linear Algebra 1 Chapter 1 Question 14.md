---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q14
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
  source-alias: "Lin-Alg-1-Ch1-PP",
  book-title: "Linear Algebra",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  },
  start-page: 28,
  class-alias: "Lin-Alg-1",
  end-page: 30,
  section-name: "Chapter 1 Practice Problems",
  ISBN: "978-0-486-63518-7"
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

### Problem Statement: 
Show that if the rows of a [[Determinants#Definition(Determinants)|determinant]] of order $\large{n}$ are [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Dependent]] then its columns are also Linearly Dependent. 

#### Solution: 
Suppose that the rows of some [[Determinants#Definition(Determinants)|determinant]] of order $\large{n}$, call it $\large{D}$, are [[Linear Dependence Between Columns of a Determinant#Definition (Linear Dependence)|Linearly Dependent]].

Then the [[Transpose of a Determinant#Definition 1.41 (Transposition)|Transpose]] of $\large{D}$, call it $\large{D^\prime}$ has a set of Linearly Dependent columns. 

A determinant equals zero if and only if its columns are Linearly Dependent by [[Linear Dependence Between Columns of a Determinant#Theorem 1.96|Theorem 1.96]]. So $\large{D^\prime = 0}$

Then by the [[Transposition Property of the Determinant#Theorem 1.41 (The Transposition Property)|Transposition Property]] of the determinant, $\large{D = 0}$

But then by [[Linear Dependence Between Columns of a Determinant#Theorem 1.96|Theorem 1.96]] again $\large{D}$ must have a set of Linearly Dependent columns

So if the rows of some determinant are linearly dependent then so are the columns of the determinant.