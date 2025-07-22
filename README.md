# calculator.py

def add(a, b):
    """Returns the sum of two numbers"""
    return a + b

def subtract(a, b):
    """Returns the difference between two numbers"""
    return a - b

def multiply(a, b):
    """Returns the product of two numbers"""
    return a * b

def divide(a, b):
    """Returns the quotient of two numbers"""
    if b == 0:
        return "Error! Division by zero."
    return a / b

def calculator():
    print("Simple Calculator")
    print("Operations available:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")
    print("5. Exit")
    
    while True:
        try:
            choice = input("Enter operation (1/2/3/4/5): ")
            
            if choice == '5':
                print("Goodbye!")
                break
                
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
            
            if choice == '1':
                print(f"Result: {add(num1, num2)}")
            elif choice == '2':
                print(f"Result: {subtract(num1, num2)}")
            elif choice == '3':
                print(f"Result: {multiply(num1, num2)}")
            elif choice == '4':
                print(f"Result: {divide(num1, num2)}")
            else:
                print("Invalid input. Please try again.")
                
        except ValueError:
            print("Invalid input. Please enter numbers only.")

if __name__ == "__main__":
    calculator()
