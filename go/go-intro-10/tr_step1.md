
### Go'da Matrislere Giriş

Bu adımda matris kavramını ve onunla Go'da nasıl çalışılacağını tanıtacağız.

### Matris Nedir?
Bir matris, sayıların satır ve sütunlarda düzenlendiği iki boyutlu bir dizidir. Doğrusal cebirde kullanılan temel bir veri yapısıdır ve çeşitli bilimsel ve matematiksel hesaplamalarda yaygın olarak kullanılır.

### Go'da Matrislerle Çalışmak
Go, matrislerle verimli bir şekilde çalışmak için çeşitli paketler ve kütüphaneler sağlar. Popüler bir kütüphane olan Gonum, sayısal hesaplamalar ve bilimsel hesaplama için geniş işlevsellikler sunar.

Go sayfası oluşturun. Adı matrix.go olmalı.

```
package main

import "fmt"

func main() {
    var i, j, rows, columns int

    var matrix [10][10]int
    var transposeMatrix [10][10]int

    fmt.Print("Matrisin satır ve sütun sayısını girin = ")
    fmt.Scan(&rows, &columns)

    fmt.Println("Transpoze etmek için Matris Elemanlarını Girin = ")
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            fmt.Scan(&matrix[i][j])
        }
    }
    for i = 0; i < rows; i++ {
        for j = 0; j < columns; j++ {
            transposeMatrix[j][i] = matrix[i][j]
        }
    }
    fmt.Println("--- Transpoze Matris Elemanları ---")
    for i = 0; i < columns; i++ {
        for j = 0; j < rows; j++ {
            fmt.Print(transposeMatrix[i][j], "  ")
        }
        fmt.Println()
    }
}
```
Bu komutu yazın
```go run matrix.go```

Şimdi Go'da matrislerle çalışmanın temellerini öğrendiniz. Bir sonraki adımda, toplama, çıkarma ve çarpma gibi matris işlemlerini keşfedeceğiz.

Sağlanan örnek kodu sanal terminalinizde çalıştırıp çıktıyı görmeyi unutmayın.

Bir sonraki adıma ilerleyiniz.