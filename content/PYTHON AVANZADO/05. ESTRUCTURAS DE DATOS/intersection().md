---
title: intersection() — Operaciones con sets en Python
description: Explicación del método intersection() para obtener elementos comunes entre sets en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, sets, operaciones, intersection, analogía]
date: 2026-03-01
---

# intersection() — Elementos comunes entre sets en Python

El método `intersection()` devuelve un nuevo set que contiene **solo los elementos presentes en todos los sets comparados**.  

> Relacionado con [[Crear sets]] y [[Operaciones con sets]].

---

## 1. Uso básico de `intersection()`

```python
set_a = {1, 2, 3, 4}
set_b = {3, 4, 5, 6}

comunes = set_a.intersection(set_b)
print(comunes)
````

**Salida:**

```python id="i1r0k"
{3, 4}
```

> **Analogía mental:** Como **tomar dos cajas de fichas y quedarte solo con las fichas que están en ambas cajas**.
> Conecta con [[union()]] y [[difference()]].

---

## 2. Intersección de varios sets

```python id="i2r1k"
set_c = {4, 5, 6}
comunes_multi = set_a.intersection(set_b, set_c)
print(comunes_multi)
```

**Salida:**

```python id="i2r2k"
{4}
```

> **Analogía:** Solo permanece **la ficha que está en todas las cajas**.
> Relacionado con [[Operaciones con sets]] y [[List Comprehension]] si quieres procesar los resultados.

---

## Buenas prácticas

* `intersection()` **no modifica los sets originales**, devuelve un nuevo set con los elementos comunes.
* Para actualizar un set existente puedes usar `&=`:

```python id="i3r3k"
set_a &= set_b
print(set_a)
```

**Salida:**

```python id="i3r4k"
{3, 4}
```

* Útil para **filtrar datos, comparar colecciones y detectar coincidencias únicas**.
* Ideal para trabajar con **listas transformadas a sets** (ver [[Crear sets]]).

---

## Resumen

* `intersection()` obtiene **solo los elementos presentes en todos los sets**.
* **Analogía final:** Es como **ver qué fichas tienen todas las cajas en común** y quedarte solo con esas.
* Conexión: [[Crear sets]], [[union()]], [[difference()]], [[Operaciones con sets]].

---
