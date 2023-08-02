
### Working with Files in Go: An Introduction with Code Examples

Go, also known as Golang, is a powerful and efficient programming language that comes with a rich standard library, including comprehensive support for file handling operations. In this article, we'll explore the basics of file operations in Go and provide code examples to demonstrate how to read, write, and manipulate files.

### Opening and Reading Files

In Go, you can use the os package to open and read files. The os.Open() function is used to open a file, and then you can read the content using a Reader.

Here's an example of how to open and read a text file in Go:

First, let's create a text file using vi.

Type `vi sample.txt` to create the file.
Inside the file, write `Cloud computing in 2023.` ( Note:To write the text, press the i key to enter insert mode.)After writing the text, save and exit the file ( Note: exit by pressing ESC, then type :wq! and hit Enter. )

Now, let's create a Go file using a text editor. The file can be named file.go. Type `vi file.go` to create the file. Edit the code in the editor and change the `filename.txt` to `sample.txt` , 
then use the >> icon to paste the content into file.go.

```
package main

import (
    "fmt"
    "os"
)

func main() {
    file, err := os.Open("filename.txt")
    if err != nil {
        fmt.Println("Error opening file:", err)
        return
    }
    defer file.Close()

    data := make([]byte, 100)
    count, err := file.Read(data)
    if err != nil {
        fmt.Println("Error reading file:", err)
        return
    }

    fmt.Printf("Read %d bytes: %s\n", count, data[:count])
}
```
lets try to work `go run file.go`
Note: If Go is not installed in the first step, you will encounter an error at this step. (Command: `apk add go`)

If you received a similar output, you can continue.

![output0.PNG](https://gitlab.bulutbilisimciler.com/bb-public/scenarios/-/raw/master/go/Assets/output0.PNG)

In the above code, we open a file named sample.txt, read its content into a byte slice, and then print the read data.

