---
title: math.sin() — Seno en Python
description: Uso de la función math.sin() para calcular el seno de un ángulo en Python, con ejemplos prácticos y analogías mentales.
tags: [python, math, trigonometria, seno, modulos, analogía]
date: 2026-03-01
---

# math.sin() en Python

La función `math.sin()` calcula el **seno de un ángulo**.

Forma parte del [[Módulo math]], por lo que debe importarse antes de usarla.

⚠ Importante: el ángulo debe estar en **radianes**, no en grados.

> Relacionado con [[Importar módulos]], [[Módulo math]], [[math.cos()]], [[math.tan()]].

---

## 1. Sintaxis

```python
import math

math.sin(x)
````

* `x` → ángulo en **radianes**
* Devuelve un `float`

---

## 2. Ejemplo básico (usando radianes)

```python
import math

resultado = math.sin(math.pi / 2)
print(resultado)
```

**Salida:**

```python
1.0
```

Porque:

sin(π/2) = 1

> **Analogía mental:** El seno mide la **altura de una onda** en un punto específico del círculo unitario.

---

## 3. Convertir grados a radianes

Si tienes grados, debes convertirlos:

Fórmula:
radianes = grados × (π / 180)

Python ya tiene una función para esto:

```python
import math

angulo_grados = 90
angulo_radianes = math.radians(angulo_grados)

print(math.sin(angulo_radianes))
```

**Salida:**

```python
1.0
```

> **Analogía:** Los radianes son el “idioma oficial” de la trigonometría en programación.

---

## 4. Ejemplo con 30 grados

```python
import math

print(math.sin(math.radians(30)))
```

**Salida:**

```python
0.49999999999999994
```

Aproximadamente:

0.5

La pequeña diferencia se debe a precisión decimal.

---

## 5. Uso práctico dentro de una función

```python
import math

def calcular_seno(grados):
    return math.sin(math.radians(grados))

print(calcular_seno(45))
```

**Salida:**

```python
0.7071067811865475
```

Relacionado con [[Definir funciones]] y [[Return]].

---

## 6. Aplicaciones reales

* Física (movimiento ondulatorio)
* Ingeniería
* Gráficos y videojuegos
* Criptografía matemática avanzada
* Procesamiento de señales

---

## Buenas prácticas

* Recordar siempre que `math.sin()` usa **radianes**.
* Convertir grados con `math.radians()`.
* Usar junto con [[math.cos()]] y [[math.tan()]] para trigonometría completa.
* Documentar cálculos complejos con [[Docstrings]].

---

## Resumen

* `math.sin(x)` calcula el seno en radianes.
* Devuelve un `float`.
* Para grados usar `math.radians()`.
* Es parte del [[Módulo math]].
* **Analogía final:** El seno mide la **altura de una onda en movimiento circular**, como el punto más alto de una rueda girando.

Conexión: [[Módulo math]], [[Importar módulos]], [[math.cos()]], [[math.tan()]], [[Definir funciones]].

---
