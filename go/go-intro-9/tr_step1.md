##  Go Fonksiyonlarının Anlaşılması: Kod Örnekleri ile Bir Giriş

Go, Golang olarak da bilinen güçlü ve verimli bir programlama dilidir ve basitliği ile eş zamanlılık özellikleriyle tanınır. Go programlamasının temel yapı taşlarından biri fonksiyon kavramıdır. Bu makalede, Go fonksiyonlarının çeşitli yönlerini keşfedecek ve kullanımlarını göstermek için kod örnekleri sunacağız.

Fonksiyonların Tanımlanması
Go'da bir fonksiyon, belirli bir görevi yerine getiren kod bloğudur. Bu görev, programın farklı bölümlerinden çağrılabilir. Bir fonksiyonun Go'da tanımlanma sözdizimi aşağıdaki gibidir:

```
func fonksiyonAdı(parametre1 tip1, parametre2 tip2) dönüşTipi {
    // Fonksiyon gövdesi
    // Çalıştırılacak kodlar
    return sonuç
}
```
Bir Go fonksiyonunun bileşenlerini inceleyelim:

func anahtar kelimesi: Fonksiyon tanımlamak için kullanılır.
fonksiyonAdı: Bu, fonksiyonun tanımlayıcısıdır. Fonksiyonun amacını açıklayan anlamlı bir isim seçilmelidir.
parametre1, parametre2: Bunlar fonksiyona giren parametrelerdir. Her parametre kendi tipini takip eder.
dönüşTipi: Fonksiyonun döndürdüğü değerin tipini temsil eder. Eğer fonksiyon herhangi bir değer döndürmüyorsa, dönüşTipi belirtilmez.
return: Bu anahtar kelime, fonksiyondan bir değer döndürmek için kullanılır. Fonksiyonun dönüş tipi olmadığı durumlarda return ifadesi opsiyoneldir.

### Kod Örneği 1: Basit Bir Toplama Fonksiyonu

Toplama işlemini gerçekleştiren basit bir fonksiyon örneğiyle başlayalım:

```
package main

import (
	"fmt"
)

func sayilariTopla(a, b int) int {
    return a + b
}

func main() {
	toplam := sayilariTopla(10, 20)

	fmt.Println("Toplam: ", toplam)
}
```

Yukarıdaki kodda, iki tamsayı a ve b parametreleri alan sayilariTopla adında bir fonksiyon tanımlıyoruz. Fonksiyon, a ve b değerlerinin toplamını tamsayı olarak döndürüyor. Kodu test edebilir ve devam edebilirsiniz.