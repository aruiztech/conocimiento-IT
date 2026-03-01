---
title: union() — Operaciones con sets en Python
description: Explicación del método union() para combinar sets en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, sets, operaciones, union, analogía]
date: 2026-03-01
---

# union() — Combinar sets en Python

El método `union()` permite **combinar dos o más sets** en un nuevo set, **eliminando duplicados automáticamente**.  

> Relacionado con [[Crear sets]] y [[Operaciones con sets]].

---

## 1. Uso básico de `union()`

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

resultado = set_a.union(set_b)
print(resultado)
````

**Salida:**

```python id="u1r0k"
{1, 2, 3, 4, 5}
```

> **Analogía mental:** Como **tomar dos cajas de fichas únicas y combinarlas en una sola**, sin repetir ninguna ficha.
> Conecta con [[Crear sets]] y [[intersection()]].

---

## 2. Unión de varios sets

```python
set_c = {5, 6, 7}
resultado_multi = set_a.union(set_b, set_c)
print(resultado_multi)
```

**Salida:**

```python id="u1r1k"
{1, 2, 3, 4, 5, 6, 7}
```

> **Analogía:** Combinas **varias colecciones de fichas únicas** en un solo archivo completo.
> Relacionado con [[difference()]] y [[Operaciones con sets]].

---

## Buenas prácticas

* `union()` **no modifica los sets originales**, devuelve un nuevo set.
* Para actualizar un set existente puedes usar `|=`:

```python
set_a |= set_b
print(set_a)
```

**Salida:**

```python id="u1r2k"
{1, 2, 3, 4, 5}
```

* Ideal para **combinar datos únicos**, filtrar duplicados y mantener colecciones consistentes.

---

## Resumen

* `union()` combina sets **sin duplicados**, devolviendo un nuevo set.
* **Analogía final:** Es como **abrir varias cajas de fichas únicas y volcar todo en una sola**, manteniendo solo elementos únicos.
* Conexión: [[Crear sets]], [[intersection()]], [[difference()]], [[Operaciones con sets]].

---
