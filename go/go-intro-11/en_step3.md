### File Operations and Manipulations

Go provides many other file operations, such as renaming, deleting, and checking the existence of files. Here are a few examples:

First, create a text file `oldText.txt`, write random text in it and exit

create new go file -> `fileOperations.go` 

Paste the code 

```
package main

import (
    "fmt"
    "os"
)

func main() {
    // Renaming a file
    err := os.Rename("oldText.txt", "newText.txt")
    if err != nil {
        fmt.Println("Error renaming file:", err)
        return
    }
}
```

`go run fileOperations.go`

Check if newText.txt has been created using the `ls` command.
You should see the new text ,after that you should delete the new text using the code down below.

create new go file-> `fileOperations2.go`
Paste the code following code into fileOperations2.go:

```
package main

import (
    "fmt"
    "os"
)

func main() {

    // File deletion
    err := os.Remove("newText.txt")
    if err != nil {
        fmt.Println("Error deleting file:", err)
        return
    }

    // Checking if the file exists
    if _, err := os.Stat("newText.txt"); err == nil {
        fmt.Println("File exists.")
    } else {
        fmt.Println("File does not exist.")
    }
}
```

After saving the file, run the following command: `go run fileOperations2.go`

Use `ls` command to check that yeni.txt file is no longer present.

If you delete the newText.txt correctly good job gopher !, you can continue..