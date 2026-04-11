# Simple Money Withdrawal System

balance = 5000  # Starting balance

while True:
    print("\n=== ATM MENU ===")
    print("1. Withdraw Money")
    print("2. Check Balance")
    print("3. Exit")
    
    choice = input("\nChoice (1-3): ")
    
    if choice == "1":
        try:
            amount = float(input("\nAmount to withdraw: "))
            
            if amount <= 0:
                print("Invalid amount. Please enter a positive number.")
            elif amount > balance:
                print("Insufficient funds...")
                
                # Options after error
                print("\nWhat would you like to do?")
                print("1. Check Balance")
                print("2. Try Again")
                print("3. Exit")
                
                option = input("Enter choice: ")
                
                if option == "1":
                    print(f"\nYour current balance is: {balance}")
                elif option == "2":
                    continue
                elif option == "3":
                    print("Thank you for using the system!")
                    break
                else:
                    print("\nInvalid option.")
            
            else:
                balance -= amount
                print("Withdrawal successful!")
                print(f"Amount withdrawn: {amount}")
                print(f"Remaining balance: {balance}")
                
        except ValueError:
            print("Invalid input! Please enter a valid number.")
            
    elif choice == "2":
        print(f"Your current balance is: {balance}")
        
    elif choice == "3":
        print("Thank you for using the system!")
        break
        
    else:
        print("Invalid choice. Please select from 1 to 3.")
