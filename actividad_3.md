

# BIBLIOTECA.

````
biblioteca = {}

# Función para agregar un nuevo libro
def agregar_libro():
    titulo = input("Ingrese el título del libro: ")
    autor = input("Ingrese el autor del libro: ")
    año = input("Ingrese el año de publicación del libro: ")
    biblioteca[titulo] = {
        "autor": autor,
        "año": año,
        "disponible": True
    }
    print(f'El libro "{titulo}" ha sido añadido a la biblioteca.')

# Función para prestar un libro
def prestar_libro():
    titulo = input("Ingrese el título del libro que desea prestar: ")
    if titulo in biblioteca:
        if biblioteca[titulo]["disponible"]:
            biblioteca[titulo]["disponible"] = False
            print(f'El libro "{titulo}" ha sido prestado.')
        else:   
            print(f'El libro "{titulo}" ya está prestado.')
    else:
        print(f'El libro "{titulo}" no se encuentra en la biblioteca.')

# Función para devolver un libro
def devolver_libro():
    titulo = input("Ingrese el título del libro que desea devolver: ")
    if titulo in biblioteca:
        if not biblioteca[titulo]["disponible"]:
            biblioteca[titulo]["disponible"] = True
            print(f'El libro "{titulo}" ha sido devuelto.')
        else:
            print(f'El libro "{titulo}" no está prestado.')
    else:
        print(f'El libro "{titulo}" no se encuentra en la biblioteca.')

# Función para mostrar todos los libros
def mostrar_libros():
    if biblioteca:
        for titulo, detalles in biblioteca.items():
            estado = "Disponible" if detalles["disponible"] else "No disponible"
            print(f'Título: {titulo}, Autor: {detalles["autor"]}, Año: {detalles["año"]}, Estado: {estado}')
    else:
        print("La biblioteca no tiene libros registrados.")

# Función para mostrar libros de un año específico
def mostrar_libros_por_año():
    año = input("Ingrese el año de publicación para buscar libros: ")
    encontrados = False
    for titulo, detalles in biblioteca.items():
        if detalles["año"] == año:
            estado = "Disponible" if detalles["disponible"] else "No disponible"
            print(f'Título: {titulo}, Autor: {detalles["autor"]}, Año: {detalles["año"]}, Estado: {estado}')
            encontrados = True
    if not encontrados:
        print(f"No se encontraron libros publicados en el año {año}.")

# Menú principal
def menu():
    while True:
        print("\n--- Menú de la Biblioteca ---")
        print("1. Agregar un nuevo libro")
        print("2. Prestar un libro")
        print("3. Devolver un libro")
        print("4. Ver todos los libros")
        print("5. Mostrar libros por año de publicación")
        print("6. Salir del programa")
        
        opcion = input("Seleccione una opción: ")

        if opcion == "1":
            agregar_libro()
        elif opcion == "2":
            prestar_libro()
        elif opcion == "3":
            devolver_libro()
        elif opcion == "4":
            mostrar_libros()
        elif opcion == "5":
            mostrar_libros_por_año()
        elif opcion == "6":
            print("Gracias por usar el sistema de la biblioteca. ¡Hasta luego Putito!")
            break
        else:
            print("Opción no válida. Por favor, intente nuevamente.")

# Ejecutamos el menú
menu()

````
