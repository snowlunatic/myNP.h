# myNP.h

how to use the functions in myNP.h



### gaussElim()

```
void gaussElim(Matrix a, Matrix b, Matrix U, Matrix d, Matrix P, Matrix L);
```

This function gives you upper triangular matrix "U" for matrix "a". And also gives you "d" changed value of original vector "b". 

Matrix "L" is lower triangular matrix(it is not necessary for the function's purpose yet it just gives it). 

"P" is for the pivoting matrix if there is a pivoting, the rows will change (partial pivoting)

For "U", "P",  "L" must have a size of "a" and "d" must of the size of "d". Also it is better to initialize the elements as zeros (except for the matrix "P", it should be an identical matrix).

- a: matrix you will process.
- b: original vector.
- U: output that is desire to be the gauss elimination matrix of "a". 
- d: output that is desire to be the gauss elimination matrix of "b".
- P: pivot matrix, shows what rows has been pivoted.
- L: lower triangle matrix.



### backsub()

```
void backsub(Matrix U, Matrix d, Matrix x);
```

It is used when solving vector for upper triangular matrix and it's respective answer.
$$
Ux=d
$$
Matrix "U" and "d" is the input and "x" is the output.

- U: input matrix which is upper triangular matrix.
- d: input (column)vector which is a answer.
- x: output vector.



### fwdsub

```
void fwdsub(Matrix L, Matrix b, Matrix y);
```

It is used when solving vector for lower triangular matrix and it's respective answer.
$$
Ly=b
$$
Matrix "L" and "b" is the input and "y" is the ouput.

- L: input matrix which is lower triangular matrix.
- b: input column vector which is known as answer.
- y: output vector.



### rowExchange()

```
void rowExchange(Matrix A, int s, int k);
```

Changes rows for matrix A. Row of s and row of k will be exchanged for "A".

- s: row of s.
- k: row of k



### invMat()

```
void invMat(Matrix A, Matrix Ainv);
```

Used for getting inverse matrix of A.

- A: matrix you will inverse.
- Ainv: inverse matrix you get. the size must be same as A.



### eig()

```
Matrix eig(Matrix A);
```

It solve for eigen value of the matrix A. But the size of the matrix must not exceed 3X3.

the value will be processed as column vector.

- A: matrix for the eigen value.



### eigvec()

```
Matrix eigvec(Matrix A);
```

It solve for eigen vector of the matrix A. But the size of the matrix must not exceed 3X3.

- A: matrix for eigen vetor.







