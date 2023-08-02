
## Go Dilinde Dosya İşlemleri: Kod Örnekleri ile Bir Giriş

Go, Golang olarak da bilinen güçlü ve verimli bir programlama dilidir ve kapsamlı bir standart kütüphane sunar. Bu kütüphane içerisinde dosya işlemleri için kapsamlı destek bulunmaktadır. Bu senaryoda, Go dilinde dosya işlemlerinin temellerini keşfedecek ve okuma, yazma ve dosyalarla çalışma konusunda nasıl kod örnekleri kullanılacağını göstereceğiz.

### Dosyaların Açılması ve Okunması

Go dilinde, dosyaları açmak ve içeriğini okumak için os paketi kullanılır. os.Open() fonksiyonu bir dosyayı açmak için kullanılır ve ardından içeriği bir Reader ile okuyabilirsiniz.

İlk olarak bir text dosyası oluşturalım `vi ornek1.txt`
İçine ` Bulut Bilisim 2023` yazalım (ipucu: Yazı yazabilmek için i harfine basıp insert modu aktif edin)
kaydet ve çık (ipucu: ESC + :wq! + enter )

Bir metin editörü ile Go sayfası oluşturun. Adı file.go olabilir `vi file.go`
Kodu editörde değiştirip dosyaismi kısmını ornek1 yapalım ve >> iconu ile file.go içine atalım.

```
package main

import (
    "fmt"
    "os"
)

func main() {
    dosya, hata := os.Open("dosyaismi.txt")
    if hata != nil {
        fmt.Println("Dosya açılırken hata oluştu:", hata)
        return
    }
    defer dosya.Close()

    veri := make([]byte, 100)
    sayac, hata := dosya.Read(veri)
    if hata != nil {
        fmt.Println("Dosya okunurken hata oluştu:", hata)
        return
    }

    fmt.Printf("Okunan %d byte: %s\n", sayac, veri[:sayac])
}
```
Kodu çalıştıralım `go run file.go`

*Not* ilk adımda go yüklenmediyse bu adımda hata alırsınız.

Yukarıdaki kodda, ornek.txt adlı bir dosya açıp,
içeriğini bir byte dizisine okutup, okunan veriyi ekrana yazdırdınız.

node1 # go run x.go /
Okunan 5 byte: gggg /
Buna benzer bir çıktı aldıysanız, devam edebilirsiniz
