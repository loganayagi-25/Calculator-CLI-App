# Calculator-CLI-App
import math
print("===== Simple Calculator =====")
print("Select operation:")
print("1. Addition")
print("2. Subtraction")
print("3. Multiplication")
print("4. Division")
print("5. Square Root")
print("6. Exit")
while True:
    choice = input("\nEnter your choice (1-6): ")

    if choice == '6':
        print("Exiting Calculator... Goodbye!")
        break

    if choice == '5':
        num = float(input("Enter number: "))
        if num < 0:
            print("Error! Cannot find square root of a negative number.")
        else:
            print("Result: \u221A", num, "=", math.sqrt(num))
        continue

    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))

    if choice == '1':
        print("Result:", num1, "+", num2, "=", num1 + num2)
    elif choice == '2':
        print("Result:", num1, "-", num2, "=", num1 - num2)
    elif choice == '3':
        print("Result:", num1, "*", num2, "=", num1 * num2)
    elif choice == '4':
        if num2 == 0:
            print("Error! Division by zero is not allowed.")
        else:
            print("Result:", num1, "/", num2, "=", num1 / num2)
    else:
        print("Invalid choice! Please select between 1 and 6.")
