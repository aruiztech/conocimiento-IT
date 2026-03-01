---
title: Parámetros y argumentos — Funciones en Python
description: Explicación de los parámetros y argumentos en funciones Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, parámetros, argumentos, analogía]
date: 2026-03-01
---

# Parámetros y argumentos en funciones Python

Los **parámetros** son variables definidas en la función que reciben información, y los **argumentos** son los valores que se pasan al llamar la función.  

> Relacionado con [[Definir funciones]], [[Argumentos por defecto]], [[*args y **kwargs]] y [[Return]].

---

## 1. Parámetros simples

```python
def saludar(nombre):
    print(f"¡Hola, {nombre}!")
    
saludar("Ángel")
````

**Salida:**

```python id="p1r0k"
¡Hola, Ángel!
```

> **Analogía mental:** Piensa en la función como una **receta**; los parámetros son los **ingredientes que la receta espera** y los argumentos son los **ingredientes que realmente das**.

---

## 2. Múltiples parámetros

```python id="p2r1k"
def presentacion(nombre, edad):
    print(f"Me llamo {nombre} y tengo {edad} años.")

presentacion("Ángel", 34)
```

**Salida:**

```python id="p2r2k"
Me llamo Ángel y tengo 34 años.
```

> **Analogía:** Una receta puede requerir varios ingredientes (parámetros) para funcionar correctamente.

---

## 3. Argumentos por posición y por nombre

```python id="p3r3k"
def coordenadas(x, y):
    print(f"Coordenada: ({x}, {y})")

coordenadas(10, 20)       # por posición
coordenadas(y=50, x=25)   # por nombre
```

**Salida:**

```python id="p3r4k"
Coordenada: (10, 20)
Coordenada: (25, 50)
```

> **Analogía:** Los argumentos posicionales se agregan en el **orden esperado**, mientras que los argumentos por nombre se colocan **específicamente en la casilla correcta**.

---

## Buenas prácticas

* Nombrar los parámetros de forma **descriptiva**.
* Usar **argumentos por nombre** para mayor claridad cuando hay muchos parámetros.
* Combinar con **Argumentos por defecto** para flexibilidad (ver [[Argumentos por defecto]]).
* Para recibir **cantidad variable de argumentos**, usar [[*args y **kwargs]].

---

## Resumen

* **Parámetros**: variables definidas en la función.
* **Argumentos**: valores que se pasan al llamar la función.
* **Analogía final:** Son **ingredientes** que le das a una receta (función) para producir el plato correcto.
* Conexión: [[Definir funciones]], [[Argumentos por defecto]], [[*args y **kwargs]], [[Return]].

---
