def is_prime(number):
    if number <= 1:
        return False
    for i in range(2, int(number ** 0.5) + 1):
        if number % i == 0:
            return False
    return True

while True:
    try:
        input_num = int(input("Enter a number: "))  
        if is_prime(input_num):
            print(f"{input_num} is a prime number")
        else:
            print(f"{input_num} is not a prime number")
    except ValueError:
        print("Invalid input. Please enter an integer.") 
    except KeyboardInterrupt:  # Handle Ctrl+C or Interrupt
        print("\nProgram interrupted.")
        break ## question one


numbera = float(input("Enter the first number: "))
numberb = float(input("Enter the second number: "))
operation = input("Enter the operation (add, subtract, multiply, divide): ")

def calculator(numbera, numberb, operation):
    if operation == "add":
        print(numbera + numberb)
    elif operation == "subtract":
        print(numbera - numberb)
    elif operation == "multiply":
        print(numbera * numberb)
    elif operation == "divide":
        if numberb != 0:
            print(numbera / numberb)
        else:
            print("Cannot divide by zero")
    else:
        print("Invalid operation") ## question two

calculator(numbera, numberb, operation)
