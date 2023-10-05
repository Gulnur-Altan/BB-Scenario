## Writing benchmark tests for a function

In this scenario, you have a function in your Golang codebase that performs a computationally intensive task. You want to write benchmark tests to measure the performance of this function.

You can use the Golang testing package's benchmarking feature to write benchmark tests for your function. Here's an example:

Next, let's create a new Go page. `vim benchTest.go`

```
package main

import (
"testing"
)

func BenchmarkFunction(b \*testing.B) {
for i := 0; i < b.N; i++ {
// Run your function here
}
}
```
After save and exit, lets run with this command,
`go run benchTest.go`
Add go again if doesn't work properly 
`apk add go`

In this example, we're using the BenchmarkFunction test function to run our function multiple times and measure its performance using the testing.B object.
