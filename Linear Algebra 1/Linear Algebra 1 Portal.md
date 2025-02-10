---
type: Academic
tags: [Entrynote]
alias: Lin-Alg-1-Portal
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
relationship: {name: standard-relationship-obj, version: 1}
parent: ["[[Linear Algebra 1 Display Portal]]"]
class-status: {
  state: "In Progress",
  template: {
    name: "status-obj",
    version: 1,
    type: "object"
  }
}
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
template: {name: class-portal-template, version: 2} 
---
### Class Description:
```dataview
TABLE class.class-name AS "Class Name", class.author AS "Class Author", class.medium AS "Class Medium", class.length AS "Class Length"
WHERE file = this.file
```
Textbook acting as a more rigorous introduction to Linear Algebra.
### Class Content:
- Chapter 1: Determinants 
- Chapter 2: Linear Spaces
- Chapter 3: Systems of Linear Equations
- Chapter 4: Linear Functions of a Vector Argument
- Chapter 5: Coordinate Transformations
- Chapter 6: The Canonical Form of the Matrix of a Linear Operator
- Chapter 7: Bilinear and Quadratic Forms
- Chapter 8: Euclidean Spaces
- Chapter 9: Unitary Spaces
- Chapter 10: Quadratic Forms in Euclidean and Unitary Spaces
- Chapter 11: Finite-Dimensional Algebras and Their Representations
- Appendix: Categories of Finite-Dimensional Spaces
### Class Progress: 
In Progress Notes:
```dataview
LIST
FROM "Academic Notes/Linear Algebra 1" 
WHERE status.state = "In Progress" OR status.state = "Stub"
LIMIT 10
```



