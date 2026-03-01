---
title: index() — Método de listas en Python
description: Explicación completa del método index() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# index() — Método de listas en Python

El método `index()` se utiliza para **encontrar la posición del primer elemento que coincide con un valor** en una lista.  

Su sintaxis básica es:

```python
lista.index(elemento, inicio=0, fin=len(lista))
````

* `lista` → cualquier lista de Python.
* `elemento` → valor que deseas buscar.
* `inicio` (opcional) → índice desde donde comenzar la búsqueda (por defecto 0).
* `fin` (opcional) → índice donde finalizar la búsqueda (por defecto el final de la lista).
* Devuelve un **entero** con la posición del primer elemento encontrado.
* Si el elemento no existe, lanza un **ValueError**.

---

## Ejemplo básico

```python id="t7w9xp"
frutas = ["manzana", "banana", "kiwi", "banana"]
pos = frutas.index("banana")
print(pos)
```

**Salida:**

```python id="m2f4rk"
1
```

> Devuelve la posición de la **primera aparición** de `"banana"`.

---

## Búsqueda en un rango específico

```python id="h5l1ts"
numeros = [10, 20, 30, 20, 40]
pos = numeros.index(20, 2)  # busca desde índice 2 en adelante
print(pos)
```

**Salida:**

```python id="n9d6kw"
3
```

---

## Comparación con count()

* [[count()]] → devuelve cuántas veces aparece el elemento.
* [[index()]] → devuelve la posición de la **primera aparición**.

---

## Buenas prácticas

* Usar `index()` cuando necesites **localizar la posición de un valor** antes de modificarlo.
* Para evitar errores, verificar si el elemento existe con `in`:

```python id="a3m8qv"
letras = ["a", "b", "c"]
if "d" in letras:
    print(letras.index("d"))
else:
    print("El elemento no existe")
```

**Salida:**

```python id="p5h2kx"
El elemento no existe
```

---

## Conexiones con otros métodos

* [[append()]] / [[insert()]] / [[extend()]] → agregar elementos antes de buscarlos.
* [[remove()]] / [[pop()]] → eliminar elementos según posición encontrada.
* [[count()]] → contar ocurrencias mientras [[index()]] encuentra posiciones.
* [[sort()]] / [[reverse()]] → cambiar el orden y luego buscar posiciones.

---

## Resumen

* `index()` devuelve la posición de la primera coincidencia de un valor en la lista.
* Complementa [[count()]] para análisis de frecuencia y [[remove()]] / [[pop()]] para modificaciones.
* Permite búsquedas dentro de rangos específicos usando los parámetros `inicio` y `fin`.

---
