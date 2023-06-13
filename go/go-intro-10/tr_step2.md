###  Matris İşlemleri - Toplama ve Çıkarma

Bu adımda, Go'da matrisler üzerinde toplama ve çıkarma işlemlerini nasıl gerçekleştireceğimizi öğreneceğiz.

#### Matris ile Toplama

Matris toplaması, iki matrisin karşılık gelen elemanlarını birbirine ekleyerek gerçekleştirilir. Toplama işlemi yapılabilmesi için matrislerin aynı boyutlarda olması gerekmektedir.
 `matrix_addition.go` adında yeni bir sayfa oluşturun.


Ardından, aşağıdaki kodu yapıştırın veya editor ile yazın: 
```
package main

import "fmt"

func main() {
    var i, j, rows, columns int

    var firstMat [10][10]int
    var secondMat [10][10]int
	var sumMat [10][10]int

    fmt.Print("Matrisin satır ve sütun sayısını girin = ")
    fmt.Scan(&rows, &columns)

    fmt.Println("Birinci Matris Elemanlarını Girin = ")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Scan(&firstMat[i][j])
        }
    }
    fmt.Println("İkinci Matris Elemanlarını Girin = ")
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

#### Matris ile Çıkarma

Matrislerde çıkarma, bir matrisin elemanlarından diğer matrisin karşılık gelen elemanları çıkarılarak gerçekleştirilir. Toplama işlemiyle olduğu gibi, matrislerin aynı boyutlarda olması gerekmektedir.

Kodu matris toplama işlemini, çıkarma işlemine çevirin ve test edin.
Eğer matrislerin toplamını ve çıkarımını bulabiliyorsanız, devam edebilirsiniz...
