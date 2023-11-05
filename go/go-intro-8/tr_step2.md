### Adım 2: Dilimler (Slices)

Slice yapısı, sabit bir boyutu olmayan, dinamik bir dizi yapısını ifade eder. make fonksiyonu kullanılarak tanımlanırlar ve append fonksiyonu kullanılarak boyutları değiştirilebilir. Bir slice nasıl oluşturulur ve değiştirilir, örnek olarak aşağıda verilmiştir:

İlk olarak,  `slice.go` isimli bir go dosyası oluşturun.

Ardından kodu yapıştırın ve çalıştırın,

```
package main

import (
	"fmt"
)

func main() {
	s := make([]int, 3) // 3 integer değer içeren bir slice oluşturur
	s[0] = 1            // ilk sayı 1
	s[1] = 2            // 2
	s[2] = 3            // 3 e eşitle
	s = append(s, 4)    // slice a yeni eleman ekler
	for i := 0; i < len(s); i++{
	fmt.Println(s[i])
	}
}
```

Bu çıktıyı almalısınız doğruysa,devam edebilirsiniz.

*1* \
*2* \
*3* \
*4* \
*5*