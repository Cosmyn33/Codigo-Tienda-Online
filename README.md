# Codigo-Tienda-Online
Automatizar tienda
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price

class ShoppingCart:
    def __init__(self):
        self.products = []

    def add_product(self, product):
        self.products.append(product)

    def total(self):
        total = 0
        for product in self.products:
            total += product.price
        return total

def main():
    # Crea productos
    p1 = Product("Laptop", 1000)
    p2 = Product("Mouse", 20)

    # Crea un carrito de compras
    shopping_cart = ShoppingCart()
    shopping_cart.add_product(p1)
    shopping_cart.add_product(p2)

    # Imprime el total
    print("Total: $", shopping_cart.total())

if __name__ == "__main__":
    main()
