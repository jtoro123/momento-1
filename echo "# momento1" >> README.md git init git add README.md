# Paso 1: Crear un diccionario vacío
mi_diccionario = {}

# Definir funciones para cada acción del menú
def agregar_elemento(diccionario):
    clave = input("Ingrese la clave: ")
    valor = input("Ingrese el valor: ")
    diccionario[clave] = valor
    print(f"Elemento '{clave}' agregado correctamente.")

def buscar_elemento(diccionario):
    clave = input("Ingrese la clave que desea buscar: ")
    if clave in diccionario:
        print(f"Valor encontrado: {diccionario[clave]}")
    else:
        print(f"La clave '{clave}' no existe en el diccionario.")

def actualizar_elemento(diccionario):
    clave = input("Ingrese la clave que desea actualizar: ")
    if clave in diccionario:
        valor = input("Ingrese el nuevo valor: ")
        diccionario[clave] = valor
        print(f"Elemento '{clave}' actualizado correctamente.")
    else:
        print(f"La clave '{clave}' no existe en el diccionario.")

def eliminar_elemento(diccionario):
    clave = input("Ingrese la clave que desea eliminar: ")
    if clave in diccionario:
        del diccionario[clave]
        print(f"Elemento '{clave}' eliminado correctamente.")
    else:
        print(f"La clave '{clave}' no existe en el diccionario.")

# Definir el bucle principal del programa
while True:
    print("\nMenu:")
    print("1. Agregar")
    print("2. Buscar")
    print("3. Actualizar dato")
    print("4. Eliminar elemento")
    print("5. Salir")
    
    opcion = input("Digite la opción: ")
    
    if opcion == "1":
        agregar_elemento(mi_diccionario)
    elif opcion == "2":
        buscar_elemento(mi_diccionario)
    elif opcion == "3":
        actualizar_elemento(mi_diccionario)
    elif opcion == "4":
        eliminar_elemento(mi_diccionario)
    elif opcion == "5":
        print("Saliendo del programa.")
        break
    else:
        print("Opción no válida. Por favor, elija una opción válida del menú.")
