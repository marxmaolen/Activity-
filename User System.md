# User System 
users = []

while True:
    print("\n•••User Management System•••")
    print("1. Show Users")
    print("2. Add User")
    print("3. Update User")
    print("4. Delete User")
    print("5. Exit")

    choice = input("\nChoice: ")

    # Show Users
    if choice == "1":
        if len(users) == 0:
            print("\nNo users found.")
        else:
            print("\n•••User List•••")
            for i, user in enumerate(users):
                print(f"{i + 1}. {user}")

    # Add User
    elif choice == "2":
        new_user = input("Enter new user name: ")
        users.append(new_user)
        print("User added successfully!")

    # Update User
    elif choice == "3":
        if len(users) == 0:
            print("No users to update.")
        else:
            for i, user in enumerate(users):
                print(f"{i + 1}. {user}")
            try:
                num = int(input("\nNumber of User to update: "))
                if 1 <= num <= len(users):
                    updated_name = input("New name: ")
                    users[num - 1] = updated_name
                    print("\nUser updated successfully!")
                else:
                    print("Invalid number.")
            except ValueError:
                print("Please enter a valid number.")

    # Delete User
    elif choice == "4":
        if len(users) == 0:
            print("\nNo users to delete.")
        else:
            for i, user in enumerate(users):
                print(f"{i + 1}. {user}")
            try:
                num = int(input("Number of User to delete: "))
                if 1 <= num <= len(users):
                    deleted = users.pop(num - 1)
                    print(f"\n{deleted} deleted successfully!")
                else:
                    print("\nInvalid number.")
            except ValueError:
                print("Please enter a valid number.")

    # Exit
    elif choice == "5":
        print("Exiting....")
        break

    else:
        print("Invalid choice. Please select 1-5.")


