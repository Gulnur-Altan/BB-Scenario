## 3. Egzersiz

# Challenge Variables

Ekrana adınızı,soyadınızı,yaşınızı ve öğrenci olma durumunuzu yazdıran kodu yazınız.

ad        -> string <br />
soyad     -> string  <br />
yaş       -> integer <br />
öğrenci mi-> boolean <br />

Yeni bir sayfa oluşturalım. File->New file <br />
isim -> ```variables2.go```

Örnek Kod:
```
package main
import "fmt"

func main() {
    age := 25
    name := "Alice"

    fmt.Println("Name:", name)
    fmt.Println("Age:", age)
}
```
Kodu yazalım, <br />
Çalıştıralım <br />
```
go run variables2.go
```
Çıktı düzgünse başardınız demektir,Golang de değişken tanımlamak bu kadar kolay :)
