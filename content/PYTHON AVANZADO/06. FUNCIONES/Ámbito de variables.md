---
title: Ámbito de variables — Funciones en Python
description: Explicación de los ámbitos locales y globales de variables en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, variables, ámbito, scope, analogía]
date: 2026-03-01
---

# Ámbito de variables en Python

El **ámbito (scope)** de una variable determina **dónde puede ser usada o modificada** dentro del código.  
- **Global:** accesible desde cualquier parte del script.  
- **Local:** accesible solo dentro de la función donde se define.

> Relacionado con [[Definir funciones]], [[Parámetros y argumentos]], [[Return]] y [[Múltiples valores de retorno]].

---

## 1. Variables locales

```python
def funcion_local():
    x = 10  # variable local
    print("Dentro de la función:", x)

funcion_local()
# print(x)  # Esto generaría un error: NameError
````

**Salida:**

```python id="av1r0k"
Dentro de la función: 10
```

> **Analogía mental:** Una variable local es como **un utensilio que solo está en la cocina de una receta**, no puedes usarlo fuera de esa cocina.

---

## 2. Variables globales

```python
y = 20  # variable global

def usar_global():
    print("Dentro de la función:", y)

usar_global()
print("Fuera de la función:", y)
```

**Salida:**

```python id="av2r1k"
Dentro de la función: 20
Fuera de la función: 20
```

> **Analogía:** Una variable global es como **una despensa compartida en toda la casa**, todos los cocineros pueden acceder a ella.

---

## 3. Modificar variables globales desde funciones

```python id="av3r2k"
z = 5

def modificar_global():
    global z
    z += 10
    print("Dentro de la función:", z)

modificar_global()
print("Fuera de la función:", z)
```

**Salida:**

```python id="av3r3k"
Dentro de la función: 15
Fuera de la función: 15
```

> **Analogía:** Usar `global` es como **permitir que la función abra la despensa y cambie los ingredientes**, no solo los lea.

---

## 4. Buenas prácticas

* Evitar abusar de variables globales; favorece la claridad y la seguridad del código.
* Prefiere **parámetros y retorno de valores** para pasar información entre funciones ([Return], [[Múltiples valores de retorno]]).
* Mantener consistencia entre [[Parámetros y argumentos]] y [[Argumentos por defecto]].

---

## Resumen

* **Local:** accesible solo dentro de la función.
* **Global:** accesible en todo el script.
* **Analogía final:** Las variables locales son **herramientas de cocina temporales**, las globales son **ingredientes de la despensa compartida**.
* Conexión: [[Definir funciones]], [[Return]], [[Múltiples valores de retorno]], [[Parámetros y argumentos]].

---

