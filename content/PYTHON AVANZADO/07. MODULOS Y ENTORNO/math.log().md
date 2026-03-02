---
title: math.log() — Logaritmos en Python
description: Uso de la función math.log() para calcular logaritmos en Python, con ejemplos prácticos y analogías mentales.
tags: [python, math, logaritmos, modulos, matematicas, analogía]
date: 2026-03-01
---

# math.log() en Python

La función `math.log()` calcula el **logaritmo** de un número.

Forma parte del [[Módulo math]], por lo que debe importarse antes de usarla.

> Relacionado con [[Importar módulos]], [[Módulo math]], [[math.pow()]], [[math.factorial()]].

---

## 1. Sintaxis

```python
import math

math.log(x, base)
````

* `x` → número positivo
* `base` → base del logaritmo (opcional)
* Devuelve un `float`

Si no se especifica la base, calcula el **logaritmo natural (base e)**.

---

## 2. Logaritmo natural (base e)

```python id="ml1k2a"
import math

resultado = math.log(10)
print(resultado)
```

**Salida:**

```python id="ml1r0k"
2.302585092994046
```

Este es el logaritmo natural (ln 10).

> **Analogía mental:** El logaritmo natural responde a la pregunta:
> “¿A qué potencia debo elevar el número e para obtener este valor?”

---

## 3. Logaritmo en base específica

```python id="ml2k3b"
import math

resultado = math.log(100, 10)
print(resultado)
```

**Salida:**

```python id="ml2r1k"
2.0
```

Porque:

10² = 100

---

## 4. Funciones relacionadas

### Logaritmo base 10

```python id="ml3k4c"
import math

print(math.log10(1000))
```

**Salida:**

```python id="ml3r2k"
3.0
```

---

### Logaritmo base 2

```python id="ml4k5d"
import math

print(math.log2(8))
```

**Salida:**

```python id="ml4r3k"
3.0
```

> **Analogía:**
>
> * `log2()` es muy usado en informática (bits).
> * `log10()` es común en cálculos científicos.
> * `log()` es el más general.

---

## 5. Error con valores inválidos

```python id="ml5k6e"
import math

math.log(-5)
```

**Resultado:**

```python id="ml5r4k"
ValueError: math domain error
```

El logaritmo solo está definido para números positivos.

---

## 6. Relación con potencias

Los logaritmos son la operación inversa de la potencia.

```python id="ml6k7f"
import math

print(math.pow(10, 2))
print(math.log(100, 10))
```

**Salida:**

```python id="ml6r5k"
100.0
2.0
```

> **Analogía clave:**
>
> * `pow()` construye la torre.
> * `log()` pregunta cuántos pisos tiene la torre.

Relacionado con [[math.pow()]].

---

## Buenas prácticas

* Usar `math.log(x, base)` cuando necesites una base personalizada.
* Usar `log2()` en cálculos relacionados con informática y bits.
* Validar que el número sea positivo.
* Documentar cálculos complejos con [[Docstrings]].

---

## Resumen

* `math.log(x)` → logaritmo natural (base e).
* `math.log(x, base)` → logaritmo en base personalizada.
* `math.log10(x)` → base 10.
* `math.log2(x)` → base 2.
* Solo acepta números positivos.
* **Analogía final:** El logaritmo responde a la pregunta:
  “¿Cuántas veces debo multiplicar la base por sí misma para obtener este número?”

Conexión: [[Módulo math]], [[math.pow()]], [[math.factorial()]], [[Importar módulos]].

---
