# RECURSIVIDAD

La dirección a este repositorio es la siguiente https://github.com/Germiprogramer/RECURSIVIDAD.git

EJERCICIO 1
* Empleando una función recursiva en la cual varía el índice de la tabla, se ha comparado si el elemento elegido es igual a alguno de los elementos de la tabla.
```
elemento = input("Selecciona el elemento que quieres buscar en la tabla: ")

def busqueda(tabla, elemento, indice):
    if elemento == str(tabla[indice]):
        print("EL ELEMENTO SE ENCUENTRA EN LA TABLA")
    else:
        if indice < (len(tabla)-1):
            indice += 1
            busqueda(tabla, elemento, indice)

busqueda([1,2,3,4,5], elemento, 0)
```   
    
EJERCICIO 2
* Para realizar el ejercicio se ha tenido que hacer pasar a la cadena de texto por cuatro filtros. El primero era comprobar si tenía carácteres alfanuméricos o no, para lo que se ha usado la función isalnum(). El segundo y el tercero consistían en convertir los acentos en letras átonas (iteración en un diccionario), y las minúsculas en mayusculas (upper()). Finalmente, para comprobar si la palabra era un palíndromo, se ha realizado una función recursiva que compara los índices del elemento de entrada.
```
entrada = str(input("Escribe una frase: "))

def filtroalfanumerico(entrada):
    entrada = entrada.isalnum()
    if entrada == True:
        pass
    else:
        quit()

filtroalfanumerico(entrada)

def sus(entrada):
    acentos = {'á': 'a', 'é': 'e', 'í': 'i', 'ó': 'o', 'ú': 'u', 'Á': 'A', 'E': 'E', 'Í': 'I', 'Ó': 'O', 'Ú': 'U'}
    for acen in acentos:
        if acen in entrada:
            entrada = entrada.replace(acen, acentos[acen])
    return entrada

entrada = sus(entrada)

def mayus(entrada):
    entrada = entrada.upper()
    return entrada

entrada = mayus(entrada)

longitud = (len(entrada)-1)
indiceizquierda = 0
indicederecha = longitud

def imagen(entrada, indicederecha, indiceizquierda):
    if indiceizquierda < longitud and indicederecha > 0:
        indiceizquierda +=1
        indicederecha -=1
        if entrada[indiceizquierda] == entrada[indicederecha]:
            imagen(entrada, indicederecha, indiceizquierda)
            pass
        else:
            quit()

imagen(entrada, indicederecha, indiceizquierda)

print("TRAS PASAR TODOSLOS FILTROS, LA CADENA INTRODUCIDA SÍ ES UN PALÍNDROMO")

```

EJERCICIO 3

```
from random import randint

fichas = ["R", "A", "V"]

tablero = []

numerofichas = int(input("¿CON CUANTAS FICHAS DESEAS JUGAR?  "))

def generartablero(fichas, tablero, indice, numerofichas):
    indice += 1
    if indice <= numerofichas:
        tablero.append(fichas[randint(0,2)])
        generartablero(fichas, tablero, indice, numerofichas)

generartablero(fichas, tablero, 0, numerofichas)
print(tablero)
```
