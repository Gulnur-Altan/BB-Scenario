### Step 2 : Slices

Slices are a dynamic version of arrays, with no fixed size. They are declared using the make function, and can be resized using the append function. Here's an example of how to create and modify a slice:

First create a go file named `nano slice.go`

Paste the code and execute

```
package main

import (
	"fmt"
)

func main() {
	s := make([]int, 3) // create a slice of 3 integers
	s[0] = 1            // set the first element to 1
	s[1] = 2            // set the second element to 2
	s[2] = 3            // set the third element to 3
	s = append(s, 4)    // add a new element to the slice
	for i := 0; i < len(s); i++{
	fmt.Println(s[i])
	}
}
```
If you see this output ,you can continue

*1* \
*2* \
*3* \
*4* \
*5*
