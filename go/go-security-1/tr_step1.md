
#### Hash örneği

Go dilinde ile bir verinin hash olarak saklanmasını öğrenelim. Bu örnekte saklanacak bir verinin MD5 dönüşümü ile çevrimi gösterilmektedir.

```
package main

import (
    "crypto/md5"
    "encoding/hex"
    "fmt"
)

func getMD5Hash(message string) string {
    hash := md5.Sum([]byte(message))
    return hex.EncodeToString(hash[:])
}

func main() {
    password := "gizliveri"
    fmt.Println("MD5 hashli değeri: ", getMD5Hash(password))
}
```

MD5 hashli değeri:  bb120293efeb518fafd7f750ec1839ff </br>

buna benzer bir çıktı alıyorsanız,devam edebilirsiniz.