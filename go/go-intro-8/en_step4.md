### Step 4: Structs

Structs are a way to group related values together into a single data structure. They are declared using the type keyword, and can be accessed using the dot notation. Here's an example of how to create and modify a struct:
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
	p := Person{Name: "Ada Lovelace", Age: 30}      // create a new person
	p.Age = 36
	fmt.Println(p)
	
	var person2 Person                              // also create a new person
	person2.Name= "Susan Wojcicki"
	person2.Age= 54
	fmt.Println(person2)
	
	person3 := new(Person)                          // also create a new person
	person3.Age=26
}

```

*{Ada Lovelace 36}* \
*{Susan Wojcicki 54}*

If you see this output,look like you finished this step successfully