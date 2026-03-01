---
title: "Métodos de listas en Python"
description: "Explicación y ejemplos de los métodos integrados para manipular listas en Python"
tags: ["Python", "Listas", "Métodos"]
date: 2026-03-01
---

# Métodos de listas en Python

Las listas tienen **métodos integrados** que permiten modificar, ordenar y manipular sus elementos fácilmente.  
Se conectan con:

- [[Crear listas]]
- [[Bucles for]]
- [[List Comprehension]]

# 1. append()
Añade un elemento al final de la lista.
```python
numeros = [1, 2, 3]
numeros.append(4)
print(numeros)
````

Resultado:

```
[1, 2, 3, 4]
```

# 2. extend()

Añade múltiples elementos (otra lista).

```python
numeros = [1, 2, 3]
numeros.extend([4, 5])
print(numeros)
```

Resultado:

```
[1, 2, 3, 4, 5]
```

Diferencia clave:

* `append([4,5])` → agrega la lista como un solo elemento.
* `extend([4,5])` → agrega cada elemento por separado.

# 3. insert()

Inserta un elemento en una posición específica.

```python
numeros = [1, 2, 4]
numeros.insert(2, 3)
print(numeros)
```

Resultado:

```
[1, 2, 3, 4]
```

# 4. remove()

Elimina el primer valor que coincida.

```python
numeros = [1, 2, 3, 2]
numeros.remove(2)
print(numeros)
```

Resultado:

```
[1, 3, 2]
```

# 5. pop()

Elimina y devuelve un elemento por índice.

```python
numeros = [10, 20, 30]
valor = numeros.pop(1)
print(valor)
print(numeros)
```

Resultado:

```
20
[10, 30]
```

Si no se especifica índice, elimina el último.

# 6. clear()

Elimina todos los elementos.

```python
numeros = [1, 2, 3]
numeros.clear()
print(numeros)
```

Resultado:

```
[]
```

# 7. index()

Devuelve la posición de un elemento.

```python
frutas = ["manzana", "banana", "cereza"]
print(frutas.index("banana"))
```

Resultado:

```
1
```

# 8. count()

Cuenta cuántas veces aparece un elemento.

```python
numeros = [1, 2, 2, 3, 2]
print(numeros.count(2))
```

Resultado:

```
3
```

# 9. sort()

Ordena la lista (modifica la original).

```python
numeros = [5, 1, 4, 2]
numeros.sort()
print(numeros)
```

Resultado:

```
[1, 2, 4, 5]
```

Orden descendente:

```python
numeros.sort(reverse=True)
print(numeros)
```

Resultado:

```
[5, 4, 2, 1]
```

# 10. reverse()

Invierte el orden actual.

```python
numeros = [1, 2, 3]
numeros.reverse()
print(numeros)
```

Resultado:

```
[3, 2, 1]
```

# 11. copy()

Crea una copia independiente.

```python
lista1 = [1, 2, 3]
lista2 = lista1.copy()

lista2.append(4)

print(lista1)
print(lista2)
```

Resultado:

```
[1, 2, 3]
[1, 2, 3, 4]
```

# Diferencia entre sort() y sorted()

`sort()` modifica la lista original.

```python
numeros = [3, 1, 2]
nueva = sorted(numeros)

print(numeros)
print(nueva)
```

Resultado:

```
[3, 1, 2]
[1, 2, 3]
```

# Buenas prácticas

1. Usa `sorted()` si no quieres modificar la lista original.
2. Usa `copy()` si necesitas trabajar con una versión independiente.
3. Evita eliminar elementos mientras iteras con [[Bucles for]].

# Mini ejercicios

1. ¿Qué imprime?

```python
lista = [1, 2, 3]
lista.pop()
print(lista)
```

Resultado:

```
[1, 2]
```

2. ¿Qué imprime?

```python
lista = [5, 2, 5, 3]
lista.remove(5)
print(lista)
```

Resultado:

```
[2, 5, 3]
```

# Notas relacionadas

* [[Crear listas]]
* [[List Comprehension]]
* [[Bucles for]]
* [[range()]]
* [[enumerate()]]

