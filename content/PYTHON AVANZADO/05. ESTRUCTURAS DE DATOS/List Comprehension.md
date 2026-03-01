---
title: List Comprehension — Listas en Python
description: Explicación completa de las List Comprehensions en Python con ejemplos y buenas prácticas.
tags: [python, listas, comprensión, métodos]
date: 2026-03-01
---

# List Comprehension — Listas en Python

Las **List Comprehensions** permiten **crear listas nuevas de forma concisa** a partir de listas existentes, aplicando expresiones, filtros o transformaciones.  

Su sintaxis básica es:

```python
[nueva_expresion for elemento in iterable if condicion]
````

* `nueva_expresion` → expresión aplicada a cada elemento.
* `elemento` → cada ítem del iterable original.
* `iterable` → cualquier objeto que se pueda recorrer (lista, rango, etc.).
* `if condicion` (opcional) → filtra los elementos que cumplen la condición.

> Nota: List Comprehensions son **más rápidas y legibles** que los bucles `for` tradicionales para crear listas.

---

## Ejemplo básico

```python id="1a9bcq"
numeros = [1, 2, 3, 4, 5]
cuadrados = [x**2 for x in numeros]
print(cuadrados)
```

**Salida:**

```python id="2b0drt"
[1, 4, 9, 16, 25]
```

> Cada elemento se eleva al cuadrado y se genera una nueva lista.

---

## Con condición (filtro)

```python id="3c2sld"
numeros = [1, 2, 3, 4, 5]
pares = [x for x in numeros if x % 2 == 0]
print(pares)
```

**Salida:**

```python id="4d1mye"
[2, 4]
```

> Solo se incluyen los números pares.

---

## Combinación de operaciones

```python id="5e3nzk"
frutas = ["manzana", "kiwi", "banana"]
mayusculas = [f.upper() for f in frutas if len(f) > 4]
print(mayusculas)
```

**Salida:**

```python id="6f2wqy"
['MANZANA', 'BANANA']
```

> Aplica transformación y filtro al mismo tiempo.

---

## Comparación con métodos tradicionales

```python id="7g1trx"
# Bucle tradicional
cuadrados = []
for x in numeros:
    cuadrados.append(x**2)
```

* List Comprehension es **más corta y legible** que el bucle con append().
* Complementa métodos como [[append()]], [[extend()]] y [[insert()]] al crear listas de forma dinámica.

---

## Buenas prácticas

* Usar List Comprehensions para **listas pequeñas y medianas**, o cuando la lógica sea clara.
* Evitar comprensiones muy complejas, usar bucles tradicionales si hay demasiadas condiciones.
* Pueden **anidarse**, pero se recomienda mantener claridad:

```python id="8h4kyp"
matriz = [[i*j for j in range(3)] for i in range(4)]
print(matriz)
```

**Salida:**

```python id="9i5lzr"
[[0, 0, 0], [0, 1, 2], [0, 2, 4], [0, 3, 6]]
```

---

## Conexiones con otros métodos de listas

* [[append()]] → agregar elementos de forma manual en bucles.
* [[extend()]] → combinar con otras listas generadas.
* [[remove()]] / [[pop()]] → modificar listas resultantes de comprehensions.
* [[count()]] / [[index()]] → análisis posterior de listas creadas.

---

## Resumen

* List Comprehensions permiten **crear listas nuevas de forma concisa y eficiente**.
* Soportan transformaciones y filtros.
* Complementan los métodos de listas para manipulación dinámica y eficiente.

---

