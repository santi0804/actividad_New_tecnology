

# ACTIVIDAD EN CLASES:



# Ejercicio 1

```

nombre = "Rogelio"
apellido = "Chingon"
print("Hola mi nombre es", nombre, apellido)

```



# Ejercicio 2

```
precio = 100
descuento = 0.15
porcentaje = (precio / descuento) *100
print(f"El valor con decuento del 15% es de {porcentaje}")

```


# Ejercicio 3

```
edad = 36
if edad >= 18:
 print("Es un puto vegete, mayor de edad")
else:
 print("Eres un mocoso menor de edad")

 ```


# Ejercicio 4 -calcular el  residuo de la disivión del numero *2.

```
numero =int(input("Ingrese tú puto número:"))

if numero % 2 ==0:
 print(f"El número {numero} es par.")
else:
 print(f"Tu jodido número {numero} es impar pendejo")

```



# Ejercicio 5. Multiples operaciones.

```
numero1 = int(input("Ingrece su primer número : "))
numero2 = int(input("Ingrece su  segundo número : "))

# Menú de opciones

print("\nseleccione el calculo a realizar:")
print("1.Suma")
print("2.Resta")
print("3.Multiplicación")
print("4.División")

# Solicitamos al ususario que seleccione una opción.
opcion =input("Seleccione su opción requerida (1/2/3/4) : ")

# Realizar operación

if opcion == "1":
    resultado = numero1 + numero2
    operacion  = "suma"
elif opcion == "2":
    resultado = numero1 - numero2
    operacion = "resta"
elif opcion == "3":
    resultado = numero1 * numero2
    operacion = "multiplicación"
elif opcion == "4":
    if numero2 !=0:
       resultado = numero1 / numero2
       operacion ="division"
    else:
       resultado = "indefinida (division por cero no permitida )"
       operacion ="division"
else:
   resultado = "Opción no validad"
   operacion = None

#Mostrar el resultado de la operación

if operacion:
   print(f"\nEl resultado de la {operacion} de {numero1} y {numero2} es: {resultado}")
else:
   print(f"\n{resultado}")

```


# Ejercicio 6. Calificaciones

```

# Ingrese sus notas en un rango de 0 a 100

nota1 = float(input("Por favor, ingrese la primera nota: "))
nota2 = float(input("Por favor, ingrese la segunda nota: "))
nota3 = float(input("Por favor, ingrese la tercera nota: "))

# Calcular promedio

promedio = (nota1 + nota2 + nota3)/3

# Determinamos si aprobo el promedio o no

if promedio >= 70:
    print(f"Aprobaste putito, con un promedio de {promedio:.2f}")
else:
    print(f"Reprobo con un promedio de {promedio:.2f}")



```



# Ejercicio 7.

```

num1 = int(input("Ingrezar # 1: "))
num2 = int(input("Ingrezar # 2: "))

#Determinar cual es mayor o menor

if num1 > num2:
    print(f"El número {num1} es mayor que {num2}.")
elif num2 > num1:
    print(f"El número {num2} es mayor de {num1}.")
else:
    print("Ambos número son iguales.")

```




# Ejercicio 8.

```
    nombre = input("Ingrece su Nombre: ")
print(f"¡Bienvenido,pendejo Alias {nombre}!")

```




# Ejercicio 9.

```

# ingrese un número
try:
    numero = int(input("Por favor, ingresa un número: "))
    
    # Imprimir la tabla de multiplicar del número ingresado
    print(f"Tabla de multiplicar del {numero}:")
    for i in range(1, 11):
        resultado = numero * i
        print(f"{numero} x {i} = {resultado}")
except ValueError:
    print("Por favor, ingresa un número entero válido.")

```



# Ejercicio 10. Mediador de promedios.

```
numero1 = float(input("Ingrese un numero que desee: "))
numero2 = float(input("Ingrese otro numero que desee: "))

promedio = (numero1 + numero2) /2

print(f"El promedio de {numero1} y {numero2} es: {promedio}")

```