## Factorial

Here's an example of how you can calculate the factorial of a number in Python using a recursive function:

```
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

# Example usage
num = 5
result = factorial(num)
print(f"The factorial of {num} is: {result}")
```


In this example, the `factorial` function takes an integer `n` as input and calculates the factorial by recursively multiplying `n` with the factorial of `n-1` until `n` becomes 0 or 1, at which point the recursion stops and the function returns 1. The result is then printed to the console.