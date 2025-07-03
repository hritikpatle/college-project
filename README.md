# college-project
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Error: Cannot divide by zero."
operations = {
    '+': add,
    '-': subtract,
    '*': multiply,
    '/': divide
}

try:
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))
except ValueError:
    print("Invalid input. Please enter valid numbers.")
    exit()

operation = input("Choose operation (+, -, *, /): ")

if operation in operations:
    result = operations[operation](num1, num2)
    print(f"Result: {result}")
else:
    print("Invalid operation. Please choose +, -, *, or /.")
