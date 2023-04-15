## Prime Number

A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself. In Python, you can write a function to check if a given number is prime or not. Here's an example of a Python function to check if a number is prime:

```
def is_prime(n):
    """
    Check if a number is prime.

    Args:
        n (int): The number to check.

    Returns:
        bool: True if the number is prime, False otherwise.
    """
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True
```

The `is_prime()` function takes an integer `n` as input and checks if it is a prime number. It returns `True` if `n` is prime and `False` otherwise. The function first checks if `n` is less than or equal to 1, in which case it returns `False`, since 1 is not a prime number. Then, it iterates from 2 to the square root of `n` (inclusive) and checks if `n` is divisible by any number in that range. If `n` is divisible by any number in that range, it returns `False`, indicating that `n` is not prime. If no divisors are found, the function returns `True`, indicating that `n` is prime.

You can use this function to check if a given number is prime or not by calling it and passing the number as an argument. For example:

```
n = 17
if is_prime(n):
    print(f"{n} is a prime number.")
else:
    print(f"{n} is not a prime number.")
```

This will output: "17 is a prime number."


