---
title: math.factorial() — Factorial en Python
description: Uso de la función math.factorial() para calcular el factorial de un número en Python, con ejemplos prácticos y analogías mentales.
tags: [python, math, factorial, modulos, matematicas, analogía]
date: 2026-03-01
---

# math.factorial() en Python

La función `math.factorial()` calcula el **factorial** de un número entero no negativo.

El factorial de un número `n` se define como:

n! = n × (n-1) × (n-2) × ... × 1

Forma parte del [[Módulo math]], por lo que debe importarse antes de usarla.

> Relacionado con [[Importar módulos]], [[Módulo math]], [[Definir funciones]], [[Return]].

---

## 1. Sintaxis

```python
import math

math.factorial(numero)
````

* `numero` debe ser un **entero >= 0**
* Devuelve un `int`

---

## 2. Ejemplo básico

```python id="mf1k2a"
import math

resultado = math.factorial(5)
print(resultado)
```

**Salida:**

```python id="mf1r0k"
120
```

Porque:

5! = 5 × 4 × 3 × 2 × 1 = 120

> **Analogía mental:** El factorial es como una **torre de multiplicaciones descendentes** que empieza en el número y baja hasta 1.

---

## 3. Casos especiales

```python id="mf2k3b"
import math

print(math.factorial(0))
```

**Salida:**

```python id="mf2r1k"
1
```

Por definición matemática:

0! = 1

---

## 4. Error con números negativos o decimales

```python id="mf3k4c"
import math

math.factorial(-3)
```

**Resultado:**

```python id="mf3r2k"
ValueError: factorial() not defined for negative values
```

También fallará si usas números decimales.

---

## 5. Implementación manual con función

```python id="mf4k5d"
def factorial_manual(n):
    resultado = 1
    for i in range(1, n + 1):
        resultado *= i
    return resultado

print(factorial_manual(5))
```

**Salida:**

```python id="mf4r3k"
120
```

Relacionado con [[Definir funciones]] y [[Return]].

> **Analogía:** Aquí estás construyendo la torre de multiplicaciones ladrillo por ladrillo.

---

## 6. Uso en combinatoria

El factorial se usa en:

* Permutaciones
* Combinaciones
* Probabilidad
* Criptografía básica

Ejemplo simple:

```python id="mf5k6e"
import math

n = 6
r = 2

combinaciones = math.factorial(n) // (math.factorial(r) * math.factorial(n-r))
print(combinaciones)
```

**Salida:**

```python id="mf5r4k"
15
```

---

## Buenas prácticas

* Usar `math.factorial()` en vez de implementarlo manualmente cuando sea posible.
* Validar que el número sea entero y no negativo.
* Documentar su uso con [[Docstrings]].
* Integrarlo dentro de funciones matemáticas personalizadas con [[Definir funciones]].

---

## Resumen

* `math.factorial(n)` calcula el factorial de un entero >= 0.
* Devuelve un número entero.
* No admite negativos ni decimales.
* Es parte del [[Módulo math]].
* **Analogía final:** Es como una **escalera de multiplicaciones que baja desde el número hasta el 1**, acumulando el resultado.

Conexión: [[Módulo math]], [[Importar módulos]], [[Definir funciones]], [[Return]].

---
