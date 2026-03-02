---
title: Módulo random — Números aleatorios en Python
description: Uso del módulo random en Python para generar números aleatorios, seleccionar elementos y mezclar datos.
tags: [python, modulos, random, aleatorio, seguridad, analogía]
date: 2026-03-01
---

# Módulo random en Python

El módulo `random` permite generar **números y selecciones aleatorias**.

Se usa en:

- Juegos
- Simulaciones
- Generación de datos
- Scripts
- Pruebas
- Automatización

> Relacionado con [[Importar módulos]], [[Definir funciones]], [[Funciones lambda]].

⚠ Nota: No es seguro para criptografía. Para seguridad real usar `secrets`.

---

## 1. Importar el módulo

```python
import random
````

Ver también [[Importar módulos]].

---

## 2. Número aleatorio decimal — `random()`

```python id="r1a2b3"
import random

print(random.random())
```

**Salida (ejemplo):**

```python id="r1r0k"
0.374829102834
```

* Devuelve un número entre 0.0 y 1.0

> **Analogía mental:** Es como girar una ruleta que siempre cae entre 0 y 1.

---

## 3. Número entero aleatorio — `randint()`

```python id="r2a3b4"
import random

print(random.randint(1, 10))
```

**Salida (ejemplo):**

```python id="r2r1k"
7
```

* Incluye ambos extremos (1 y 10)

> **Analogía:** Sacar una bola numerada de una bolsa del 1 al 10.

---

## 4. Número en rango — `randrange()`

```python id="r3a4b5"
import random

print(random.randrange(0, 20, 2))
```

**Salida (ejemplo):**

```python id="r3r2k"
14
```

* Similar a `range()`
* Permite pasos personalizados

---

## 5. Elegir elemento aleatorio — `choice()`

```python id="r4a5b6"
import random

colores = ["rojo", "azul", "verde"]
print(random.choice(colores))
```

**Salida (ejemplo):**

```python id="r4r3k"
azul
```

> **Analogía:** Cerrar los ojos y elegir un papel de una caja.

Relacionado con [[List Comprehension]] y estructuras como listas.

---

## 6. Mezclar lista — `shuffle()`

```python id="r5a6b7"
import random

numeros = [1, 2, 3, 4, 5]
random.shuffle(numeros)
print(numeros)
```

**Salida (ejemplo):**

```python id="r5r4k"
[3, 1, 5, 2, 4]
```

> **Analogía:** Barajar una baraja de cartas.

---

## 7. Selección múltiple — `sample()`

```python id="r6a7b8"
import random

numeros = [1, 2, 3, 4, 5]
print(random.sample(numeros, 3))
```

**Salida (ejemplo):**

```python id="r6r5k"
[4, 1, 5]
```

Selecciona elementos únicos sin repetir.

---

## 8. Ejemplo práctico

Simulador de dado:

```python id="r7a8b9"
import random

def lanzar_dado():
    return random.randint(1, 6)

print(lanzar_dado())
```

**Salida (ejemplo):**

```python id="r7r6k"
4
```

Relacionado con [[Definir funciones]] y [[Return]].

---

## 9. Advertencia de seguridad

El módulo `random` NO es seguro para:

* Generar contraseñas
* Tokens
* Criptografía

Para eso usar el módulo `secrets`.

Esto es importante en contextos de ciberseguridad.

---

## Buenas prácticas

* Usar `randint()` para números enteros.
* Usar `choice()` para listas.
* Usar `shuffle()` para mezclar.
* No usar `random` en sistemas de seguridad.
* Documentar funciones con [[Docstrings]].

---

## Resumen

* `random` genera valores aleatorios.
* Incluye números, selección y mezcla.
* No es seguro para criptografía.
* **Analogía final:** El módulo `random` es como una **ruleta digital integrada en Python** que genera resultados impredecibles.

Conexión: [[Importar módulos]], [[Definir funciones]], [[List Comprehension]].

---
