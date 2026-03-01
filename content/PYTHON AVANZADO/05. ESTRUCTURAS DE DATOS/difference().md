---
title: difference() — Operaciones con sets en Python
description: Explicación del método difference() para obtener los elementos que están en un set pero no en otro, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, sets, operaciones, difference, analogía]
date: 2026-03-01
---

# difference() — Elementos únicos de un set en Python

El método `difference()` devuelve un nuevo set con **los elementos que están en el set original pero no en los sets comparados**.  

> Relacionado con [[Crear sets]] y [[Operaciones con sets]].

---

## 1. Uso básico de `difference()`

```python
set_a = {1, 2, 3, 4}
set_b = {3, 4, 5, 6}

solo_a = set_a.difference(set_b)
print(solo_a)
````

**Salida:**

```python id="d1r0k"
{1, 2}
```

> **Analogía mental:** Es como **quitar de la primera caja las fichas que también aparecen en la segunda**, quedándote solo con las únicas de la primera.
> Conecta con [[union()]] y [[intersection()]].

---

## 2. Diferencia con varios sets

```python id="d2r1k"
set_c = {2, 3}
resultado_multi = set_a.difference(set_b, set_c)
print(resultado_multi)
```

**Salida:**

```python id="d2r2k"
{1}
```

> **Analogía:** Solo permanece **la ficha que no se repite en ninguna otra caja**.
> Relacionado con [[Operaciones con sets]] y [[List Comprehension]] si quieres procesar resultados.

---

## Buenas prácticas

* `difference()` **no modifica los sets originales**, devuelve un nuevo set.
* Para actualizar un set existente puedes usar `-=`:

```python id="d3r3k"
set_a -= set_b
print(set_a)
```

**Salida:**

```python id="d3r4k"
{1, 2}
```

* Ideal para **filtrar elementos únicos**, eliminar duplicados y comparar colecciones rápidamente.

---

## Resumen

* `difference()` devuelve **los elementos presentes en un set pero ausentes en otros**.
* **Analogía final:** Es como **quedarte solo con las fichas únicas de tu caja**, eliminando las que aparecen en otras cajas.
* Conexión: [[Crear sets]], [[union()]], [[intersection()]], [[Operaciones con sets]].

---

