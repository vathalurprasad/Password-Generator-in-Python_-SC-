# Password-Generator-in-Python_-SC-
# Password Generator

This is a simple Python program to generate a strong random password based on the desired length provided by the user.

## Features
- Generates passwords with a mix of uppercase and lowercase letters, digits, and special characters.
- User can specify the desired length of the password.
- Validates user input to ensure only valid numbers are accepted.

## How to Use
1. Run the Python script.
2. When prompted, enter the desired length for the password.
3. The program generates and displays a secure random password.

## Code Example
```python
import random
import string

def generate_password(length=12):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choices(characters, k=length))
    return password

try:
    user_length = int(input(" Enter desired password length: "))
    print(" Generated Password:", generate_password(user_length))
except ValueError:
    print(" Please enter a valid number.")
