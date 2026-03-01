---
title: Docstrings — Documentación de funciones en Python
description: Explicación de cómo usar docstrings en Python para documentar funciones, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, documentación, docstrings, buenas_prácticas, analogía]
date: 2026-03-01
---

# Docstrings en Python

Los **docstrings** son cadenas de texto utilizadas para **documentar funciones, clases o módulos** en Python.  
Se escriben justo después de la definición con comillas triples (`"""`) y sirven para explicar **qué hace la función y cómo usarla**.

> Relacionado con [[Definir funciones]], [[Parámetros y argumentos]], [[Return]], [[Múltiples valores de retorno]], [[Funciones lambda]], [[Funciones como argumentos]].

---

## 1. Sintaxis básica de docstring

```python
def sumar(a, b):
    """
    Devuelve la suma de dos números.
    
    Parámetros:
    a (int/float): primer número
    b (int/float): segundo número
    
    Retorna:
    int/float: suma de a y b
    """
    return a + b

resultado = sumar(5, 3)
print(resultado)
````

**Salida:**

```python id="ds1r0k"
8
```

> **Analogía mental:** Un docstring es como **la etiqueta de una receta**, que indica los ingredientes, pasos y resultado esperado.

---

## 2. Acceder a un docstring

```python
print(sumar.__doc__)
```

**Salida:**

```python id="ds2r1k"
Devuelve la suma de dos números.

Parámetros:
a (int/float): primer número
b (int/float): segundo número

Retorna:
int/float: suma de a y b
```

> **Analogía:** Es como abrir la **etiqueta de la receta** para ver cómo usarla antes de cocinar.

---

## 3. Buenas prácticas

* Documentar todas las funciones importantes.
* Explicar **qué hace, qué recibe y qué devuelve**.
* Mantener la **claridad y concisión**.
* Combinable con [[Return]] y [[Múltiples valores de retorno]] para indicar qué devuelve la función.
* Útil para funciones que se pasan como argumentos ([Funciones como argumentos]).

---

## Resumen

* Los **docstrings** permiten documentar el propósito y uso de funciones, clases y módulos.
* Se escriben con `"""` justo después de la definición.
* **Analogía final:** Un docstring es como **la etiqueta de una receta**, clara y accesible, que explica cómo usarla correctamente.
* Conexión: [[Definir funciones]], [[Parámetros y argumentos]], [[Return]], [[Múltiples valores de retorno]], [[Funciones lambda]], [[Funciones como argumentos]].

---

