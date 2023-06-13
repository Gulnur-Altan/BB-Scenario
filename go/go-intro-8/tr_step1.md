
### Adım 1: Diziler (Arrays)

Bir dizi, aynı türdeki elemanların sabit bir boyutta toplandığı bir veri yapısıdır. Go dilinde, aşağıdaki sözdizimini kullanarak bir dizi oluşturabilirsiniz:

*var numbers [5]int*

Bu, uzunluğu 5 olan int türünde bir numbers dizisi oluşturur. Dizinin elemanlarına, 0'dan başlayan index numaralarını kullanarak erişebilirsiniz:


*numbers[0] = 10* \
*numbers[1] = 20* \
*numbers[2] = 30* \
*numbers[3] = 40* \
*numbers[4] = 50* 

Ayrıca, bir dizi oluşturup başlatmak için kısa bir sözdizimi de kullanabilirsiniz:

*numbers := [5]int{10, 20, 30, 40, 50}*

Dizinin elemanlarını yazdırmak için bir döngü kullanabilirsiniz.
İlk olarak,  `nano array.go` komutunu kullanarak bir go dosyası oluşturun.

Ardından kodu yapıştırın ve çalıştırın:


```
package main

import (
	"fmt"
)

func main() {
	var numbers [5]int
	numbers[0] = 10
	numbers[1] = 20
	numbers[2] = 30
	numbers[3] = 40
	numbers[4] = 50

	for i := 0; i < len(numbers); i++ {
    fmt.Println(numbers[i])
}
}
```

`go run array.go`

*10* \
*20* \
*30* \
*40* \
*50*

çıktısını alıyorsanız devam edebilirsiniz.
