---
title: "Crear listas en Python"
description: "Explicación y ejemplos sobre cómo crear, acceder y manipular listas en Python"
tags: ["Python", "Listas", "Estructuras de datos"]
date: 2026-03-01
---

# Crear listas en Python

Las **listas** son estructuras de datos que permiten almacenar múltiples valores en una sola variable.

Son **ordenadas**  
Son **mutables** (se pueden modificar)  
Permiten elementos duplicados  
Pueden contener distintos tipos de datos

Se usan constantemente con:

- [[Bucles for]]
- [[range()]]
- [[enumerate()]]
- [[List Comprehension]]

# 1. Crear una lista básica
```python
numeros = [1, 2, 3, 4, 5]
print(numeros)
````

Resultado:

```
[1, 2, 3, 4, 5]
```

# 2. Lista de strings

```python
frutas = ["manzana", "banana", "cereza"]
print(frutas)
```

Resultado:

```
['manzana', 'banana', 'cereza']
```

# 3. Lista con distintos tipos

```python
mi_lista = [10, "Hola", True, 3.14]
print(mi_lista)
```

Resultado:

```
[10, 'Hola', True, 3.14]
```

Aunque es posible mezclar tipos, en proyectos profesionales se recomienda mantener coherencia.

# 4. Crear lista con list()

```python
numeros = list((1, 2, 3))
print(numeros)
```

Resultado:

```
[1, 2, 3]
```

También se puede crear desde un string:

```python
letras = list("Python")
print(letras)
```

Resultado:

```
['P', 'y', 't', 'h', 'o', 'n']
```

# 5. Crear lista con range()

```python
numeros = list(range(5))
print(numeros)
```

Resultado:

```
[0, 1, 2, 3, 4]
```

Relacionado con [[range()]].

# 6. Acceder a elementos

```python
frutas = ["manzana", "banana", "cereza"]

print(frutas[0])
print(frutas[1])
```

Resultado:

```
manzana
banana
```

Los índices empiezan en **0**.

# 7. Índices negativos

```python
print(frutas[-1])
```

Resultado:

```
cereza
```

El `-1` accede al último elemento.

# 8. Modificar elementos

```python
frutas = ["manzana", "banana", "cereza"]
frutas[1] = "kiwi"
print(frutas)
```

Resultado:

```
['manzana', 'kiwi', 'cereza']
```

Las listas son **mutables**.

# 9. Añadir elementos

```python
frutas = ["manzana", "banana"]
frutas.append("cereza")
print(frutas)
```

Resultado:

```
['manzana', 'banana', 'cereza']
```

# 10. Eliminar elementos

```python
frutas = ["manzana", "banana", "cereza"]
frutas.remove("banana")
print(frutas)
```

Resultado:

```
['manzana', 'cereza']
```

# 11. Longitud de una lista

```python
frutas = ["manzana", "banana", "cereza"]
print(len(frutas))
```

Resultado:

```
3
```

# Ejemplo práctico

```python
numeros = []

for i in range(1, 6):
    numeros.append(i * 2)

print(numeros)
```

Resultado:

```
[2, 4, 6, 8, 10]
```

Relacionado con [[Bucles for]].

# Buenas prácticas

1. Usa nombres descriptivos (`usuarios`, `productos`, etc.).
2. Evita modificar una lista mientras la recorres.
3. Usa [[List Comprehension]] para crear listas de forma más elegante.

# Mini ejercicios

1. ¿Qué imprime?

```python
lista = [10, 20, 30]
lista.append(40)
print(lista)
```

Resultado:

```
[10, 20, 30, 40]
```

2. ¿Qué imprime?

```python
lista = ["a", "b", "c"]
print(lista[-2])
```

Resultado:

```
b
```

# Notas relacionadas

* [[List Comprehension]]
* [[Bucles for]]
* [[range()]]
* [[enumerate()]]
* [[Crear tuplas]]
* [[Crear diccionarios]]
* [[Crear sets]]

