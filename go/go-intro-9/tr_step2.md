
## Kod Örneği 2: Birden Fazla Değer Döndüren Fonksiyon

Go fonksiyonları birden fazla değer döndürebilir, bu da oldukça kullanışlı bir özelliktir. İşte iki sayının bölümünü ve kalanını hesaplayan bir fonksiyon örneği:

```
package main

import (
	"fmt"
)

func bol(a, b int) (int, int) {
    bolum := a / b
    kalan := a % b
    return bolum, kalan
}

func main() {
	b, k := bol(10, 3)

	fmt.Println("Bölüm: ", b)
	fmt.Println("Kalan: ", k)
}
```
Yukarıdaki bol fonksiyonunda, a sayısını b sayısına böler ve sonucunda bölümü ve kalanı ayrı ayrı değerler olarak döndürür.

Go fonksiyonları bu esnek özellikleriyle programlamayı daha kolay ve hızlı hale getirir. Daha fazla örnek ve pratiklerle Go dilindeki fonksiyonları daha iyi anlayabilir ve projelerinizde etkili bir şekilde kullanabilirsiniz. 