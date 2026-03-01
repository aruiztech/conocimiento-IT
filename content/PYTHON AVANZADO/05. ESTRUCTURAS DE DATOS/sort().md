---
title: sort() — Método de listas en Python
description: Explicación completa del método sort() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# sort() — Método de listas en Python

El método `sort()` se utiliza para **ordenar los elementos de una lista en su lugar** (modifica la lista original).  

Su sintaxis básica es:

```python
lista.sort(key=None, reverse=False)
````

* `lista` → cualquier lista de Python.
* `key` (opcional) → función que sirve para personalizar el criterio de ordenación.
* `reverse` (opcional) → `True` para ordenar de manera descendente; `False` por defecto (ascendente).

> Nota: `sort()` **modifica la lista original** y no devuelve una nueva lista. Para crear una lista ordenada sin modificar la original, usar `sorted()`.

---

## Ejemplo básico

```python
numeros = [4, 2, 9, 1]
numeros.sort()
print(numeros)
```

**Salida:**

```python
[1, 2, 4, 9]
```

---

## Orden descendente

```python
numeros = [4, 2, 9, 1]
numeros.sort(reverse=True)
print(numeros)
```

**Salida:**

```python
[9, 4, 2, 1]
```

---

## Orden personalizado con key

```python
palabras = ["manzana", "kiwi", "banana"]
palabras.sort(key=len)
print(palabras)
```

**Salida:**

```python
['kiwi', 'banana', 'manzana']
```

> La lista se ordena por la longitud de cada palabra.

---

## Comparación con reverse()

* [[reverse()]] → invierte la lista sin ordenar.
* [[sort()]] → ordena la lista según criterio definido.

---

## Buenas prácticas

* Usar `sort()` cuando necesites **ordenar la lista permanentemente**.
* Para ordenar sin modificar la lista original, usar `sorted(lista)`.

---

## Conexiones con otros métodos

* [[append()]] / [[extend()]] / [[insert()]] → agregar elementos antes de ordenar.
* [[reverse()]] → invertir lista ya ordenada.
* [[count()]] / [[index()]] → consultar elementos después de ordenar.

---

## Resumen

* `sort()` ordena **la lista original** según criterios ascendente, descendente o personalizados.
* Complementa [[reverse()]] y [[sorted()]] según necesidad de orden y manipulación de listas.

---


