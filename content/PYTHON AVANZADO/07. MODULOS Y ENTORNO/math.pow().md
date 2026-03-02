---
title: math.pow() — Potencias en Python
description: Uso de la función math.pow() para calcular potencias en Python, con ejemplos prácticos y comparación con el operador **.
tags: [python, math, pow, modulos, matematicas, analogía]
date: 2026-03-01
---

# math.pow() en Python

La función `math.pow()` devuelve un número elevado a una potencia.

Forma parte del módulo estándar [[Módulo math]], por lo que debe importarse antes de usarla.

> Relacionado con [[Importar módulos]], [[Módulo math]], [[math.sqrt()]], [[Definir funciones]].

---

## 1. Sintaxis

```python
import math

math.pow(base, exponente)
````

* `base` → número base
* `exponente` → potencia
* Devuelve siempre un `float`

---

## 2. Ejemplo básico

```python
import math

resultado = math.pow(2, 3)
print(resultado)
```

**Salida:**

```python
8.0
```

> **Analogía mental:** `math.pow()` es como una calculadora científica que multiplica un número por sí mismo tantas veces como indique el exponente.

---

## 3. Con números decimales

```python
import math

resultado = math.pow(9, 0.5)
print(resultado)
```

**Salida:**

```python
3.0
```

Aquí estamos calculando la raíz cuadrada usando potencia decimal.
Ver también [[math.sqrt()]].

---

## 4. Diferencia con el operador `**`

Python también permite usar el operador de potencia:

```python
print(2 ** 3)
```

**Salida:**

```python
8
```

Diferencias importantes:

| math.pow()                        | **                                  |
| --------------------------------- | ----------------------------------- |
| Siempre devuelve `float`          | Devuelve `int` si ambos son enteros |
| Requiere importar `math`          | No requiere importación             |
| Más formal en contexto científico | Más común en código general         |

> **Analogía:**
>
> * `math.pow()` → calculadora científica formal.
> * `**` → multiplicación rápida hecha mentalmente.

---

## 5. Uso dentro de funciones

```python
import math

def potencia_segura(base, exponente):
    return math.pow(base, exponente)

print(potencia_segura(4, 2))
```

**Salida:**

```python
16.0
```

Relacionado con [[Definir funciones]] y [[Return]].

---

## Buenas prácticas

* Usar `math.pow()` en cálculos matemáticos formales o científicos.
* Usar `**` cuando busques simplicidad y rendimiento.
* Documentar funciones matemáticas con [[Docstrings]].
* Mantener consistencia dentro del proyecto.

---

## Resumen

* `math.pow(base, exponente)` calcula potencias.
* Siempre devuelve `float`.
* Es parte del [[Módulo math]].
* Alternativa: operador `**`.
* **Analogía final:** `math.pow()` es como usar una **calculadora científica oficial**, mientras que `**` es hacer el cálculo directamente con lápiz y papel.

Conexión: [[Módulo math]], [[math.sqrt()]], [[Importar módulos]], [[Definir funciones]], [[Return]].

---

