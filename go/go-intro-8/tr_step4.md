### Step 4: Structs

Struct yapısı, ilgili değerleri tek bir veri yapısında gruplandırmanın bir yoludur. Type anahtar sözcüğü kullanılarak bildirilirler ve nokta işareti kullanılarak erişilebilirler. İşte bir struct yapısının nasıl oluşturulup değiştirileceğine dair bir örnek:

Yeni bir sayfa oluşturalım.`struct.go`

```
package main

import (
	"fmt"
)

type Person struct {
	Name string
	Age  int
}

func main() {
	p := Person{Name: "Ada Lovelace", Age: 30}      // yeni bir kişi oluşturur
	p.Age = 36
	fmt.Println(p)
	
	var person2 Person                              // yeni bir kişi oluşturur 
	person2.Name= "Susan Wojcicki"
	person2.Age= 54
	fmt.Println(person2)
	
	person3 := new(Person)                          // yeni bir kişi oluşturur
	person3.Age=26
}

```

*{Ada Lovelace 36}* \
*{Susan Wojcicki 54}*

Çıktısını görüyorsanız ,adımları başarı ile tamamladınız demektir.