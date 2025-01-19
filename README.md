def calculator():
    while True:  
        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
            print("Enter 1 for addition")
            print("Enter 2 for subtraction")
            print("Enter 3 for multiplication")
            print("Enter 4 for division")
            operation = int(input("Choose operation (1/2/3/4): "))

            if operation == 1:
                print("Result:", num1 + num2)
            elif operation == 2:
                print("Result:", num1 - num2)
            elif operation == 3:
                print("Result:", num1 * num2)
            elif operation == 4:
                if num2 != 0:
                    print("Result:", num1 / num2)
                else:
                    print("Cannot divide by zero!")
            else:
                print("Invalid choice!")
        except ValueError:
            print("Invalid input! Please enter a valid number.")

        continue_program = input("Do you want to perform another calculation? (yes/no): ").lower()
        if continue_program != 'yes':
            print("Exiting calculator...")
            break

calculator()
