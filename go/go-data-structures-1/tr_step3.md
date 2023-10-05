#### Graf Veri Yapısı:

Açıklama: Graf, nesnelerin düğümlerle ve bu düğümleri birleştiren kenarlarla temsil edildiği bir veri yapısıdır. Graf algoritmaları, düğümler arasındaki ilişkileri analiz etmek ve belirli problemleri çözmek için kullanılır.

* Go'da graf veri yapısı için bazı üçüncü taraf paketler bulunur. Örneğin, "github.com/yourbasic/graph" paketi, graf işlemlerini destekler.

Yeni bir go dosyası oluşturalım: ```nano graf.go```

```
package main

import (
	"fmt"
	"github.com/yourbasic/graph"
)

func main() {
	g := graph.New(5) // 5 düğümlü bir graf oluşturuluyor

	g.AddBoth(0, 1) // Kenar ekleniyor
	g.AddBoth(0, 2)
	g.AddBoth(1, 3)
	g.AddBoth(2, 4)

	// Dolaşma işlemi gerçekleştiriliyor
	graph.BFS(g, 0, func(v, w int, _ int64) {
		fmt.Printf("Düğüm %d -> Düğüm %d\n", v, w)
	})
}
```

Çıktıyı görelim:

Düğüm 0 -> Düğüm 2 <br />
Düğüm 0 -> Düğüm 1 <br />
Düğüm 2 -> Düğüm 4 <br />
Düğüm 1 -> Düğüm 3 <br />

Çıktı doğruysa devam edelim..
