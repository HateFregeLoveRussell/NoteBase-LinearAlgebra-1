---
type: Academic
tags:
alias: Lin-Alg-1-CommonNumberFields
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
friends: [[[Number Fields]], [[Elements of Number Fields]], [[Field Isomorphisms]]]
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
#### Definition (Field of Rational Numbers):
This field denoted $\large{\Bbb Q}$ contains all numbers of the form $\large{\frac{p}{q}}$ where both $\large{p}$ and $\large{q}$ are integers and $\large{q \ne 0}$, subject to the ordinary operations of arithmetic.

##### Note: 
It follows that every field $\large{K}$ has an [[Field Isomorphisms#Definition (Field Isomorphisms)|Isomorphic]] subfield to $\large{\Bbb Q}$.
TODO: prove this 

##### Note: 
The integers themselves $\large{\Bbb Z}$ don't form a field because they do not satisfy [[Number Fields#Multiplication|Axiom (M4)]] 
TODO: prove this

#### Definition (Field of Real Numbers):
This field is denoted $\large{\Bbb R}$ is the set of all points on the real line. The [[Number Fields#Definition (Number Fields)|Field Axioms]] are satisfied through the **==Axioms of Order==** and the **==Least Upper Bound Axiom==** typically used to build the Real Numbers. This set is subject to the usual operations of arithmetic. 

#### Definition (Field of Complex Numbers): 
This field is denoted $\large{\Bbb C}$ and is the set of all numbers of the form $\large{a + bi}$ where $\large{a, b }$ are entries in the [[Common Number Fields#Definition (Field of Real Numbers)|Real Number Field]] ($\large i$ is not a real number), with the following definitions of [[Number Fields#Addition|Addition]] and [[Number Fields#Multiplication|Multiplication]]:
$$\large{\begin{eqnarray}
(a_1 + b_1i) + (a_2 + b_2i) &=& (a_1 + a_2) + (b_1 + b_2)i 
\\
(a_1 + b_1i)\cdot (a_2 + b_2 i) &=& (a_1a_2 - b_1b_2) + (a_1b_2 + a_2b_1)i
\end{eqnarray}
}$$

For numbers of the form $\large{a + 0i}$ the operations above reduce to the familiar ones of the [[Common Number Fields#Definition (Field of Real Numbers)|Real Numbers]] and so we write $\large{a + i0 = a}$ and call them **==real==**.

Numbers of the form $\large{0 + bi}$ we call **==purely imaginary==** and we write $\large{0 + bi = bi}$.
It follows that $\large{i^2 = i*i = (0 + 1i)(0 + 1i) = -1}$.

#### Sufficiency of the Real and Complex Fields
According to the **==Fundamental Theorem of Algebra==** we can solve any algebraic equation: 
$$\large{z^n + a_1 z^{n-1} + \ldots + a_n = 0}$$ using the [[Common Number Fields#Definition (Field of Complex Numbers)|Complex Field]] $\large {\Bbb C}$.

##### Note:
The[[Common Number Fields#Definition (Field of Real Numbers)| Real Field]] does not have this property as $\large{z^2 + 1 = 0}$ has no solution in $\large{\Bbb R}$.