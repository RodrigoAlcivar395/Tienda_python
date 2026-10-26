class Producto:

    def __init__(self, nombre, precio, descuento):
        self.nombre = nombre
        self.precio = precio
        self.descuento = descuento

    def mostrar_producto(self):
        print("Nombre del producto:", self.nombre)
        print("Precio:", self.precio)
        print("Descuento:", self.descuento, "%")

    def calcular_descuento(self):
        descuento = self.precio * self.descuento / 100
        return descuento

    def mostrar_precio_final(self):
        descuento = self.calcular_descuento()
        precio_final = self.precio - descuento
        print("Precio final:", precio_final)

    def mostrar_ahorro(self):
        ahorro = self.calcular_descuento()
        print("Te estás ahorrando:", ahorro)

producto1 = Producto("Tenis", 1000, 20)
producto1.mostrar_producto()
print("Descuento en pesos:", producto1.calcular_descuento())
producto1.mostrar_precio_final()
producto1.mostrar_ahorro()

