---
title: Módulo math — Matemáticas en Python
description: Uso del módulo math en Python para operaciones matemáticas avanzadas, con ejemplos, resultados y analogías mentales.
tags: [python, modulos, math, matematicas, import, analogía]
date: 2026-03-01
---

# Módulo math en Python

El módulo `math` es un módulo estándar de Python que proporciona **funciones matemáticas avanzadas** como raíces, potencias, logaritmos y constantes.

> Relacionado con [[Importar módulos]], [[Definir funciones]], [[Funciones lambda]].

---

## 1. Importar el módulo

```python
import math
````

> Recuerda: los módulos se cargan usando `import`.
> Ver también [[Importar módulos]].

---

## 2. Raíz cuadrada — `sqrt()`

```python
import math

resultado = math.sqrt(49)
print(resultado)
```

**Salida:**

```python
7.0
```

> **Analogía mental:** `sqrt()` es como una calculadora científica integrada dentro de Python.

---

## 3. Potencias — `pow()`

```python
import math

resultado = math.pow(2, 5)
print(resultado)
```

**Salida:**

```python
32.0
```

> Nota: También puedes usar `**` en Python.

---

## 4. Constantes matemáticas

```python
import math

print(math.pi)
print(math.e)
```

**Salida:**

```python
3.141592653589793
2.718281828459045
```

* `math.pi` → número π
* `math.e` → número e (base de logaritmos naturales)

> **Analogía:** Son como **constantes universales grabadas en piedra**, listas para usar.

---

## 5. Redondeo hacia arriba y abajo

```python
import math

print(math.ceil(4.3))
print(math.floor(4.7))
```

**Salida:**

```python
5
4
```

* `ceil()` → redondea hacia arriba
* `floor()` → redondea hacia abajo

> **Analogía:** `ceil` sube al siguiente piso; `floor` baja al piso inferior.

---

## 6. Valor absoluto y factorial

```python
import math

print(math.fabs(-8))
print(math.factorial(5))
```

**Salida:**

```python
8.0
120
```

* `fabs()` → valor absoluto
* `factorial()` → multiplicación descendente (5 × 4 × 3 × 2 × 1)

---

## 7. Logaritmos

```python
import math

print(math.log(100, 10))
print(math.log2(8))
```

**Salida:**

```python
2.0
3.0
```

---

## Buenas prácticas

* Usar `import math` cuando necesites funciones matemáticas avanzadas.
* Evitar reinventar cálculos que ya existen en el módulo.
* Documentar su uso con [[Docstrings]].
* Integrarlo en funciones propias usando [[Definir funciones]].

---

## Resumen

* `math` ofrece herramientas matemáticas avanzadas.
* Incluye raíces, potencias, logaritmos y constantes.
* Permite cálculos más precisos y profesionales.
* **Analogía final:** El módulo `math` es como una **calculadora científica integrada en Python**, lista para usar en cualquier proyecto.

Conexión: [[Importar módulos]], [[Definir funciones]], [[Funciones lambda]].

---
