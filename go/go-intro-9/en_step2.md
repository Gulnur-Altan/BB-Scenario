
## Code Example 2: Function with Multiple Return Values

Go functions can return multiple values, which is a handy feature. Here's an example of a function that calculates the quotient and remainder of two numbers:

```
package main

import (
	"fmt"
)

func divide(a, b int) (int, int) {
    quotient := a / b
    remainder := a % b
    return quotient, remainder
}

func main() {
	q,r:=divide(10, 3)

	fmt.Println("The quotient is: ", q)
	fmt.Println("The remainder is: ", r)
}
```
In the divide function above, we divide a by b and return the quotient and remainder as separate values.
