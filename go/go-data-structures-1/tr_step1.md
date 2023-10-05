### Go ile Advanced Veri Yapıları


#### Heap (Yığın) Veri Yapısı:

Heap, verileri hiyerarşik bir şekilde düzenleyen ve en yüksek veya en düşük değere hızlı erişim sağlayan bir ağaç tabanlı veri yapısıdır. Birçok algoritma, özellikle öncelik sıralamalarını ve işlem kuyruklarını uygularken heap'i kullanır.

* Go'da heap, "container/heap" paketiyle uygulanır. Bu paket, heap veri yapısının temel işlemlerini (ekleme, çıkarma, vb.) kolayca yapmanızı sağlar

Yeni bir go dosyası oluşturalım: ```nano heap.go```

```
package main

import (
	"container/heap"
	"fmt"
)

type MinHeap []int

func (h MinHeap) Len() int           { return len(h) }
func (h MinHeap) Less(i, j int) bool { return h[i] < h[j] }
func (h MinHeap) Swap(i, j int)      { h[i], h[j] = h[j], h[i] }

func (h *MinHeap) Push(x interface{}) {
	*h = append(*h, x.(int))
}

func (h *MinHeap) Pop() interface{} {
	old := *h
	n := len(old)
	x := old[n-1]
	*h = old[:n-1]
	return x
}

func main() {
	h := &MinHeap{9, 5, 7, 1, 3}
	heap.Init(h)

	heap.Push(h, 4)
	fmt.Printf("Min value: %d\n", (*h)[0])

	for h.Len() > 0 {
		fmt.Printf("%d ", heap.Pop(h))
	}
}
```

Çalıştırmak için: ```go run heap.go```

Çıktıyı görelim:

Min value: 1 <br />
1 3 4 5 7 9  <br />

Çıktı doğruysa devam edelim..
