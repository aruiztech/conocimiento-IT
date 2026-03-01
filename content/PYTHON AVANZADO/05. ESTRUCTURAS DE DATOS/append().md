---
title: append() — Método de listas en Python
description: Explicación completa del método append() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# append() — Método de listas en Python

El método `append()` se utiliza para **agregar un elemento al final de una lista** en Python.  

Su sintaxis básica es:

```python
lista.append(elemento)
````

* `lista` → cualquier lista de Python.
* `elemento` → cualquier objeto que quieras añadir a la lista.

---

## Ejemplo simple

```python
frutas = ["manzana", "plátano"]
frutas.append("naranja")
print(frutas)
```

**Salida:**

```
['manzana', 'plátano', 'naranja']
```

---

## Características

* Modifica la **lista original** (no crea una nueva).
* Solo añade un **elemento** a la vez.
* Si añades otra lista, se agrega **como un solo elemento**:

```python
numeros = [1, 2, 3]
numeros.append([4, 5])
print(numeros)
```

**Salida:**

```
[1, 2, 3, [4, 5]]
```

> Nota: para agregar múltiples elementos de manera individual, usar [[extend()]].

---

## Buenas prácticas

* Usar `append()` cuando necesites **agregar un solo elemento**.
* Para construir listas dinámicamente en bucles, `append()` es muy eficiente:

```python
resultado = []
for i in range(5):
    resultado.append(i*i)
print(resultado)
```

**Salida:**

```
[0, 1, 4, 9, 16]
```

---

## Conexiones con otros métodos

* [[extend()]] → para agregar múltiples elementos de otra lista.
* [[insert()]] → para agregar un elemento en una posición específica.
* [[pop()]] → para eliminar el último elemento agregado.
* [[count()]] / [[index()]] → para consultar elementos después de agregar.

---

## Resumen

* `append()` agrega **un elemento al final** de la lista.
* Modifica la lista original.
* Ideal para construir listas paso a paso o dentro de bucles.
* Para agregar múltiples elementos, usar [[extend()]].


---
