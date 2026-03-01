---
title: reverse() — Método de listas en Python
description: Explicación completa del método reverse() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# reverse() — Método de listas en Python

El método `reverse()` se utiliza para **invertir el orden de los elementos de una lista**.  

Su sintaxis básica es:

```python
lista.reverse()
````

* `lista` → cualquier lista de Python.
* No recibe parámetros.
* Modifica la lista original y **no devuelve un valor**.

> Nota: Para crear una copia invertida sin modificar la lista original, usar `reversed(lista)` y luego convertirlo a lista: `list(reversed(lista))`.

---

## Ejemplo básico

```python
numeros = [1, 2, 3, 4]
numeros.reverse()
print(numeros)
```

**Salida:**

```python
[4, 3, 2, 1]
```

---

## Diferencia con sort()

* [[sort()]] → ordena la lista según criterios definidos.
* [[reverse()]] → simplemente **invierte el orden actual** de la lista.

---

## Buenas prácticas

* Usar `reverse()` cuando necesites **invertir el orden de la lista rápidamente**.
* Para cadenas o iterables, combinar con `list(reversed(iterable))`:

```python
palabras = ["manzana", "banana", "kiwi"]
invertidas = list(reversed(palabras))
print(invertidas)
```

**Salida:**

```python
['kiwi', 'banana', 'manzana']
```

---

## Conexiones con otros métodos

* [[append()]] / [[extend()]] / [[insert()]] → agregar elementos antes de invertir.
* [[sort()]] → ordenar antes de invertir si se requiere orden específico.
* [[pop()]] / [[remove()]] → eliminar elementos antes o después de invertir.

---

## Resumen

* `reverse()` invierte el orden de los elementos en la lista original.
* No modifica los valores ni ordena, solo cambia la secuencia.
* Complementa [[sort()]] y [[reversed()]] según necesidad de manipulación de listas.

---


