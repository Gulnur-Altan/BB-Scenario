### Matris Çarpımı
Matris çarpımı, ilk matrisin satırlarının karşılık gelen elemanlarını ikinci matrisin sütunlarındaki karşılık gelen elemanlarla çarparak sonuçları toplamayı içeren temel bir işlemdir. Elde edilen matrisin boyutları, orijinal matrislerin boyutlarına bağlıdır.

Go'da matris çarpımını gerçekleştirmek için aşağıdaki adımları takip edin:

1- Birinci matrisin boyutları (m x n), ikinci matrisin boyutları ise (n x p) olacak şekilde iki matris oluşturun.
`matrix_multiply.go`, gibi bir Go sayfası oluşturun 
ve aşağıdaki kodu yapıştırın:


```
package main

import "fmt"

func main() {
    var rows, columns, i, j int

    var mat1 [10][10]int
    var mat2 [10][10]int
    var multiplicationmat [10][10]int

    fmt.Print("Satır ve Sütun Sayılarını Girin = ")
    fmt.Scan(&rows, &columns)

    fmt.Print("Birinci Matrisin Elemanlarını Girin = ")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Scan(&mat1[i][j])
        }
    }

    fmt.Print("İkinci Matrisin Elemanlarını Girin = ")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Scan(&mat2[i][j])
        }
    }

    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            multiplicationmat[i][j] = 0
            for k := 0; k < columns; k++ {
                multiplicationmat[i][j] += mat1[i][k] * mat2[k][j]
            }
        }
    }
    fmt.Println("-- Matris Çarpımının Sonucu --")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Print(multiplicationmat[i][j], "\t")
        }
        fmt.Println()
    }
}
```

Eğer `go run matrix_multiply.go` şeklinde kodu çalıştırırsanız ve 
aşağıdaki girdileri girerseniz:

Satır ve Sütun Sayılarını Girin = 2 2

Birinci Matrisin Elemanlarını Girin = 1 2 3 4

İkinci Matrisin Elemanlarını Girin = 1 2 3 4

Çıktı muhtemelen şuna benzeyecektir: \
-- Matris Çarpımının Sonucu -- \
1       4  \
9       16

Bu işlem her bir elemanı kendi index değerinde bulunan eleman ile çarpar,
 sonuç doğru olmalı ve şu şekilde olmalıdır:

1*1 + 2*3  1*2 + 2*4 \
3*1 + 4*3  3*2 + 4*4 

Matris Çarpımının Doğru Sonucu:
7       10
15      22

Doğru çıktıyı almak için kodu değiştirin ,sonucu gördüğünüzde devam edebilirsiniz..
