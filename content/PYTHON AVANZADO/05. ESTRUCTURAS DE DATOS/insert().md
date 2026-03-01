---
title: insert() — Método de listas en Python
description: Explicación completa del método insert() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# insert() — Método de listas en Python

El método `insert()` se utiliza para **agregar un elemento en una posición específica de una lista**, desplazando los elementos posteriores a la derecha.  

Su sintaxis básica es:

```python
lista.insert(indice, elemento)
````

* `lista` → cualquier lista de Python.
* `indice` → posición donde quieres insertar el elemento (empezando en 0).
* `elemento` → cualquier objeto que quieras añadir.

---

## Ejemplo simple

```python
frutas = ["manzana", "plátano", "naranja"]
frutas.insert(1, "kiwi")
print(frutas)
```

**Salida:**

```python
['manzana', 'kiwi', 'plátano', 'naranja']
```

> El elemento `"kiwi"` se inserta en la posición 1, y los demás elementos se desplazan a la derecha.

---

## Inserción al inicio o al final

* **Inicio (índice 0)**

```python
numeros = [2, 3, 4]
numeros.insert(0, 1)
print(numeros)
```

**Salida:**

```python
[1, 2, 3, 4]
```

* **Final (índice igual a la longitud de la lista)**

```python
numeros.insert(len(numeros), 5)
print(numeros)
```

**Salida:**

```python
[1, 2, 3, 4, 5]
```

> Nota: Para agregar al final también se puede usar [[append()]].

---

## Buenas prácticas

* Usar `insert()` cuando necesites **controlar la posición exacta** del nuevo elemento.
* Evitar en listas muy grandes si es dentro de bucles frecuentes, porque desplazar elementos tiene costo O(n).

---

## Comparación con otros métodos

* [[append()]] → agrega un elemento al final de la lista.
* [[extend()]] → agrega varios elementos al final de la lista.
* [[pop()]] / [[remove()]] → eliminan elementos.

---

## Conexiones con otros métodos

* [[append()]] → para agregar al final.
* [[extend()]] → para agregar múltiples elementos.
* [[pop()]] → eliminar por índice.
* [[remove()]] → eliminar por valor.
* [[count()]] / [[index()]] → consultar elementos.

---

## Resumen

* `insert()` permite agregar un elemento en **una posición específica** de la lista.
* Desplaza los elementos posteriores.
* Complementa [[append()]] y [[extend()]] según la necesidad de control de posición.

---

