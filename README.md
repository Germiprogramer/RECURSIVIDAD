# RECURSIVIDAD

EJERCICIO 2
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

print(entrada)

```
