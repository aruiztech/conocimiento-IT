---
title: math.sqrt() — Raíz cuadrada en Python
description: Uso de la función math.sqrt() para calcular raíces cuadradas en Python, con ejemplos prácticos y analogías mentales.
tags: [python, math, sqrt, modulos, matematicas, analogía]
date: 2026-03-01
---

# math.sqrt() en Python

La función `math.sqrt()` devuelve la **raíz cuadrada** de un número.

Forma parte del módulo estándar [[Módulo math]], por lo que debe importarse antes de usarla.

> Relacionado con [[Importar módulos]], [[Módulo math]], [[Definir funciones]].

---

## 1. Sintaxis

```python
import math

math.sqrt(numero)
````

* `numero` debe ser un valor positivo (int o float).
* Devuelve un `float`.

---

## 2. Ejemplo básico

```python
import math

resultado = math.sqrt(64)
print(resultado)
```

**Salida:**

```python id="ms1r0k"
8.0
```

> **Analogía mental:** `math.sqrt()` es como preguntarle a una calculadora científica:
> “¿Qué número multiplicado por sí mismo da este resultado?”

---

## 3. Con variable

```python id="d1k7sh"
import math

numero = 81
raiz = math.sqrt(numero)
print(raiz)
```

**Salida:**

```python id="ms2r1k"
9.0
```

---

## 4. Error con números negativos

```python id="pw3e0q"
import math

math.sqrt(-4)
```

**Resultado:**

```python
ValueError: math domain error
```

El módulo `math` no permite raíces cuadradas de números negativos (para eso se usa `cmath`).

---

## 5. Comparación con operador `**`

También puedes calcular la raíz cuadrada usando potencias:

```python
print(64 ** 0.5)
```

**Salida:**

```python id="ms3r2k"
8.0
```

Pero `math.sqrt()` es **más claro y profesional** cuando trabajas con cálculos matemáticos formales.

---

## Buenas prácticas

* Siempre importar el módulo antes de usar la función:

  ```python
  import math
  ```
* Usar `math.sqrt()` cuando trabajes con cálculos matemáticos serios o científicos.
* Documentar su uso con [[Docstrings]].
* Integrarlo dentro de funciones propias usando [[Definir funciones]].

---

## Resumen

* `math.sqrt()` calcula la raíz cuadrada.
* Requiere importar el módulo `math`.
* Devuelve un número tipo `float`.
* No admite números negativos.
* **Analogía final:** Es como una **calculadora científica integrada en Python especializada en raíces cuadradas**.

Conexión: [[Módulo math]], [[Importar módulos]], [[Definir funciones]], [[Docstrings]].

---
