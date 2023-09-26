### Exploring Reflection and Introspection in Go


Bir Go programı oluşturmak için bir struct oluşturup ve yansıtma (reflection) kullanmak için bir fonksiyon oluşturalım.  <br />
Yeni bir go dosyası oluşturun ```nano reflection.go``` ve aşağıdaki kodu yapıştırın. 

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
Programı çalıştıralım <br />
```go run reflection.go```

Fields:  <br />
Name (string): John Doe  <br />
Age (int): 30  <br />
Address (string): 123 Main St 

struct ın tipini ve değerleri görüyorsanız,devam edebilirsiniz..



