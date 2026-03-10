# Shopping Cart 
class Item:
    def __init__(self, name, price):
        self.name = name
        self.price = price

class ShoppingCart:
    def __init__(self):
        self.cart = []

    def add_item(self, name, price):
        item = Item(name, price)
        self.cart.append(item)
        print(f"\nItem '{name}' is successfully added to cart.")

    def remove_item(self, name):
        for item in self.cart:
            if item.name == name:
                self.cart.remove(item)
                print(f"Item {name} is removed from cart.")
                return
        print("Item not found.")

    def view_cart(self):
        if not self.cart:
            print("Your cart is empty.")
            return

        print("\n•••Items in Cart•••")
        total = 0
        for item in self.cart:
            print(item.name, "-", item.price)
            total += item.price
        print("\nTotal:", total)

    def checkout(self):
        total = 0
        for item in self.cart:
            total += item.price

        print("\nCheckout Total:", total)
        print("Thank you,for shopping with us!")
        self.cart.clear()

cart = ShoppingCart()

while True:
    print("\n•••Shopping Cart Menu•••")
    print("1. Add Item")
    print("2. Remove Item")
    print("3. View Cart")
    print("4. Checkout")
    print("5. Exit")

    choice = input("\nChoose: ")

    if choice == "1":
        name = input("Item name: ")
        price = float(input("Item price: "))
        cart.add_item(name, price)

    elif choice == "2":
        name = input("Item name to remove: ")
        cart.remove_item(name)

    elif choice == "3":
        cart.view_cart()

    elif choice == "4":
        cart.checkout()

    elif choice == "5":
        print("Exiting......")
        break

    else:
        print("Invalid choice.")
