---
title: Dict Comprehension — Crear diccionarios con comprensión en Python
description: Explicación de Dict Comprehension para crear diccionarios de manera concisa en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, diccionarios, comprensión, analogía]
date: 2026-03-01
---

# Dict Comprehension — Crear diccionarios de manera concisa

La **Dict Comprehension** permite **crear diccionarios en una sola línea** de manera elegante y eficiente, similar a las **List Comprehension**, pero produciendo pares clave-valor.

---

## 1. Sintaxis básica

```python
# Crear un diccionario de cuadrados
cuadrados = {x: x**2 for x in range(5)}
print(cuadrados)
````

**Salida:**

```python id="sq1r2k"
{0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

> **Analogía mental:** Es como **llenar fichas de un archivo automáticamente**: cada número (clave) obtiene su cuadrado (contenido).
> Relacionado con [[Crear diccionarios]], [[List Comprehension]] y [[items()]].

---

## 2. Filtrar elementos

```python
# Crear diccionario solo con números pares
pares = {x: x**2 for x in range(10) if x % 2 == 0}
print(pares)
```

**Salida:**

```python id="sq2r2k"
{0: 0, 2: 4, 4: 16, 6: 36, 8: 64}
```

> **Analogía:** Solo **llenamos fichas de interés**, ignorando las que no cumplen la condición.
> Conecta con [[Condicionales if]] y [[List Comprehension]].

---

## 3. Transformar valores existentes

```python
# Convertir valores de otro diccionario
usuario = {"nombre": "Ángel", "edad": 34}
usuario_mayus = {k: str(v).upper() for k, v in usuario.items()}
print(usuario_mayus)
```

**Salida:**

```python id="sq3r2k"
{'nombre': 'ÁNGEL', 'edad': '34'}
```

> **Analogía:** Es como **copiar fichas y modificar su contenido mientras las traspasas a un nuevo archivo**.
> Relacionado con [[items()]], [[values()]] y [[keys()]].

---

## Buenas prácticas

* Usar Dict Comprehension para **crear diccionarios nuevos de manera concisa**.
* Ideal para **transformaciones, filtrados y automatización** de datos.
* Combinable con métodos de diccionarios como `get()`, `update()` y `items()`.
* Perfecto para trabajar con **JSON, APIs y datos externos** (relacionado con [[JSON y APIs REST]] y [[Sockets]]).

---

## Resumen

* Dict Comprehension permite **crear diccionarios de forma compacta y clara**.
* Puedes añadir **condiciones** o **transformar valores** al vuelo.
* **Analogía final:** Es como **llenar un archivo de fichas automáticamente**, con filtros y transformaciones integradas.
* Conexión: [[Crear diccionarios]], [[List Comprehension]], [[items()]], [[keys()]], [[values()]] y [[Desempaquetado]].

---

