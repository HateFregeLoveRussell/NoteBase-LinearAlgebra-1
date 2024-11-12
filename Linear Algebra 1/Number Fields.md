---
type: Academic
tags:
alias: Lin-Alg-1-NumFields
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
  section-name: "Number Fields",
  ISBN: "978-0-486-63518-7",
  book-title: "Linear Algebra",
  class-alias: "Lin-Alg-1",
  source-alias: "Lin-Alg-1-Ch1-Sec1-1",
  start-page: 1,
  end-page: 3,
  template: {
    name: "source-tbsection-obj",
    version: 1,
    type: "object"
  }
}
relationship: {name: standard-relationship-obj, version: 1}
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

#### Definition (Number Fields):  
A ==**Number Field**== is a set $\large K$ of objects, called **==numbers==** which when subjected to four arithmetic operations $\large{+, - , /, \cdot}$ give elements of $\large K$. More specifically, these operations have the following properties called the 
**==Field Axioms==**:
##### Addition:
For every $\large{\alpha, \beta \in K}$ there corresponds a unique number $\large{\alpha + \beta \in K}$ called the **==sum==** of $\large{\alpha}$ and $\large{\beta}$ such that: 

- (A1) $\large{\alpha + \beta = \beta + \alpha}$ for every $\large{\alpha,\beta \in K}$ (Addition is Commutative)
- (A2) $\large{\alpha + (\beta + \gamma) = (\alpha + \beta) + \gamma}$ for ever $\large{\alpha, \beta, \gamma \in K}$ (Addition is Associative)
- (A3) There exists a number $\large{0 \in K }$ such that $\large{0 + \alpha = \alpha}$ for every $\large{\alpha \in K }$ called the **==zero element==**
- (A4) For every $\large{\alpha \in K}$ there exists a number called the **==negative element==** denoted $\large{\gamma \in K}$ such that $\large{\alpha + \gamma = 0}$.

##### Subtraction: 
[[Number Fields#Addition|Axiom A4]] allow us to define a new operation called the **==difference==** of $\large {\alpha \in K}$ and $\large{\beta \in K}$ denoted $\large{\beta - \alpha \in K}$ that is the sum of $\large{\beta}$ and the solution $\large{\gamma \in K}$ of the equation $\large{\alpha + \gamma = 0}$ 

##### Multiplication: 
For every pair of numbers $\large{\alpha, \beta \in K}$ there corresponds a unique number $\large{\alpha \cdot \beta \in K }$ (also denoted as $\large{\alpha \beta}$)called the **==product==** of $\large{\alpha}$ and $\large{\beta}$ such that: 

- (M1) $\large{\alpha \cdot \beta = \beta \cdot \alpha}$ for every $\large{\alpha, \beta \in K}$ (Multiplication is Commutative)
- (M2) $\large{\alpha \cdot (\beta \cdot \gamma) = (\alpha \cdot \beta) \cdot \gamma}$ for every $\large{\alpha, \beta, \gamma \in K}$ (Multiplication is Associative)
- (M3) There exists a number $\large{1 \in K}$ such that $\large{1 \ne 0}$ and $\large{1\cdot \alpha = \alpha }$ for every $\alpha \in K$ 
- (M4) For Every $\large{\alpha \in K }$ where $\large{\alpha \ne 0}$ there exists a number $\large{\gamma \in K}$ called the **==reciprocal element==** such that $\large{\alpha \cdot \gamma = 1}$ 
- (M5) $\large{\alpha \cdot (\beta + \gamma) = (\alpha \cdot \beta) + (\alpha \cdot \gamma)}$ for every $\large{\alpha, \beta, \gamma \in K}$ (Multiplication is Right Distributive over Addition)
##### Division: 
Axiom (M4) allows us to define the operation of **==division==** by defining the quotient $\large{\alpha / \beta}$ as the product of the number $\large{\beta \in K}$ and the number $\large{\gamma \in K }$ being the solution to $\large{\alpha \cdot \gamma = 1}$
   
###### Note: 
Our definition of [[Number Fields#Multiplication|Axiom (M5)]] alongside [[Number Fields#Multiplication|Axiom (M1)]] imply that $\large{(\alpha + \beta)\gamma = \alpha \gamma + \beta \gamma}$ meaning that Left Distributivity of Multiplication over Addition does not need to be assumed as an axiom in order to get the Distributivity Property of Multiplication over Addition.

