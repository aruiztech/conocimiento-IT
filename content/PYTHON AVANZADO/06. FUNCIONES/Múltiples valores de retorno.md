---
title: Múltiples valores de retorno — Funciones en Python
description: Explicación de cómo devolver múltiples valores desde funciones Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, return, tuplas, desempaquetado, analogía]
date: 2026-03-01
---

# Múltiples valores de retorno en funciones Python

Una función en Python puede devolver **más de un valor** al mismo tiempo.  
Cuando se devuelven múltiples valores, Python los empaqueta automáticamente en una **tupla**.

> Relacionado con [[Return]], [[Crear tuplas]], [[Desempaquetado]], [[Parámetros y argumentos]].

---

## 1. Devolver varios valores como tupla

```python
def operaciones(a, b):
    suma = a + b
    resta = a - b
    producto = a * b
    return suma, resta, producto

resultado = operaciones(5, 3)
print(resultado)
````

**Salida:**

```python id="mvr1r0k"
(8, 2, 15)
```

> **Analogía mental:** Es como **entregar una bandeja con varios platos**; la función te da todo lo que preparó en un solo paquete.

---

## 2. Desempaquetado de múltiples valores

```python
s, r, p = operaciones(7, 2)
print("Suma:", s)
print("Resta:", r)
print("Producto:", p)
```

**Salida:**

```python id="mvr2r1k"
Suma: 9
Resta: 5
Producto: 14
```

> **Analogía:** Es como **sacar cada plato de la bandeja** y colocarlo en su plato correspondiente.
> Relacionado con [[Desempaquetado]] y [[Crear tuplas]].

---

## 3. Buenas prácticas

* Usar múltiples valores de retorno para **devolver resultados relacionados** sin usar variables globales.
* Documentar lo que devuelve la función en [[Docstrings]].
* Evitar devolver **demasiados valores** que compliquen la comprensión; usa estructuras como diccionarios si es necesario.

```python
def info_persona():
    return {"nombre": "Ángel", "edad": 34, "ciudad": "Granada"}

datos = info_persona()
print(datos)
```

**Salida:**

```python id="mvr3r2k"
{'nombre': 'Ángel', 'edad': 34, 'ciudad': 'Granada'}
```

> **Analogía:** Usar un **diccionario** es como entregar una **caja etiquetada** con varios platos, cada uno con su nombre y contenido.

---

## Resumen

* Las funciones pueden devolver **varios valores**, que Python empaqueta como **tuplas** o estructuras como diccionarios.
* **Analogía final:** Es como entregar **una bandeja con varios platos o una caja etiquetada**, lista para desempaquetar.
* Conexión: [[Return]], [[Crear tuplas]], [[Desempaquetado]], [[Parámetros y argumentos]], [[Docstrings]].

---
