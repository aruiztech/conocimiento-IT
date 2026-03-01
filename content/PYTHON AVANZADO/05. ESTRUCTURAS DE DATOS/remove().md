---
title: remove() — Método de listas en Python
description: Explicación completa del método remove() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# remove() — Método de listas en Python

El método `remove()` se utiliza para **eliminar la primera aparición de un elemento específico** de una lista.  

Su sintaxis básica es:

```python
lista.remove(elemento)
````

* `lista` → cualquier lista de Python.
* `elemento` → valor que se desea eliminar.

> Nota: Si el elemento no existe en la lista, Python lanzará un **ValueError**.

---

## Ejemplo simple

```python
frutas = ["manzana", "plátano", "naranja", "plátano"]
frutas.remove("plátano")
print(frutas)
```

**Salida:**

```python
['manzana', 'naranja', 'plátano']
```

> Solo se elimina la **primera aparición** de `"plátano"`.

---

## Manejo de errores

Para evitar que el programa falle si el elemento no existe:

```python
frutas = ["manzana", "naranja"]
elemento = "kiwi"

if elemento in frutas:
    frutas.remove(elemento)
else:
    print(f"{elemento} no está en la lista")
```

**Salida:**

```python
kiwi no está en la lista
```

---

## Comparación con otros métodos

* [[pop()]] → elimina por índice y devuelve el elemento eliminado.
* [[insert()]] / [[append()]] / [[extend()]] → agregan elementos.
* [[count()]] / [[index()]] → consultar elementos.

---

## Buenas prácticas

* Usar `remove()` cuando necesites eliminar un **elemento específico por valor**.
* Para eliminar múltiples ocurrencias, combinar con un bucle o comprensión de listas:

```python
numeros = [1, 2, 3, 2, 4, 2]
numeros = [x for x in numeros if x != 2]
print(numeros)
```

**Salida:**

```python
[1, 3, 4]
```

---

## Resumen

* `remove()` elimina la primera aparición de un valor en la lista.
* Genera error si el valor no existe.
* Complementa [[pop()]] y [[insert()]] para modificar listas según valor o posición.

---

