---
title: pop() — Método de listas en Python
description: Explicación completa del método pop() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# pop() — Método de listas en Python

El método `pop()` se utiliza para **eliminar y devolver un elemento de una lista**.  

Su sintaxis básica es:

```python
lista.pop([indice])
````

* `lista` → cualquier lista de Python.
* `indice` (opcional) → posición del elemento a eliminar.

  * Si no se especifica, elimina y devuelve el **último elemento** de la lista.

> Nota: Si la lista está vacía, Python lanzará un **IndexError**.

---

## Ejemplo eliminando el último elemento

```python
frutas = ["manzana", "plátano", "naranja"]
ultimo = frutas.pop()
print(ultimo)
print(frutas)
```

**Salida:**

```python
naranja
['manzana', 'plátano']
```

---

## Ejemplo eliminando un elemento por índice

```python
numeros = [10, 20, 30, 40]
eliminado = numeros.pop(1)
print(eliminado)
print(numeros)
```

**Salida:**

```python
20
[10, 30, 40]
```

---

## Comparación con remove()

* [[remove()]] elimina un elemento **por valor**.
* [[pop()]] elimina un elemento **por índice** y devuelve el valor eliminado.

---

## Buenas prácticas

* Usar `pop()` cuando necesites **obtener el elemento eliminado**.
* Ideal en estructuras tipo **stack** (LIFO, Last In First Out):

```python
pila = []
pila.append(1)
pila.append(2)
ultimo = pila.pop()
print(ultimo)  # 2
```

---

## Conexiones con otros métodos

* [[append()]] → agrega al final.
* [[insert()]] → agrega en posición específica.
* [[remove()]] → elimina por valor.
* [[extend()]] → agrega múltiples elementos.

---

## Resumen

* `pop()` elimina y devuelve un elemento de la lista.
* Por defecto, elimina el último elemento.
* Complementa [[remove()]] y [[insert()]] según se necesite eliminar por índice o valor.

---


