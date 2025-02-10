---
type: Academic
tags:
alias: Lin-Alg-1-PracticalEvaluationOfADeterminantExample
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
  section-name: "Practical Evaluation of Determinants",
  ISBN: "978-0-486-63518-7",
  template: {
    type: "object",
    name: "source-tbsection-obj",
    version: 1
  },
  book-title: "Linear Algebra",
  start-page: 16,
  end-page: 18,
  source-alias: "Lin-Alg-1-Ch1-Sec1-6"
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
#### Introduction: 
The following is an example used to demonstrate the utility of several theorems proven in the book in evaluating [[Determinants#Definition(Determinants)|determinants]]. 

#### Example 1.62:
Calculate the following determinant: 
$$\large{D = 
\begin{vmatrix} 
-2 & 5 & 0 & -1 & 3 \\ 
1 & 0 & 3 & 7 & -2  \\ 
3 & -1& 0 &5 &-5 \\
2& 6 &-4 &1 &2 \\
0 &-3 &-1 &2 &3
\end{vmatrix}
}
$$
First we use [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]] by multiplying row 5 by 3 and adding it to row 2:
$$\large{
D = 
\begin{vmatrix}
-2 & 5 & 0 & -1 & 3 \\
1 & -9 & 0 & 13 & 7 \\ 
3 & -1 & 0 & 5 & -5 \\
2 & 6 & -4 & 1 & 2 \\ 
0 & -3 & -1 & 2 & 3
\end{vmatrix}
}$$
Again we can use [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]] by multiplying row 5 by 4 and subtracting it from row 4: 
$$ \large{
D = 
\begin{vmatrix}
-2 & 5 & 0 & -1 & 3 \\ 
1 & -9 & 0 & 13 & 7 \\
3 & -1 & 0 & 5 & -5 \\
2 & 18 & 0 & -7 & -10\\
0 & -3 & -1 & 2 & 3
\end{vmatrix}
}
$$
Now we can use [[Minors of a Determinant#Theorem 1.54|Theorem 1.54]] to reduce the determinant. 
$$\large{
D = (-1)^{3+5}(-1)
\begin{vmatrix}
-2 & 5 & -1 & 3 \\
1 & -9 & 13 & 7 \\
3 & -1 & 5 & -5 \\ 
2 & 18 & -7 & -10 
\end{vmatrix} = -1 \begin{vmatrix}
-2 & 5 & -1 & 3 \\
1 & -9 & 13 & 7 \\
3 & -1 & 5 & -5 \\ 
2 & 18 & -7 & -10 
\end{vmatrix} 
}$$
Now use [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]] successively to produce 3 zeros by first multiplying row 2 by 2 and add it to row 1 then multiply row 2 by -3 and add it to row 3 and then subtract row 2 multiplied by 2 from row 4:
$$\large{
D = - 
\begin{vmatrix}
0 & -13 & 25 & 17 \\
1 & -9 & 13 & 7 \\
0 & 26 & -34 & -26 \\ 
0 & 36 & -33 & -24
\end{vmatrix}
}$$
Now use [[Minors of a Determinant#Theorem 1.54|Theorem 1.54]] again to reduce the determinant: 
$$\large{
D = (-1)(-1)^{1+2} 
\begin{vmatrix}
-13 & 25 & 17 \\
26 & -34 & -26 \\ 
36 & -33 & -24
\end{vmatrix} = 
\begin{vmatrix}
-13 & 25 & 17 \\
26 & -34 & -26 \\ 
36 & -33 & -24
\end{vmatrix}
}$$
Next we factor a 2 out of row 2 through [[The Linearity Property of Determinants#Corollary 1.45.1|Corollary 1.45.1]]. Then we use [[The Linearity Property of Determinants#Corollary 1.47a.1|Corollary 1.47a.1]] to add row 2 to row 1 and again to subtract row 2 from row 3. We Use [[The Linearity Property of Determinants#Corollary 1.45.1|Corollary 1.45.1]] again to factor another 4 out of row 1. 
$$\large{
D = 2 
\begin{vmatrix}
-13 & 25 & 17 \\
13 & -17 & -13 \\ 
36 & -33 & -24
\end{vmatrix} =2 
\begin{vmatrix}
0 & 8 & 4 \\ 
13 & -17 & -13 \\ 
10 & 1 & 2
\end{vmatrix} = 
2*4\begin{vmatrix}
0  & 2 & 1 \\
13 & -17 & -13 \\
10 &  1 & 2
\end{vmatrix}
}$$
We now use [[The Linearity Property of Determinants#Theorem 1.47a|Theorem 1.47a]] to produce the second zero by subtracting column 3 multiplied by 2 from column 2
$$\large{
D = 8
\begin{vmatrix}0 & 2 & 1 \\ 
13 & -17 & -13 \\
10 & 1 & 2
\end{vmatrix} = 8
\begin{vmatrix} 0 & 0 & 1 \\ 
13 & 9 & -13 \\ 
10 & -3 & 2 
\end{vmatrix}
}
$$
Reducing again using [[Minors of a Determinant#Theorem 1.54|Theorem 1.54]]:
$$\large{
D = 8 (-1)^{3+1} \begin{vmatrix}13 & 9 \\ 10 & -3 \end{vmatrix}
}$$
We can extract a factor of 3 using [[The Linearity Property of Determinants#Corollary 1.45.1|Corollary 1.45]] applied to column 2. Afterwards the computation of the determinant is trivial. 
$$\large{
D= 8* 3\begin{vmatrix}13 & 3 \\10 & -1 \end{vmatrix} = 8*3*(-13 - 30) = -8*3*43= -1032
}
$$
