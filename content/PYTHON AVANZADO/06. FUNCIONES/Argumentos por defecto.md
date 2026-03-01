---
title: Argumentos por defecto — Funciones en Python
description: Explicación de los argumentos por defecto en funciones Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, argumentos, defecto, analogía]
date: 2026-03-01
---

# Argumentos por defecto en funciones Python

Los **argumentos por defecto** permiten **asignar un valor predeterminado a un parámetro** si no se proporciona un argumento al llamar la función.  

> Relacionado con [[Parámetros y argumentos]], [[*args y **kwargs]], [[Definir funciones]] y [[Return]].

---

## 1. Uso básico de argumentos por defecto

```python
def saludar(nombre="Usuario"):
    print(f"¡Hola, {nombre}!")
    
saludar("Ángel")  # Se pasa argumento
saludar()         # Se usa valor por defecto
````

**Salida:**

```python id="ad1r0k"
¡Hola, Ángel!
¡Hola, Usuario!
```

> **Analogía mental:** Es como **una receta que tiene un ingrediente por defecto**, pero puedes reemplazarlo si quieres.

---

## 2. Combinación de argumentos con y sin valor por defecto

```python id="ad2r1k"
def presentar(nombre, edad=30):
    print(f"Me llamo {nombre} y tengo {edad} años.")

presentar("Ángel")      # usa valor por defecto de edad
presentar("Laura", 25)  # se pasa un argumento
```

**Salida:**

```python id="ad2r2k"
Me llamo Ángel y tengo 30 años.
Me llamo Laura y tengo 25 años.
```

> **Analogía:** Piensa en **una receta de café**: si no dices cuánta azúcar quieres, la receta usa la cantidad estándar.

---

## Buenas prácticas

* Colocar siempre **los parámetros con valor por defecto al final** de la lista de parámetros.
* Evitar usar **valores mutables como listas o diccionarios** como argumentos por defecto (puede generar errores inesperados).
* Combinar con [[*args y **kwargs]] para funciones más flexibles.

```python id="ad3r3k"
def agregar_elementos(lista=[]):
    lista.append(1)
    return lista

print(agregar_elementos())
print(agregar_elementos())
```

**Salida (problema clásico):**

```python id="ad3r4k"
[1]
[1, 1]  # La lista se mantiene entre llamadas
```

> Solución: usar `None` como valor por defecto y crear la lista dentro de la función.

---

## Resumen

* Los argumentos por defecto **proporcionan flexibilidad y valores predeterminados**.
* **Analogía final:** Es como **ingredientes de reserva en una receta**, que se usan si no indicas otro valor.
* Conexión: [[Parámetros y argumentos]], [[*args y **kwargs]], [[Definir funciones]], [[Return]].

---

