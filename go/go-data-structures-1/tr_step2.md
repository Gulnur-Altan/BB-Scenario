
#### AVL Ağacı:

AVL ağacı, sıralı bir veri yapısıdır ve her düğümde bir denge faktörü bulunur. Denge faktörü, ağacın dengesini korumak için kullanılır. AVL ağaçları, arama, ekleme ve silme işlemlerini O(log n) karmaşıklıkla yapabilirler.

*Go'da AVL ağaçları için üçüncü taraf paketler kullanılır, örneğin "github.com/emirpasic/gods" paketi bu tür veri yapılarını sağlar.

Yeni bir go dosyası oluşturalım: ```nano avlTree.go```

```
package main

import (
	"fmt"
	"github.com/emirpasic/gods/maps/treemap"
)

func main() {
	tree := treemap.NewWithIntComparator()

	tree.Put(3, "Apple")
	tree.Put(1, "Banana")
	tree.Put(2, "Orange")
	tree.Put(4, "Mango")

	value, found := tree.Get(2)
	if found {
		fmt.Println("Value:", value)
	}

	tree.Remove(3)

	fmt.Println("Size:", tree.Size())
	fmt.Println("Empty:", tree.Empty())
}
```

Çıktıyı görelim:

Value: Orange <br />
Size: 3 <br />
Empty: false <br />

Çıktı doğruysa devam edelim..
