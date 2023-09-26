Programı yansıtma (reflection) kullanarak dinamik alan değişikliğine izin vermek için düzenleyin. Belirli bir alana yeni bir değer belirlemek için bir fonksiyon ekleyelim

Aynı dosyayı düzenleyebilir ve yeniden çalıştırabilirsiniz,
```vi reflection.go``` 

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
Değişiklikleri eklediysen, kodu çalıştır. Artık yansıtma (reflection) kullanarak belirli bir alanın değerini dinamik olarak değiştirmenize izin verilir.

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

Çıktıyı görüyorsanız,devam edebilirsiniz.


