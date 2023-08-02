### Writing to Files

To write data to a file in Go, you can use the os.Create() function to create a new file or truncate an existing one. After obtaining a file handle, you can write data using a Writer.

Here's an example of how to create and write to a new text file in Go:

Type `vi create.go` to create new go file. Paste the code (by Ctrl + Shift + V )

```
package main

import (
    "fmt"
    "os"
)

func main() {
    file, err := os.Create("output.txt")
    if err != nil {
        fmt.Println("Error creating file:", err)
        return
    }
    defer file.Close()

    content := "Hello, this is written to a file!"
    _, err = file.WriteString(content)
    if err != nil {
        fmt.Println("Error writing to file:", err)
        return
    }

    fmt.Println("Data written to the file successfully.")
}
```

In this code, we create a new file named output.txt and write the content "Hello, this is written to a file!" into it.

Run the code , if you have same output ,you can move forward to next step.

![output1.PNG](https://github.com/Gulnur-Altan/BB-Scenario/blob/master/go/Assets/output1.PNG)

