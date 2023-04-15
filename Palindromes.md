## Palindromes

Palindromes are words, phrases, numbers, or other sequences of characters that read the same backward and forward. Here are some examples of checking if a word or phrase is a palindrome in Python:

1. Using String Manipulation:

```
def is_palindrome(s):
    s = s.lower().replace(" ", "")  # Convert to lowercase and remove spaces
    return s == s[::-1]  # Compare with its reverse

# Example usage
word = "racecar"
result = is_palindrome(word)
print(f"'{word}' is a palindrome: {result}")
```

2. Using Deque (Double-ended Queue):

```
from collections import deque

def is_palindrome(s):
    s = s.lower().replace(" ", "")  # Convert to lowercase and remove spaces
    dq = deque(s)
    while len(dq) > 1:
        if dq.popleft() != dq.pop():
            return False
    return True

# Example usage
phrase = "A man a plan a canal Panama"
result = is_palindrome(phrase)
print(f"'{phrase}' is a palindrome: {result}")
```


In both examples, the `is_palindrome` function takes a string `s` as input and checks if it is a palindrome by either comparing it with its reverse using string manipulation (first example) or using a deque to compare characters from both ends (second example). The result is then printed to the console.

