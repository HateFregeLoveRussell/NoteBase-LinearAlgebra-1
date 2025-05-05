---
type: Academic
tags: [practice]
alias: Lin-Alg-1-Ch1-PP-Q7
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
  template: {
    version: 1,
    type: "object",
    name: "source-tbsection-obj"
  },
  end-page: 30,
  type: "tbsection",
  ISBN: "978-0-486-63518-7",
  class-alias: "Lin-Alg-1",
  start-page: 28,
  source-alias: "Lin-Alg-1-Ch1-PP",
  book-title: "Linear Algebra",
  section-name: "Chapter 1 Practice Problems"
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
template: {name: class-textbook-practice-problem, version: 1}
---
### Problem Statement:
Calculate the two [[Determinants#Definition(Determinants)|determinants]] below: 
$$\large{\Delta_1 = \begin{vmatrix}246 & 427 & 327 \\ 
1014 & 543 & 443 \\ 
-342 & 721 & 621
\end{vmatrix}}$$
$$\large{\Delta_2 = \begin{vmatrix}
2 & 1 & 1 & 1 & 1 \\
1 & 3 & 1 & 1 & 1 \\ 
1 & 1 & 4 & 1 & 1 \\
1 & 1 & 1 & 5 & 1 \\ 
1 & 1 & 1 & 1 & 6
\end{vmatrix}}$$
#### Solution: 

##### Solution for $\large{\Delta_1}$: 
Extracting a factor of $\large{6}$ using [[The Linearity Property of Determinants#Corollary 1.45|Corollary 1.45]] from $\large{\Delta_1}$: 
$$\large{\Delta_1 = 
6*\begin{vmatrix}41 & 427 & 327 \\ 
169 & 543 & 443 \\ 
-57 & 721 & 621\end{vmatrix}}$$
Subtracting from the second column the third column using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{\Delta_1 = 6*\begin{vmatrix}41 & 100 & 327 \\
169 & 100 & 443 \\ 
-57 & 100 & 621\end{vmatrix}}$$
Now subtracting from the third column, the second column scaled by $\large{3}$ using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]: 
$$\large{\Delta_1 = 6 * \begin{vmatrix}41 & 100 & 27 \\ 169 & 100 & 143 \\ -57 & 100 &  321\end{vmatrix}}$$We now factor our a $\large{10^2}$ using [[The Linearity Property of Determinants#Corollary 1.45|Corollary 1.45]]:
$$\large{\Delta_1 = 6 * 10^2 *\begin{vmatrix}41 & 1 &  27 \\ 169 & 1 &143 \\ -57 & 1 & 321 \end{vmatrix}}$$
Subtracting from the first row the second and third row using [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]]: 
$$\large{\Delta_1 = 6 * 10^2  \begin{vmatrix}98 & 0 & -294 \\ 
226 & 0 & -178 \\ -57 & 1 & 321\end{vmatrix}}$$
We can now preform [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the second column: 
$$\large{\Delta_1 = -6 * 10^2 \begin{vmatrix}98 & -294 \\ 226 & -178 \end{vmatrix}}$$
Factoring out a factor of $\large{7^2}$ from the first row and a factor of $\large{2^2}$ from the second row and a factor of $\large{-1}$ from the second column using [[The Linearity Property of Determinants#Corollary 1.45|Corollary 1.45]] and [[The Linearity Property of Determinants#Corollary 1.45.1|Corollary 1.45.1]]: 
$$\large{
\Delta_1 = 6*10^2*7^2*2^2 \begin{vmatrix} 1 & 3 \\ 113 & 89\end{vmatrix}
}$$

Evaluating the second degree [[Determinants#Definition(Determinants)|determinant]]: 
$$\large{\Delta_1 = 6*10^2*2^2*7^2(89 -3*113) = -29400000}$$

##### Solution for $\large{\Delta_2}$:
Subtracting consecutive rows from each other from the first row until the fourth row using [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]]
$$\large{\Delta_2 = \begin{vmatrix}1 & -2 &0 & 0 & 0 \\
0 & 2 & -3 & 0 & 0 \\
0 & 0 & 3 & -4 & 0 \\
0 & 0 & 0 & 4 & -5 \\
1 & 1 & 1 & 1 & 6\end{vmatrix}}
$$
Now using [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] on the first column: 
$$\large{
\Delta_2 = \begin{vmatrix} 
2 & -3 & 0 & 0 \\
0 & 3 & -4 & 0 \\ 
0 & 0 & 4 & -5 \\
1 & 1 & 1 & 6
\end{vmatrix} + 
\begin{vmatrix}
-2 & 0 & 0 & 0 \\
2 & -3 & 0 & 0 \\ 
0 & 3 & -4 & 0 \\
0 & 0 & 4 & -5
\end{vmatrix}
}$$
We recognise the second term as a [[The Triangular Determinant#Definition|Triangular Determinant]] and hence, using [[The Triangular Determinant#Theorem 1.55b|Theorem 1.55b]] arrive at: 
$$\large{\Delta_2 = \begin{vmatrix}
2 & -3 & 0 & 0 \\ 
0 & 3 & -4 & 0 \\ 
0 & 0 & 4 & -5 \\ 
1 & 1 & 1 & 6
\end{vmatrix} + 2* 3 * 4 * 5 }$$
Now using [[Minors of a Determinant#Theorem 1.54|Cofactor Expansion]] again on the first column of the first term: 
$$\large{\Delta_2  = 
2\begin{vmatrix}3 & -4 & 0 \\ 0 & 4 & -5 \\ 1 & 1 & 6 \end{vmatrix}
- \begin{vmatrix}-3 & 0 & 0 \\ 3 & -4 & 0 \\ 0 & 4 & -5 \end{vmatrix}
+ 120}$$
we recognise that the second term is again [[The Triangular Determinant#Definition|triangular]] and so using [[The Triangular Determinant#Theorem 1.55b|Theorem 1.55b]].
$$\large{\Delta_2 = 
2\begin{vmatrix}3 & -4 & 0 \\ 0 & 4 & -5 \\ 1 & 1 & 6 \end{vmatrix}+ 60 + 120}$$
Using [[Minors of a Determinant#Theorem 1.53|Cofactor Expansion]] on the first column of the first term: 
$$\large{
\Delta_2 = 6 \begin{vmatrix}4 & -5 \\ 1 & 6\end{vmatrix} + 2\begin{vmatrix} -4 & 0 \\ 4 & -5 \end{vmatrix} + 180
}$$
Now computing the second order [[Determinants#Definition(Determinants)|determinants]] directly: 
$$\large{\Delta_2 = 6(24 + 5) + 2(20) + 180 = 394}$$
