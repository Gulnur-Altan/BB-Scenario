### Matrix Multiplication

Matrix multiplication is a fundamental operation that involves multiplying corresponding elements of rows from the first matrix with corresponding elements of columns from the second matrix and summing the results. The resulting matrix's dimensions depend on the dimensions of the original matrices.

To perform matrix multiplication in Go, follow these steps:

1- Create two matrices, one with dimensions (m x n) and the other with dimensions (n x p).
Create a go page like `matrix_multiply.go`,
and paste the code below

```
package main

import "fmt"

func main() {
    var rows, columns, i, j int

    var mat1 [10][10]int
    var mat2 [10][10]int
    var multiplicationnmat [10][10]int

    fmt.Print("Enter the Row and Column Numbers = ")
    fmt.Scan(&rows, &columns)

    fmt.Print("Enter the First Matrix Elements = ")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Scan(&mat1[i][j])
        }
    }

    fmt.Print("Enter the Second Matrix Elements = ")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Scan(&mat2[i][j])
        }
    }

    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            multiplicationnmat[i][j] = mat1[i][j] * mat2[i][j]
        }
    }
    fmt.Println("-- The Result of Matrix Multiplication --")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Print(multiplicationnmat[i][j], "\t")
        }
        fmt.Println()
    }
}
```
If you run the code like tthis `go run matrix_multiply.go` then 
put this inputs

Enter the Row and Column Numbers = 2 2 

Enter the First Matrix Elements = 1 2 3 4 

Enter the Second Matrix Elements = 1 2 3 4 

output is probably look like this \
-- The Result of Matrix Multiplication -- \
1       4  \
9       16

But it should be like this

1*1 + 2*3  1*2 + 2*4 \
3*1 + 4*3  3*2 + 4*4 

The Right Result of Matrix Multiplication is should be
7       10
15      22

Can you change the code for right output ?,if you see this output you can continue..
