# Simple Messaging App

filename = "message.txt"

try:
    with open(filename, "x") as file:
        print("File created successfully!")
except FileExistsError:
    print("Error: File already exists.")

while True:
    print("\n\t=== MENU ===")
    print("1. Send a message")
    print("2. View all messages")
    print("3. Exit\n")

    choice = input("Choice (1-3): ")

    if choice == "1":
        try:
            message = input("Enter Message: ")
            with open(filename, "a") as file:
                file.write(message + "\n")
            print("Message is saved!")
        except Exception as e:
            print("Error writing to file:", e)

    elif choice == "2":
        try:
            with open(filename, "r") as file:
                content = file.read()
                if content:
                    print("\n--- Messages ---")
                    print(content)
                else:
                    print("There is no message at the moment...")
        except Exception as e:
            print("There is some trouble reading the file please refresh..", e)

    elif choice == "3":
        print("Thank you for using the program...")
        break

    else:
        print("Invalid...Please try again...") 
