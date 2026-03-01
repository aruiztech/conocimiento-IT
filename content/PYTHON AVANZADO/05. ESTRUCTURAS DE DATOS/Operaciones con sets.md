---
title: Operaciones con sets — union(), intersection(), difference() en Python
description: Explicación de las operaciones básicas con sets en Python: union(), intersection() y difference(), con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, sets, operaciones, analogía]
date: 2026-03-01
---

# Operaciones con sets en Python

Los sets permiten realizar **operaciones matemáticas** de manera eficiente:  
- `union()` → unión de sets  
- `intersection()` → intersección de sets  
- `difference()` → diferencia de sets  

> Relacionado con [[Crear sets]] y [[Mutabilidad vs inmutabilidad]].

---

## 1. Unión de sets — `union()`

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

union_set = set_a.union(set_b)
print(union_set)
````

**Salida:**

```python id="u1r0k"
{1, 2, 3, 4, 5}
```

> **Analogía mental:** Combinar dos cajas de fichas únicas en **una sola caja**, sin repetir elementos.
> Conecta con [[Crear sets]].

---

## 2. Intersección de sets — `intersection()`

```python
interseccion_set = set_a.intersection(set_b)
print(interseccion_set)
```

**Salida:**

```python id="u1r1k"
{3}
```

> **Analogía:** Solo las fichas que **están en ambas cajas** permanecen, como elementos comunes en dos colecciones.
> Relacionado con [[values()]] y [[items()]] cuando quieres filtrar elementos.

---

## 3. Diferencia de sets — `difference()`

```python
diferencia_set = set_a.difference(set_b)
print(diferencia_set)
```

**Salida:**

```python id="u1r2k"
{1, 2}
```

> **Analogía:** Quitar de la primera caja las fichas que también están en la segunda.
> Útil para filtrar datos y eliminar duplicados no deseados, conecta con [[List Comprehension]].

---

## Buenas prácticas

* Usar sets y sus operaciones para **comparaciones rápidas y limpieza de datos**.
* Ideal para resolver problemas de **pertenencia, duplicados o coincidencias**.
* Combinar con List Comprehension o Dict Comprehension para **transformar resultados en listas o diccionarios**.
* Operaciones eficientes incluso con sets grandes (relacionado con [[Mutabilidad vs inmutabilidad]]).

---

## Resumen

* `union()` → combina todos los elementos sin duplicados.
* `intersection()` → mantiene solo los elementos comunes.
* `difference()` → elimina los elementos presentes en otro set.
* **Analogía final:** Manipular sets es como **jugar con cajas de fichas únicas**, combinando, filtrando o eliminando según tus reglas.
* Conexión: [[Crear sets]], [[Mutabilidad vs inmutabilidad]], [[List Comprehension]].

---
