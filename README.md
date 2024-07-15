# semana7
uso constructores y destructores
class ProductoCosmetico:
    def __init__(self, nombre, precio, cantidad):
        """
        Constructor de la clase ProductoCosmetico.
        
        Este método se llama automáticamente al crear una nueva instancia del objeto.
        
        Args:
        - nombre (str): Nombre del producto cosmético.
        - precio (float): Precio unitario del producto.
        - cantidad (int): Cantidad disponible en inventario.
        """
        self.nombre = nombre
        self.precio = precio
        self.cantidad = cantidad
        print(f"Se ha creado un nuevo producto: {self.nombre}")
    
    def __del__(self):
        """
        Destructor de la clase ProductoCosmetico.
        
        Este método se llama automáticamente cuando todas las referencias al objeto son eliminadas.
        Aquí podríamos realizar alguna acción de limpieza o liberación de recursos si fuera necesario.
        """
        print(f"Se está eliminando el producto: {self.nombre}")
    
    def mostrar_informacion(self):
        """
        Método para mostrar la información del producto.
        """
        print(f"Información del producto:")
        print(f"Nombre: {self.nombre}")
        print(f"Precio: ${self.precio}")
        print(f"Cantidad disponible: {self.cantidad} unidades")


# Creación de instancias de ProductoCosmetico
producto1 = ProductoCosmetico("Crema facial", 25.5, 50)
producto2 = ProductoCosmetico("Labial rojo", 15.75, 30)

# Mostrar información de los productos
producto1.mostrar_informacion()
producto2.mostrar_informacion()

# Simulación de eliminación de referencias a los objetos (para activar los destructores)
del producto1
del producto2
