---
title: extend() — Método de listas en Python
description: Explicación completa del método extend() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# extend() — Método de listas en Python

El método `extend()` se utiliza para **agregar todos los elementos de un iterable (lista, tupla, set, etc.) al final de otra lista**.  

Su sintaxis básica es:

```python
lista.extend(iterable)
````

* `lista` → cualquier lista de Python.
* `iterable` → lista, tupla, set, cadena, u otro objeto iterable cuyos elementos se agregan individualmente.

---

## Ejemplo simple con lista

```python
numeros = [1, 2, 3]
numeros.extend([4, 5, 6])
print(numeros)
```

**Salida:**

```python
[1, 2, 3, 4, 5, 6]
```

> Nota: cada elemento del iterable se agrega **individualmente**, no como una lista anidada.

---

## Ejemplo con cadena

```python
letras = ['a', 'b']
letras.extend('cd')
print(letras)
```

**Salida:**

```python
['a', 'b', 'c', 'd']
```

> Cada carácter de la cadena se agrega como un elemento individual.

---

## Comparación con append()

* `append()` agrega **un solo elemento** al final de la lista.
* `extend()` agrega **todos los elementos de un iterable** al final de la lista.

```python
a = [1, 2]
b = [3, 4]

a.append(b)   # [1, 2, [3, 4]]
a = [1, 2]
a.extend(b)   # [1, 2, 3, 4]
```

---

## Buenas prácticas

* Usar `extend()` cuando necesites **combinar listas** o agregar múltiples elementos de un iterable.
* Ideal para construir listas de manera eficiente dentro de bucles:

```python
resultado = []
for i in range(3):
    resultado.extend([i, i*2])
print(resultado)
```

**Salida:**

```python
[0, 0, 1, 2, 2, 4]
```

---

## Conexiones con otros métodos

* [[append()]] → agrega un único elemento.
* [[insert()]] → agrega un elemento en una posición específica.
* [[pop()]] → elimina el último elemento o un índice específico.
* [[remove()]] → elimina un elemento por valor.
* [[count()]] / [[index()]] → para consultar elementos después de agregar.

---

## Resumen

* `extend()` agrega todos los elementos de un iterable **individualmente** al final de una lista.
* Modifica la lista original.
* Útil para combinar listas o agregar múltiples elementos de manera eficiente.
* Complementa [[append()]] según el tipo de operación que necesites.

---

