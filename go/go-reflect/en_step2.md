### Step 2: 

Modify the program to allow dynamic field modification using reflection. Add a function to set a new value for a specific field.
You can edit the same file and execute again,

```
func setField(person interface{}, fieldName string, newValue interface{}) {
	valueOf := reflect.ValueOf(person).Elem()

	field := valueOf.FieldByName(fieldName)

	if field.IsValid() && field.CanSet() {
		newFieldValue := reflect.ValueOf(newValue)
		if newFieldValue.Type() == field.Type() {
			field.Set(newFieldValue)
		} else {
			fmt.Printf("Error: Type mismatch for field %s\n", fieldName)
		}
	} else {
		fmt.Printf("Error: Field %s not found or cannot be set\n", fieldName)
	}
}

func main() {
	person := Person{
		Name:    "John Doe",
		Age:     30,
		Address: "123 Main St",
	}

	inspectStruct(person)

	setField(&person, "Age", 35)
	inspectStruct(person)
}
```
Step 3: Run the modified program. It should now allow you to change the value of a specific field dynamically using reflection.

Type: main.Person<br />
Fields:<br />
Name (string): John Doe<br />
Age (int): 30<br />
Address (string): 123 Main St<br />

Type: main.Person<br />
Fields:<br />
Name (string): John Doe<br />
Age (int): 35<br />
Address (string): 123 Main St<br />
Program exited.

Step 4 (Optional): Experiment with different struct types and field values to further explore the capabilities of reflection and introspection in Go.

