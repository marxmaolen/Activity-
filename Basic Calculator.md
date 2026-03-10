# Basic Calculator
print("•••Basic Calculator•••")

num1 = float(input("Enter number: "))
num2 = float(input("Enter number: "))

print("\n\t(+, -, *, /)")
operation = input("Operation: ")

if operation == "+":
    result = num1 + num2
    print(f"\n{num1} + {num2} = {result}")

elif operation == "-":
    result = num1 - num2
    print(f"\n{num1} - {num2} = {result}")

elif operation == "*":
    result = num1 * num2
    print(f"\n{num1} * {num2} = {result}")

elif operation == "/":
    if num2 != 0:
        result = num1 / num2
        print(f"\n{num1} / {num2} = {result}")
    else:
        print("\nError!")
        print("Cannot divide by zero")

else:
    print("Invalid operation")
    
