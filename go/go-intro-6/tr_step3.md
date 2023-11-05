
### Adım 3: Go'da Manuel Bellek Yönetimi

Go'nun çöp toplayıcısı oldukça etkili olsa da, make() ve delete() işlevlerini kullanarak manuel olarak bellek tahsis etmek ve serbest bırakmak mümkündür. Ancak, bu genellikle daha karmaşık ve hata eğilimli kodlara yol açabileceğinden önerilmez.

Bir dilim için bellek tahsisi yapmak için make() işlevini kullanmanın bir örneğini şöyle gösterebiliriz:

Bir önceki adımdaki dosyada değişiklik yapmadan farklı bir dosya oluşturup kodu çalıştırın.
dosya ismi -> `exp2.go`

```
package main

import "fmt"

func main() {
    slice := make([]int, 5, 10)
    slice[0] = 1
    slice[1] = 2
    slice[2] = 3
    slice[3] = 4
    slice[4] = 5
    fmt.Println(slice)
    // Dilim için belleği serbest bırak
    slice = nil
}
```

Bu programda, 5 uzunluğunda ve 10 değerli bir slice bellek tahsisi yapmak için make() işlevini kullanıyoruz. Ardından slice öğelerine değer atarız ve slice ın tamamını konsola yazdırırız. Son olarak, slice için belleği serbest bırakırız, bunu nil ile yapabiliriz.