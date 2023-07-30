## Kod Örneği 4: Fonksiyonları Birinci Sınıf İşlemci(First-class citizen) Olarak Kullanma 

first-class citizen: Belirli bir fonksiyon ya da nesnenin, diğer varlıklara özgü tüm özellikleri yapabimesidir örneğin bir değişkene atanabilme, fonksiyon argümanı olarak kullanılabilme, bir fonksiyondan geri dönme vb. gibi özellikler.

Go dilinde fonksiyonlar birinci sınıf işlemci olarak kabul edilir, yani değişkenlere atanabilir, diğer fonksiyonlara argüman olarak geçilebilir ve diğer fonksiyonlardan döndürülebilirler. Örneği inceleyip , test edin.

```
func carp(a, b int) int {
    return a * b
}

func islemUygula(islem func(int, int) int, a, b int) int {
    return islem(a, b)
}

func main() {
    sonuc := islemUygula(carp, 5, 3)
    fmt.Println(sonuc) // Çıktı: 15
}
```

Yukarıdaki kod örneğinde, islemUygula fonksiyonu başka bir fonksiyon olan islemi argüman olarak kabul eder. main fonksiyonunda, carp fonksiyonunu islem argümanı olarak geçerek 5 ve 3 sayılarının çarpımını hesaplarız.

## Sonuç 

Go fonksiyonları, kodu modüler bir şekilde düzenleyip yapılandırmada önemli bir rol oynar. Belirli görevleri kapsülleyerek programınız boyunca tekrar kullanmanıza olanak sağlarlar. Bu senaryoda verilen örneklerle, Go fonksiyon kullanımını test ettiniz.
