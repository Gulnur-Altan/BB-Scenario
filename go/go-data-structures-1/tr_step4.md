
#### Trie (Önek Ağacı):

Trie veya önek ağacı, metin işleme uygulamalarında sıkça kullanılan bir veri yapısıdır. Her düğüm, metinlerin karakterlerini temsil eder ve kelime veya önekler bu düğümleri birleştirir. Bu, hızlı metin eşleştirmeleri ve aramaları sağlar.
* Go'da'trie veri yapısını uygulamak için üçüncü taraf paketler bulunur. Örneğin, "github.com/derekparker/trie" paketi bu tür veri yapılarına olanak tanır.

Yeni bir go dosyası oluşturalım: ```nano trie.go```

```
package main

import (
	"fmt"
	"github.com/derekparker/trie"
)

func main() {
	t := trie.New()

	t.Add("apple", 1)
	t.Add("banana", 2)
	t.Add("orange", 3)

	fmt.Println("Contains 'apple':", t.Has("apple"))

	value, _ := t.Get("banana")
	fmt.Println("Value for 'banana':", value)

	t.Remove("orange")

	fmt.Println("Prefix search:")
	t.PrefixSearch("ap", func(key string, value interface{}) bool {
		fmt.Printf("Key: %s, Value: %v\n", key, value)
		return true
	})
}

```
