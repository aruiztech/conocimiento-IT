---
title: Return — Funciones en Python
description: Explicación del uso de return para devolver valores desde funciones Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, return, modularidad, analogía]
date: 2026-03-01
---

# Return en funciones Python

El **`return`** permite que una función **devuelva un valor** que puede ser usado más adelante, en lugar de solo mostrarlo en pantalla.  
Sin `return`, la función devuelve automáticamente `None`.

> Relacionado con [[Definir funciones]], [[Parámetros y argumentos]], [[*args y **kwargs]], [[Argumentos por defecto]].

---

## 1. Uso básico de return

```python
def sumar(a, b):
    return a + b

resultado = sumar(3, 5)
print(resultado)
````

**Salida:**

```python
8
```

> **Analogía mental:** `return` es como **entregar un plato terminado al cliente**; la función cocina algo y lo devuelve listo para usar, no solo lo muestra en la cocina.

---

## 2. Return vs print

```python
def suma_print(a, b):
    print(a + b)

def suma_return(a, b):
    return a + b

x = suma_print(2, 3)
y = suma_return(2, 3)

print("x:", x)
print("y:", y)
```

**Salida:**

```python
5
x: None
y: 5
```

> **Analogía:** `print` es como mostrar el plato en la mesa de la cocina; `return` es **entregarlo al cliente** para que pueda usarlo.

---

## 3. Devolver múltiples valores

```python
def operaciones(a, b):
    suma = a + b
    producto = a * b
    return suma, producto

res = operaciones(3, 4)
print(res)
```

**Salida:**

```python
(7, 12)
```

> **Analogía:** Es como entregar **una bandeja con varios platos**; la función puede devolver más de un valor empaquetado en una tupla.
> Relacionado con [[Crear tuplas]] y [[Desempaquetado]].

---

## 4. Buenas prácticas

* Usar `return` para **devolver resultados y evitar efectos secundarios innecesarios**.
* Combinar con [[Parámetros y argumentos]] y [[*args y **kwargs]] para funciones flexibles.
* Documentar claramente lo que devuelve la función en [[Docstrings]].

---

## Resumen

* `return` permite que una función **entregue un valor usable** en lugar de solo mostrarlo.
* Puede devolver **un solo valor, múltiples valores (como tuplas) o incluso estructuras complejas**.
* **Analogía final:** Es como **una función que cocina un plato y te lo entrega listo para usar**, no solo te lo muestra en la cocina.
* Conexión: [[Definir funciones]], [[Parámetros y argumentos]], [[Argumentos por defecto]], [[*args y **kwargs]], [[Crear tuplas]], [[Desempaquetado]].

---
