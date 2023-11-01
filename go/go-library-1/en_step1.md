### Math Libraries

#### Basic functions

```
package main

import (
    "fmt"
    "math"
)

func main() {
    fmt.Println("Pi = ", math.Pi)
    fmt.Println("E = ", math.E)
    fmt.Println("Phi = ", math.Phi)
    fmt.Println("Sqrt of 2 = ", math.Sqrt2)
    fmt.Println("Naturla Log 2 = ", math.Ln2)
    fmt.Println("Naturla Log 10 = ", math.Ln10)
}
```

```go run constants.go```

You should see this output

Pi =  3.141592653589793 <br />
E =  2.718281828459045 <br />
Phi =  1.618033988749895 <br />
Sqrt of 2 =  1.4142135623730951 <br />
Naturla Log 2 =  0.6931471805599453 <br />
Naturla Log 10 =  2.302585092994046 <br />

returns absolute value of provided number

```
package main

import (
    "fmt"
    "math"
)

func main() {
    x := 50
    y := 100
    diff := x - y
    fmt.Println(diff)

    absolute_diff := math.Abs(float64(x) - float64(y))
    fmt.Println(absolute_diff)
}
```

*Type Casting

We can caste a type into other type by using the variable around the type name as type_name(variable)

```
a := 44
fmt.Printf("Type of a = %T \n", a)
fmt.Println("a = ", int(a))
fmt.Println("String Cast: ", string(a))
fmt.Println("Float Cast: ", float64(a))
```

big
Package big implements arbitrary-precision arithmetic (big numbers).
bits
Package bits implements bit counting and manipulation functions for the predeclared unsigned integer types.
cmplx
Package cmplx provides basic constants and mathematical functions for complex numbers.
rand
Package rand implements pseudo-random number generators suitable for tasks such as simulation, but it should not be used for security-sensitive work.

Lets use rand() and make a guess game.

```
package main

import (
 "fmt"
 "math/rand"
 "time"
)

func xrand(min, max int) int {
 rand.Seed(time.Now().Unix())
 return rand.Intn(max-min) + min
}
func main() {
 myrand := xrand(1, 10)
 tries := 0
 var guess int
 fmt.Scanf("%v", &guess)
 for guess != myrand {
  fmt.Println("Guess")

  tries++
  if guess > myrand {
   fmt.Println("Bigger")
   fmt.Scanf("%v", &guess)
  } else if guess < myrand {
   fmt.Println("Lower")
   fmt.Scanf("%v", &guess)
  } else {
   break
  }

 }
}
```

```go run randomTest.go```
