---
title: "enumerate() en Python"
description: "Explicación y ejemplos del uso de enumerate() en Python"
tags: ["Python", "Bucles", "enumerate"]
date: 2026-03-01
---

# enumerate() en Python
`enumerate()` es una función integrada que permite **iterar sobre un iterable y obtener al mismo tiempo el índice y el valor**.
Es una alternativa más limpia que usar `range(len(...))`.
Se usa principalmente con [[Bucles for]].

## Sintaxis
```python
enumerate(iterable, start=0)
````

### Parámetros

* `iterable` → Lista, tupla, string, etc.
* `start` → Índice inicial (opcional, por defecto es 0)

## Ejemplo básico

```python
frutas = ["manzana", "banana", "cereza"]

for indice, fruta in enumerate(frutas):
    print(indice, fruta)
```

Resultado:

```
0 manzana
1 banana
2 cereza
```

`enumerate()` devuelve pares `(índice, valor)` en cada iteración.

## Cambiando el índice inicial

```python
frutas = ["manzana", "banana", "cereza"]

for indice, fruta in enumerate(frutas, start=1):
    print(indice, fruta)
```

Resultado:

```
1 manzana
2 banana
3 cereza
```

Muy útil cuando quieres numeraciones humanas (empezando en 1).

## Comparación: range(len()) vs enumerate()

### Forma menos recomendada

```python
frutas = ["manzana", "banana", "cereza"]

for i in range(len(frutas)):
    print(i, frutas[i])
```

Resultado:

```
0 manzana
1 banana
2 cereza
```

Relacionado con [[range()]].

### Forma recomendada

```python
for i, fruta in enumerate(frutas):
    print(i, fruta)
```

Más legible y más “pythónico”.

## Ejemplo con string

```python
for indice, letra in enumerate("Python"):
    print(indice, letra)
```

Resultado:

```
0 P
1 y
2 t
3 h
4 o
5 n
```

## Ejemplo práctico: Lista numerada

```python
tareas = ["Estudiar", "Entrenar", "Programar"]

for num, tarea in enumerate(tareas, start=1):
    print(f"{num}. {tarea}")
```

Resultado:

```
1. Estudiar
2. Entrenar
3. Programar
```

## ¿Qué devuelve realmente enumerate()?

Devuelve un objeto `enumerate`, que puede convertirse en lista:

```python
numeros = ["a", "b", "c"]

print(list(enumerate(numeros)))
```

Resultado:

```
[(0, 'a'), (1, 'b'), (2, 'c')]
```

## Buenas prácticas

1. Usa `enumerate()` cuando necesites índice + valor.
2. Evita `range(len())` si no es estrictamente necesario.
3. Usa `start=1` cuando sea numeración visible para usuarios.

## Mini ejercicios

1️⃣ ¿Qué imprime?

```python
for i, valor in enumerate([10, 20, 30], start=1):
    print(i, valor)
```

Resultado:

```
1 10
2 20
3 30
```

2️⃣ ¿Qué imprime?

```python
for i, letra in enumerate("Hola", start=2):
    print(i, letra)
```

Resultado:

```
2 H
3 o
4 l
5 a
```

# Notas relacionadas

* [[Bucles for]]
* [[range()]]
* [[List Comprehension]]
* [[Crear listas]]
