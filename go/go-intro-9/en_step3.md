## Code Example 3: Function with a Variable Number of Arguments

Go allows functions to have a variable number of arguments using the ... syntax. Here's an example of a function that calculates the average of multiple numbers:

```
func calculateAverage(numbers ...float64) float64 {
    total := 0.0
    for _, num := range numbers {
        total += num
    }
    return total / float64(len(numbers))
}
```
In the calculateAverage function, the numbers parameter is prefixed with ..., indicating that it can accept any number of floating-point values. The function calculates the sum of all the numbers and returns their average.

Write the code and test it this func.