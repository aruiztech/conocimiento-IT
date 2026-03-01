---
title: Bucles for en Python
description: Guía sobre el uso de bucles for en Python para iterar sobre secuencias y repetir tareas.
tags: [python, bucles, for, iterables, listas, tuplas, diccionarios, strings]
date: 2026-03-01
---

El **bucle `for`** se utiliza para **iterar sobre elementos de una secuencia**: listas, tuplas, strings, diccionarios, sets o cualquier iterable.  
Es ideal para repetir tareas sin necesidad de escribir código repetitivo.  
Se conecta con **listas** [[Crear listas]], **tuplas** [[Crear tuplas]], **sets** [[Crear sets]] y **diccionarios** [[Crear diccionarios]].

## Sintaxis básica
```python id="forres0"
for variable in iterable:
    # bloque de código a repetir
````

* `variable`: toma **cada elemento** del iterable en cada iteración.
* `iterable`: cualquier objeto sobre el que se pueda iterar (lista, string, tupla, etc.).

## Ejemplo simple con lista

```python id="forres1"
frutas = ["manzana", "banana", "cereza"]

for fruta in frutas:
    print(fruta)
```

Resultado:

```id="forres1r"
manzana
banana
cereza
```

## Ejemplo con string

```python id="forres2"
for letra in "Python":
    print(letra)
```

Resultado:

```id="forres2r"
P
y
t
h
o
n
```

## Ejemplo con tupla

```python id="forres3"
numeros = (1, 2, 3, 4)

for num in numeros:
    print(num * 2)
```

Resultado:

```id="forres3r"
2
4
6
8
```

## Iterando con `range()`

```python id="forres4"
for i in range(5):
    print(i)
```

Resultado:

```id="forres4r"
0
1
2
3
4
```

* `range(5)` genera los números 0 a 4.
* Cada iteración asigna un valor a `i`.

### Personalizando `range()`

```python id="forres5"
for i in range(2, 10, 2):
    print(i)
```

Resultado:

```id="forres5r"
2
4
6
8
```

* Primer parámetro: inicio
* Segundo parámetro: fin (no inclusivo)
* Tercer parámetro: paso

## Iterando con diccionarios

```python id="forres6"
edades = {"Ana": 25, "Luis": 30, "Eva": 22}

for nombre, edad in edades.items():
    print(f"{nombre} tiene {edad} años")
```

Resultado:

```id="forres6r"
Ana tiene 25 años
Luis tiene 30 años
Eva tiene 22 años
```

⚡ `.items()` devuelve **pares clave-valor**.

## Buenas prácticas

1. Usa nombres descriptivos para la variable del bucle.
2. Evita modificar el iterable mientras iteras sobre él.
3. Combina con **`break`**, **`continue`** y **`else` en bucles** [[break y continue]], [[else en bucles]] para mayor control.

## Mini ejercicios

1️⃣ Itera e imprime todos los números de 1 a 10:

```python id="forres7"
for i in range(1, 11):
    print(i)
```

Resultado:

```id="forres7r"
1
2
3
4
5
6
7
8
9
10
```

2️⃣ Itera una lista de colores e imprime solo los que tengan más de 5 letras:

```python id="forres8"
colores = ["rojo", "verde", "azul", "amarillo"]

for color in colores:
    if len(color) > 5:
        print(color)
```

Resultado:

```id="forres8r"
amarillo
```

## Notas relacionadas

* [[range()]]
* [[break y continue]]
* [[else en bucles]]
* [[List Comprehension]]
* [[Condicionales if]]

