# ViLearnX-Task-2
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Division by zero is not allowed."
    return x / y

def calculator():
    print("Welcome to the Basic Calculator!")
    # User input
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
    except ValueError:
        print("Invalid input. Please enter numeric values.")
        return
    # Operation selection
    print("Select an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    operation = input("Enter the number corresponding to the operation (1/2/3/4): ")
    # Operation execution
    if operation == '1':
        result = add(num1, num2)
        operation_symbol = "+"
    elif operation == '2':
        result = subtract(num1, num2)
        operation_symbol = "-"
    elif operation == '3':
        result = multiply(num1, num2)
        operation_symbol = "*"
    elif operation == '4':
        result = divide(num1, num2)
        operation_symbol = "/"
    else:
        print("Invalid operation selection.")
        return
    # Result display
    print(f"{num1} {operation_symbol} {num2} = {result}")

if __name__ == "__main__":
    calculator()
