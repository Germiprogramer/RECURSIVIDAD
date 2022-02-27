# RECURSIVIDAD

```
EJERCICIO 2
entrada = str(input("Escribe una frase: "))

#def filtroalfanumerico(entrada):

def sus(entrada):
    acentos = {'á': 'a', 'é': 'e', 'í': 'i', 'ó': 'o', 'ú': 'u', 'Á': 'A', 'E': 'E', 'Í': 'I', 'Ó': 'O', 'Ú': 'U'}
    for acen in acentos:
        if acen in entrada:
            entrada = entrada.replace(acen, acentos[acen])
    return entrada


def mayus(entrada):
    entrada = entrada.upper()
    return entrada


def imagen(entrada):
    longitud = len(entrada)
    indicederecha = 0
    indiceizquierda = 0
    indicederecha +=1
    indiceizquierda -=1
    if indicederecha < longitud and indiceizquierda > (-longitud):
        if entrada[indicederecha] == entrada[indiceizquierda]:
            pass
        else:
            pass
    else:
        pass
    imagen(entrada)

imagen(entrada)
```
