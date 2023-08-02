
### Dosyalara Yazma

Go dilinde verileri dosyaya yazmak için os.Create() fonksiyonu kullanılır. Bu fonksiyon, yeni bir dosya oluşturur veya varolan bir dosyanın içeriğini siler. Dosya tutamaçı elde ettikten sonra, verileri bir Writer ile yazabilirsiniz.

Bu adımda Create ile yeni bir metin dosyası oluşturup içine veri yazalım.
Yeni bir go sayfasını oluşturun `vi create.go`

```
package main

import (
    "fmt"
    "os"
)

func main() {
    dosya, hata := os.Create("cikti.txt")
    if hata != nil {
        fmt.Println("Dosya oluşturulurken hata oluştu:", hata)
        return
    }
    defer dosya.Close()

    icerik := "Merhaba, bu dosyaya yazıldı!"
    _, hata = dosya.WriteString(icerik)
    if hata != nil {
        fmt.Println("Dosyaya yazılırken hata oluştu:", hata)
        return
    }

    fmt.Println("Veri başarıyla dosyaya yazıldı.")
}
```
Bu kodda, cikti.txt adında yeni bir dosya oluşturur ve içeriğe "Merhaba, bu dosyaya yazıldı!" yazısını yazar.
Bu çıktıyı alıyorsanız devam edebilirsiniz.

![cikti0.png](https://github.com/Gulnur-Altan/BB-Scenario/blob/master/go/Assets/cikti0.PNG)
