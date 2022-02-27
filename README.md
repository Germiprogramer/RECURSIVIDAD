# RECURSIVIDAD

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
