---
title: Importar módulos — Modularidad en Python
description: Cómo importar módulos en Python para reutilizar código, con ejemplos, resultados, analogías mentales y conexiones con otras notas.
tags: [python, modulos, import, modularidad, buenas_prácticas, analogía]
date: 2026-03-01
---

# Importar módulos en Python

Los **módulos** permiten organizar y reutilizar código.  
Un módulo es simplemente un archivo `.py` que contiene funciones, variables o clases que pueden ser usadas en otros archivos.

> Relacionado con [[Definir funciones]], [[Docstrings]], [[if __name__ == "__main__"]], [[Funciones como argumentos]].

---

## 1. Importar un módulo completo

```python
import math

resultado = math.sqrt(25)
print(resultado)
````

**Salida:**

```python
5.0
```

Aquí estamos usando el módulo estándar `math` para calcular la raíz cuadrada.

> **Analogía mental:** Importar un módulo es como **abrir una caja de herramientas externa** para usar herramientas que no fabricaste tú.

---

## 2. Importar solo una función

```python
from math import sqrt

resultado = sqrt(36)
print(resultado)
```

**Salida:**

```python
6.0
```

Aquí importamos únicamente `sqrt`, sin necesidad de escribir `math.sqrt()`.

> **Analogía:** Es como **sacar solo el destornillador que necesitas** en vez de traer toda la caja.

---

## 3. Importar con alias

```python
import math as m

resultado = m.pow(2, 3)
print(resultado)
```

**Salida:**

```python
8.0
```

El alias (`as m`) permite abreviar nombres largos.

> **Analogía:** Ponerle apodo a una herramienta para usarla más rápido.

---

## 4. Crear e importar tu propio módulo

Archivo `operaciones.py`:

```python
def sumar(a, b):
    return a + b
```

Archivo principal:

```python
import operaciones

resultado = operaciones.sumar(4, 6)
print(resultado)
```

**Salida:**

```python
10
```

> **Analogía:** Es como crear tu propia caja de herramientas personalizada y luego usarla en otros proyectos.

---

## 5. Buenas prácticas

* Organizar funciones relacionadas en un mismo módulo.
* Usar nombres claros y descriptivos.
* Evitar `from modulo import *` (reduce claridad).
* Documentar funciones con [[Docstrings]].
* Usar `if __name__ == "__main__"` para ejecutar código solo cuando el archivo se ejecuta directamente.

---

## Resumen

* Los módulos permiten **reutilizar y organizar código**.
* Se importan con `import` o `from ... import ...`.
* Se pueden usar alias con `as`.
* Puedes crear tus propios módulos.
* **Analogía final:** Un módulo es una **caja de herramientas reutilizable** que puedes llevar a cualquier proyecto.

Conexión: [[Definir funciones]], [[Docstrings]], [[if **name** == "**main**"]], [[Funciones como argumentos]].

---
