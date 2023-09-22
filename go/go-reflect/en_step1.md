### Exploring Reflection and Introspection in Go


Lets Create a Go program with a struct definition and a function to inspect its fields using reflection.
Make a new file ```vi reflection.go``` and paste the code down below.

```
package main

import (
	"fmt"
	"reflect"
)

type Person struct {
	Name    string
	Age     int
	Address string
}

func inspectStruct(person interface{}) {
	valueOf := reflect.ValueOf(person)
	typeOf := reflect.TypeOf(person)

	fmt.Printf("Type: %v\n", typeOf)

	if valueOf.Kind() == reflect.Struct {
		fmt.Printf("Fields:\n")
		for i := 0; i < valueOf.NumField(); i++ {
			field := valueOf.Field(i)
			fieldName := typeOf.Field(i).Name
			fieldType := field.Type()
			fieldValue := field.Interface()

			fmt.Printf("%s (%v): %v\n", fieldName, fieldType, fieldValue)
		}
	}
}

func main() {
	person := Person{
		Name:    "John Doe",
		Age:     30,
		Address: "123 Main St",
	}

	inspectStruct(person)
}
```
Lets Run the program and observe the output.
```go run reflection.go```

It should display the type of the struct and the fields along with their names, types, and values.
If you see the output, you can continue..

