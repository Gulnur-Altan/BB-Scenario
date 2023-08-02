
### Dosya İşlemleri ve Değişiklikler

Go dilinde dosya işlemleriyle ilgili başka birçok fonksiyon da bulunmaktadır, bunlar arasında dosya adını değiştirme, dosya silme ve dosyanın var olup olmadığını kontrol etme gibi işlemler yer alır. 
Son adımda bu işlemleri gerçekleştirelim.
İlk olarak 1 text dosyasını oluşturun `vi eski.txt`, içine random yazı yazıp çıkın
(yazı yazabilmek için i harfine basıp insert modu aktif edin)

Go sayfasını olşturun `vi fileOperations.go`

```
package main

import (
    "fmt"
    "os"
)

func main() {
    // Dosya adını değiştirme
    hata := os.Rename("eski.txt", "yeni.txt")
    if hata != nil {
        fmt.Println("Dosya adı değiştirilirken hata oluştu:", hata)
        return
    }
}
```
`go run fileOperations.go`

ls komutu ile yeni.txt oluşturulmuş mu kontrol edin,

Yeni go sayfasını olşturun `vi fileOperations2.go`
Oluşturduğunuz yeni dosyayı sildirin,

```
package main

import (
    "fmt"
    "os"
)

func main() {

    // Dosya silme
    hata = os.Remove("yeni.txt")
    if hata != nil {
        fmt.Println("Dosya silinirken hata oluştu:", hata)
        return
    }

    // Dosyanın var olup olmadığını kontrol etme
    if _, hata := os.Stat("yeni.txt"); hata == nil {
        fmt.Println("Dosya mevcut.")
    } else {
        fmt.Println("Dosya mevcut değil.")
    }
}
```

`go run fileOperations2.go`
ls ile yeni.txt dosyasının artık olmadığını kontrol edin.

