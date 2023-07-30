## Kod Örneği 3: Değişken Sayıda Argüman Alan Fonksiyon
Go, fonksiyonlara ... sözdizimi kullanarak değişken sayıda argüman geçme olanağı tanır. İşte birden fazla sayının ortalamasını hesaplayan bir fonksiyon örneği:

```
func ortalamaHesapla(sayilar ...float64) float64 {
    toplam := 0.0
    for _, sayi := range sayilar {
        toplam += sayi
    }
    return toplam / float64(len(sayilar))
}
```

Yukarıdaki ortalamaHesapla fonksiyonunda, sayilar parametresi ... ile başlar, bu da onun değişken sayıda ondalık sayı argümanını kabul edebileceğini belirtir. Fonksiyon, verilen tüm sayıların toplamını hesaplar ve ortalamasını döndürür.

Bu fonksiyonu yazın ve test edin:

```
package main

import (
	"fmt"
)

func ortalamaHesapla(sayilar ...float64) float64 {
    toplam := 0.0
    for _, sayi := range sayilar {
        toplam += sayi
    }
    return toplam / float64(len(sayilar))
}

func main() {
	ortalama := ortalamaHesapla(10.5, 7.2, 4.8, 9.1, 6.6)

	fmt.Println("Ortalama: ", ortalama)
}
```