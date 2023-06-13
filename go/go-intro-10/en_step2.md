###  Matrix Operations - Addition and Subtraction

In this step, we will learn how to perform addition and subtraction operations on matrices in Go.

#### Matrix Addition

Matrix addition is performed by adding corresponding elements of two matrices together. The matrices should have the same dimensions for addition to be possible.
Create new page named like `matrix_addition.go`

An then paste the code or write with the editor
```
package main

import "fmt"

func main() {
    var i, j, rows, columns int

    var firstMat [10][10]int
    var secondMat [10][10]int
	var sumMat [10][10]int

    fmt.Print("Enter the Matrix rows and Columns = ")
    fmt.Scan(&rows, &columns)

    fmt.Println("Enter the First Matrix Items = ")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Scan(&firstMat[i][j])
        }
    }
    fmt.Println("Enter the Second Matrix Items = ")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Scan(&secondMat[i][j])
        }
    }
  	for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            sumMat[i][j]=firstMat[i][j]+secondMat[i][j]
        }
    }
	for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
        	    fmt.Print(sumMat[i][j], "  ")
        }
        fmt.Println()        
	}    	
}
```
Then run the code
```go run matrix_addition.go```

#### Matrix Subtraction

Matrix subtraction is performed by subtracting corresponding elements of one matrix from the corresponding elements of another matrix. As with addition, the matrices should have the same dimensions.

- Change the code for substraction of the matrix and test

If you can find the sum and substraction of the matrices you can continue..
