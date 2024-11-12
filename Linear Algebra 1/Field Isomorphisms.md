---
type: Academic
tags:
alias: Lin-Alg-1-FieldIsomorphisms
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
  section-name: "Number Fields",
  start-page: 1,
  type: "tbsection",
  template: {
    name: "source-tbsection-obj",
    version: 1,
    type: "object"
  },
  class-alias: "Lin-Alg-1",
  source-alias: "Lin-Alg-1-Ch1-Sec1-1",
  ISBN: "978-0-486-63518-7",
  end-page: 3,
  book-title: "Linear Algebra"
}
relationship: {name: standard-relationship-obj, version: 1}
friends: [[[Number Fields]], [[Elements of Number Fields]]]
status: {
  state: "In Progress",
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
#### Definition (Field Isomorphisms): 
Two [[Number Fields#Definition (Number Fields)|Fields]] denoted $\large{K_1}$ and $\large{K_2}$ are regarded as **==Isomorphic==** if one can find a one-to-one correspondence between the elements of $\large K_1$ and $\large K_2$ such that the [[Number Fields#Addition|Sum]] or [[Number Fields#Multiplication|Product]] of any two elements in $\large{K_1}$ are equal to the  Sum or Product of the corresponding elements in $\large{K_2}$.

##### Note: 
The equality of the [[Number Fields#Subtraction|Difference]] and [[Number Fields#Division|Quotient]] of two elements in $\large{K_1}$ and their corresponding elements in $\large{K_2}$ follows from the equality of products and sums described above.
TODO: Prove this
