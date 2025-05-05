---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q11
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
  source-alias: "Lin-Alg-1-Ch1-PP",
  template: {
    type: "object",
    version: 1,
    name: "source-tbsection-obj"
  },
  type: "tbsection",
  book-title: "Linear Algebra",
  ISBN: "978-0-486-63518-7",
  section-name: "Chapter 1 Practice Problems",
  end-page: 30,
  start-page: 28,
  class-alias: "Lin-Alg-1"
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
Solve the following [[Systems of Linear Equations#Definition (Systems of Linear Equations)|System of Linear Equations]]:
$$\large{
\begin{eqnarray}
x_1 + 2x_2 + 3x_3 + 4x_4 + 5x_5 &=& 13 \\ 
2x_1 + x_2 +2x_3 + 3x_4 + 4x_5 &=& 10 \\
2x_1 + 2x_2 + x_3 + 2x_4 + 3x_5 &=& 11 \\ 
2x_1 + 2x_2 + 2x_3 + x_4 + 2x_5 &=& 6 \\
2x_1 + 2x_2 + 2x_3 + 2x_4 + x_5 &=& 3
\end{eqnarray}
}$$

#### Solution:
The coefficient [[Square Matrices#Definition (Square Matrix)|matrix]] of the system: 
$$\large{
D = \begin{vmatrix}
1 & 2 &3 & 4 & 5 \\
2 & 1 & 2 &3 & 4 \\ 
2 & 2 & 1 & 2 & 3 \\
2 & 2 & 2 & 1 & 2 \\
2 & 2 & 2 & 2 & 1
\end{vmatrix}
}
$$
The constant term column: 
$$\large{
B = \begin{vmatrix}
13 \\ 10 \\ 11 \\ 6 \\ 3
\end{vmatrix}
}$$
By [[Cramer's Rule and Solving Systems of Linear Equations#Theorem 1.71|Cramer's Rule]]: 
$$\large{
c_i = \frac{D_i(B)}{D}
}$$
##### Computing $\large{D}$:
Subtract consecutive columns starting at column column 1 and ending at column 4 using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]:
$$\large{
D = 
\begin{vmatrix} 
-1 & -1 & -1 & -1 & 5 \\
1 & -1 & -1 & -1 & 4 \\
0 & 1 & -1 & -1 & 3 \\
0 & 0 & 1 & -1 & 2 \\
0 & 0 & 0 & 1 & 1
\end{vmatrix}
}$$
Add row two to row 1 using [[The Linearity Property of Determinants#Corollary 1.47a.1|Theorem 1.47a.1]]: 
$$\large{D = 
\begin{vmatrix} 
0 & -2 & -2 & -2 & 9 \\
1 & -1 & -1 & -1 & 4 \\
0 & 1 & -1 & -1 & 3 \\
0 & 0 & 1 & -1 & 2 \\ 
0 & 0 & 0 &1 & 1
\end{vmatrix}
}$$
Now using [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the first column: 
$$\large{
D = -
\begin{vmatrix}
-2 & -2 & -2 & 9 \\
1 & -1 & -1 & 3 \\
0 & 1 & -1 & 2 \\
0 & 0 &1 & 1
\end{vmatrix}
}
$$
Add the second row, scaled by $\large{2}$ to the first row Using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollaty 1.47a.1]]: 
$$\large{
D = - 
\begin{vmatrix} 
0 & -4 & -4 & 15 \\
1 & -1 & -1 & 3 \\
0 & 1 & -1 & 2 \\
0 & 0 & 1 & 1
\end{vmatrix}
}$$
Using [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] again on the first column: 
$$\large{D = \begin{vmatrix} 
-4 & -4 & 15 \\
1 & -1 & 2 \\
0 & 1 & 1
\end{vmatrix}}$$
Add row $\large{2}$ scaled by $\large{4}$ to row $\large{1}$ using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{
D = \begin{vmatrix} 
0 & -8 & 23 \\ 
1 & -1 & 2 \\
0 & 1 & 1
\end{vmatrix}
}$$
Using [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] again: 
$$\large{
D = - \begin{vmatrix}
-8 & 23 \\
1 & 1
\end{vmatrix}
}$$
Now evaluating the second order remainder: 
$$\large{
	D = -(-8 -23) = 8 + 23 + 31
}$$

##### Compute $\large{D_1(B)}$: 

$$\large{
D_1(B) = 
\begin{vmatrix}
13 & 2 & 3 & 4 & 5 \\
10 & 1 & 2 & 3 & 4 \\
11 & 2 & 1 & 2 & 3 \\
6 & 2 & 2 & 1 & 2 \\ 
3 & 2 & 2 &2 & 1
\end{vmatrix}
}$$
Subtract consecutive columns from columns $\large{2}$ to column $\large{4}$ using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]] :
$$\large{D_1(B) = 
\begin{vmatrix} 
13 & -1 & -1 & -1 & 5 \\
10 & -1 & -1 & -1 & 4 \\ 
11 & 1 &  -1 & -1 & 3 \\ 
6 & 0 & 1 & -1 & 2 \\
3 & 0 & 0 & 1 & 1
\end{vmatrix}}$$

Subtract consecutive rows from row $\large{1}$ to row $\large{4}$ using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_1(B) = 
\begin{vmatrix}
3 & 0 & 0 & 0 & 1 \\
-1 & -2 & 0 & 0 & 1 \\ 
5 & 1 & -2 & 0 & 1 \\ 
3 & 0 & 1 & -2 & 1  \\ 
3 & 0 & 0 & 1 & 1
\end{vmatrix}}$$
Subtract column $\large{5}$ scaled by $\large{3}$ from column $\large{1}$ using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{
D_1(B) = \begin{vmatrix} 
0 & 0 & 0 & 0 & 1 \\ 
-4 & -2 & 0 & 0 & 1 \\ 
2 & 1 & -2 & 0 & 1 \\ 
0 & 0 & 1 & -2 & 1 \\ 
0  & 0 & 0 & 1 & 1
\end{vmatrix}
}$$
Preform [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the first row: 
$$\large{
D_1(B) = \begin{vmatrix}
-4 & -2 & 0 & 0  \\ 
2 & 1 & -2 & 0 \\
0 & 0 &1 & -2 \\
0 & 0 & 0 & 1
\end{vmatrix}
}$$
Preform [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the fourth row: 
$$\large{
D_1(B) = \begin{vmatrix} 
-4 & -2 & 0  \\ 
2 & 1 & -2 \\
0 & 0 & 1
\end{vmatrix}
}$$
Preform [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the third row: 
$$\large{
D_1(B) = \begin{vmatrix}-4  & -2 \\ 2 & 1 \end{vmatrix}
}$$
Evaluating the remaining second degree determinant: 
$$\large{
D_1(B) = -4 + 4 = 0
}$$
##### Compute $\large{D_2(B)}$: 
$$\large{D_2(B) = \begin{vmatrix}
1 & 13 & 3 & 4 & 5 \\ 
2 & 10 & 2 & 3 & 4 \\
2 & 11 & 1 & 2 & 3 \\ 
2 & 6 & 2 & 1 & 2 \\
2 & 3 & 2 & 2 & 1
\end{vmatrix}}$$
Subtract consecutive columns from the third column to the fourth column using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]:
$$\large{D_2(B) = 
\begin{vmatrix}
1 & 13 & -1 & -1 & 5\\ 
2 & 10 & -1 & -1 & 4 \\
2 & 11 & -1 & -1 & 3\\
2 & 6 & 1 & -1  & 2 \\ 
2 & 3 & 0 & 1 & 1
\end{vmatrix}
}$$
Subtract consecutive rows starting at the first row and ending at the fourth row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{
D_2(B) = \begin{vmatrix}
-1 & 3 & 0 & 0 & 1 \\ 
0 & -1 & 0 & 0 & 1 \\ 
0 & 5 & -2 & 0 & 1 \\ 
0 & 3 & 1 & -2 & 1 \\
2 & 3 & 0 & 1 & 1
\end{vmatrix}
}$$
Subtract consecutive rows starting at the first row and ending at the fourth row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]:
$$\large{D_2(B) = 
\begin{vmatrix} 
-1 & 4 & 0 & 0 & 0 \\ 
0 & -6 & 2 & 0 & 0 \\
0 & 2 & -3 & 2 & 0 \\
-2 & 0 & 1 & -3 & 0  \\ 
2 & 3 & 0 & 1 & 1
\end{vmatrix}
}$$
Use [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the fifth column: 
$$\large{
D_2(B) = 
\begin{vmatrix}
-1 & 4 & 0 & 0 \\
0 & -6 & 2 & 0 \\
0 & 2 & -3 & 2 \\
-2 & 0 & 1 & -3
\end{vmatrix}
}$$
Subtract the first row scaled by $\large{2}$ from the fourth row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{
D_2(B) = 
\begin{vmatrix}
-1 & 4 & 0 & 0 \\
0 & -6 & 2 & 0 \\
0 & 2 & -3 & 2 \\
0 & -8 & 1 & -3
\end{vmatrix}
}$$
Use [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the first column: 
$$\large{
D_2(B) = 
-\begin{vmatrix}
-6 & 2 & 0 \\
2 & -3 & 2 \\
-8 & 1 & -3
\end{vmatrix}
}$$
Subtract the third column from the first column using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]:
$$\large{
D_2(B) = -\begin{vmatrix} 
-6 & 2 & 0 \\
0 & -3 & 2 \\ 
-5 & 1 & -3
\end{vmatrix}
}$$
Add the third column scaled by $\large{3}$ to the first column [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]:
$$\large{
D_2(B) = -\begin{vmatrix} 
0 & 2 & 0 \\
-9 & -3 & 2 \\ 
-2 & 1 & -3
\end{vmatrix}
}$$ Use [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the first row: 
$$\large{
D_2(B) = 2\begin{vmatrix} 
-9 & 2 \\
-2 & -3
\end{vmatrix}
}$$
Evaluate the remaining second order determinant: 
$$\large{D_2(B) = 2 (27  + 4) = 2(31) = 62}$$

##### Compute $\large{D_3(B)}$: 
$$\large{
D_3(B) = \begin{vmatrix}
1 & 2 & 13 & 4 & 5 \\
2 & 1 & 10 & 3 & 4 \\
2 & 2 & 11 & 2 & 3 \\ 
2 & 2 & 6 & 1 & 2 \\
2 & 2 & 3 & 2 & 1
\end{vmatrix}
}$$
Subtracting the second column from the first and the fifth column from the fourth using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{
D_3(B) = \begin{vmatrix} 
-1 & 2 & 13 & -1 & 5 \\
1 &1 & 10 & -1 & 4 \\
0 & 2 & 11 & -1 & 3 \\
0 & 2 & 6 & -1 & 2 \\
0 & 2 & 3 & 1 &1 
\end{vmatrix}
}$$
Add the first row to the second row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_3(B) = 
\begin{vmatrix}
-1 & 2 & 13 & -1 & 5 \\
0 & 3 & 23 & -2 & 9 \\
0 & 2 & 11 & -1 & 3 \\
0 & 2 & 6 & -1 & 2 \\
0 & 2 & 3 & 1 & 1
\end{vmatrix}}$$
Using [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the first column: 
$$\large{D_3(B) = -\begin{vmatrix} 
3 & 23 & -2 & 9 \\
2 & 11 & -1 & 3 \\
2 & 6 & -1 & 2 \\ 
2 & 3 & 1 & 1
\end{vmatrix}}$$
Subtract the third row from the second and the fourth row from the third using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{
D_3(B) = -\begin{vmatrix} 
3 & 23 & -2 & 9 \\
0 & 5 & 0 & 1 \\ 
0 & 3 & -2 & 1 \\
2 & 3 & 1 & 1
\end{vmatrix}
}$$
Subtract the fourth row from the third and the third row from the second row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_3(B) =  - \begin{vmatrix}
3 & 23 & -2 & 9 \\ 
0 & 2 & 2 & 0 \\
-2 & 0 &-3 & 0 \\ 
2 & 3 & 1 & 1
\end{vmatrix}}$$
Add the third row to the fourth row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_3(B) = - 
\begin{vmatrix} 
3  & 23 & -2 & 9 \\
0 & 2 & 2 & 0 \\
-2 & 0 & -3 & 0 \\ 
0 & 3 & -2 & 1
\end{vmatrix}}$$
Subtract the fourth row scaled by $\large{9}$ from the first row using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]:
$$\large{D_3(B) = - \begin{vmatrix}
3 & -4 & 16 & 0 \\
0 & 2 & 2 & 0 \\
-2 & 0 & -3 & 0 \\ 
0 & 3 & -2 & 1
\end{vmatrix}}$$
Using [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the fourth column: 
$$\large{D_3(B) =  -\begin{vmatrix}
3 & -4 & 16 \\ 
0 & 2 &  2 \\ 
-2 & 0 & -3
\end{vmatrix}}$$
Subtract the second column to the third column using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{D_3(B) = -\begin{vmatrix} 
3 & -4 & 20 \\
0 & 2 & 0 \\
-2 & 0 & -3
\end{vmatrix}}$$
Use [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the second row:
$$\large{
D_3(B) = -2\begin{vmatrix} 
3 & 20 \\ -2 & -3
\end{vmatrix}
}$$
Extract a factor of $\large{-1}$ from the second row using [[The Linearity Property of Determinants#Corollary 1.45.1|Corollary 1.45.1]]:
$$\large{D_3(B) = 2 \begin{vmatrix}3 & 20 \\ 2  & 3\end{vmatrix}}$$
Evaluate the remaining second order [[Determinants#Definition(Determinants)|determinant]]:
$$\large{D_3(B) = 2(9 - 40) = -62}$$

##### Compute $\large{D_4(B)}$: 
$$\large{D_4(B) = \begin{vmatrix} 
1 & 2 & 3 & 13 & 5 \\ 
2 & 1 & 2 & 10 & 4 \\ 
2 & 2 & 1 & 11 & 3 \\
2 & 2 & 2 & 6 & 2 \\ 
2 & 2 & 2 & 3 & 1
\end{vmatrix}}$$
Subtract consecutive columns starting from the first column and ending at the second column using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{D_4(B) = \begin{vmatrix}
-1 & -1 & 3 & 13 & 5 \\ 
1 & -1 & 2 & 10 & 4 \\ 
0 & 1 & 1 & 11 &3 \\ 
0 & 0 & 2 & 6 & 2 \\
0 & 0 & 2 & 3 &1
\end{vmatrix}}$$
Add the second row to the first row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_4(B) = \begin{vmatrix} 
0 & -2 & 5 & 23 & 9 \\
1 & -1 & 2 & 10 & 4 \\ 
0 & 1 & 1 & 11 & 3 \\ 
0 & 0 & 2 & 6 & 2 \\ 
0 & 0 & 2 & 3 & 1
\end{vmatrix}}$$
Use [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the first column: 
$$\large{
D_4(B) = -\begin{vmatrix}
-2 & 5 & 23 & 9 \\
1 & 1 & 11 & 3 \\
0 & 2 & 6 & 2 \\ 
0 & 2 & 3 & 1
\end{vmatrix}
}$$
Scale the second row by $\large{2}$ and add it to the first row, additionally, subtract the fourth row from the third row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_4(B) = - \begin{vmatrix}
0 & 7 & 45 & 15 \\
1 & 1 & 11 & 3 \\ 
0 & 0 & 3 & 1  \\ 
0 & 2 & 3 & 1
\end{vmatrix}}$$
Preform [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the first column: 
$$\large{D_4(B) = -\begin{vmatrix}7 & 45 & 15 \\
0 & 3 & 1 \\ 
2 & 3 & 1\end{vmatrix}}$$
Subtract from the third row the second row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_4(B) = - \begin{vmatrix} 7 & 45 & 15 \\ 
-2 & 0 & 0  \\
2 & 3 & 1\end{vmatrix}}$$
Preform [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the second row: 
$$\large{D_4(B) = 2\begin{vmatrix}
 45 & 15 \\ 
3 & 1
\end{vmatrix}}$$
Evaluate the remaining second order [[Determinants#Definition(Determinants)|determinant]]: 
$$\large{D_4(B) = 2(45 - 45) = 0}$$
##### Compute $\large{D_5(B)}$: 
$$\large{ D_5(B) = \begin{vmatrix}
1 & 2 & 3 & 4 & 13 \\ 
2 & 1 & 2 & 3 & 10 \\
2 & 2 &1 & 2 & 11 \\ 
2& 2 & 2 & 1& 6 \\ 
2 & 2 & 2 & 2 & 3
\end{vmatrix}
}$$

Subtract consecutive columns from each other starting from the first column and ending on the third column using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{D_5(B) = \begin{vmatrix} 
-1 & -1 & -1 & 4 & 13 \\ 
1 & -1 & -1 & 3 & 10 \\ 
0 & 1 & -1 & 2 & 11 \\ 
0 & 0 & 1 & 1 & 6 \\ 
0 & 0 & 0 & 2 & 3
\end{vmatrix}}$$

Add the second row into the first row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_5(B) = \begin{vmatrix}
0 & -2 & -2 & 7 & 23 \\
 1 & -1 & -1 & 3 & 10 \\ 
 0 & 1 & -1 & 2 & 11 \\ 
 0 & 0 & 1 & 1 & 6 \\ 
 0 & 0 & 0 & 2 & 3
\end{vmatrix}}$$

Preform [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the first column: 
$$\large{D_5(B) = - \begin{vmatrix} 
-2 & -2 & 7 & 23 \\
1 & -1 & 2 & 11 \\
0 & 1 & 1 & 6 \\ 
0 & 0 & 2 & 3
\end{vmatrix}}$$

Scale the second row by $\large{2}$ and add the row to the first row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{D_5(B) = -\begin{vmatrix}
0 & -4 & 11 & 45  \\ 
1 & -1 & 2 & 11 \\ 
0 & 1 & 1 & 6 \\
0 & 0 & 2 & 3
\end{vmatrix}}$$

Preform [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the first column: 
$$\large{D_5(B) = \begin{vmatrix}
-4 & 11 & 45 \\ 
1 & 1 & 6 \\ 
0 & 2 & 3
\end{vmatrix}}$$

Scale the third row by $\large{2}$ and subtract from the second row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{
D_5(B) = \begin{vmatrix} 
-4 & 11 & 45 \\ 
1 & -3 & 0 \\ 
0 & 2 & 3
\end{vmatrix}
}$$

Scale the second row by $\large{4}$ and add to the first row using [[The Linearity Property of Determinants#Theorem 1.47a|Threoem 1.47a]]: 
$$\large{D_5(B) = \begin{vmatrix} 
0 & -1 & 45 \\ 
1 & -3 & 0 \\ 
0 & 2 & 3
\end{vmatrix}}$$

Use [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the first column: 
$$\large{D_5(B) = -\begin{vmatrix} 
-1 & 45 \\ 
2 & 3
\end{vmatrix}}$$

Evaluating the remaining second order [[Determinants#Definition(Determinants)|determinant]]: 
$$\large{D_5(B) = - ( -3 - 90 ) = 93}$$

##### Computing the Solution to the System: 
$$\large{\begin{eqnarray}
c_1 &=& \frac{D_1(B)}{D} &=& \frac{0}{31} &=& 0  \\
c_2 &=& \frac{D_2(B)}{D} &=& \frac{62}{31} &=& 2 \\ 
c_3 &=& \frac{D_3(B)}{D} &=& \frac{-62}{31} &=& -2 \\
c_4 &=& \frac{D_4(B)}{D} &=& \frac{0}{31} &=& 0 \\
c_5 &=& \frac{D_5(B)}{D} &=& \frac{93}{31} &=& 3
\end{eqnarray}}$$
