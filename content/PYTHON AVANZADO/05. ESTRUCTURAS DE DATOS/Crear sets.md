---
title: Crear sets — Conjuntos en Python
description: Explicación de cómo crear sets en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, sets, estructuras, analogía]
date: 2026-03-01
---

# Crear sets en Python

Un **set** es una colección **no ordenada y sin elementos duplicados**.  
Se utiliza para **almacenar elementos únicos** y realizar operaciones matemáticas como unión, intersección y diferencia.

---

## 1. Crear un set vacío

```python
# Forma correcta
mi_set = set()
print(mi_set)
````

**Salida:**

```python id="s1r0k"
set()
```

> **Analogía mental:** Un set vacío es como **una caja vacía donde solo caben objetos únicos**, sin repetir.

---

## 2. Crear un set con elementos

```python
frutas = {"manzana", "banana", "naranja", "manzana"}
print(frutas)
```

**Salida:**

```python id="s1r1k"
{'manzana', 'banana', 'naranja'}
```

> **Analogía:** Aunque pongas varias fichas de “manzana”, el set **guarda solo una**, como si fueran **tarjetas únicas en una colección**.
> Conecta con [[Crear listas]] y [[List Comprehension]] para entender diferencias entre listas y sets.

---

## 3. Crear un set a partir de una lista

```python
numeros = [1, 2, 2, 3, 4, 4, 5]
set_numeros = set(numeros)
print(set_numeros)
```

**Salida:**

```python id="s1r2k"
{1, 2, 3, 4, 5}
```

> **Analogía:** Es como **filtrar fichas repetidas de un montón de papeles**, quedándote solo con los elementos únicos.
> Relacionado con [[Mutabilidad vs inmutabilidad]] y [[List Comprehension]].

---

## Buenas prácticas

* Usar sets cuando necesites **elementos únicos** y no te importe el orden.
* Ideal para **comparaciones, filtros y operaciones matemáticas**.
* Combina con métodos de sets como `union()`, `intersection()` y `difference()` (ver [[Operaciones con sets]]).
* Útil para eliminar duplicados de listas rápidamente.

---

## Resumen

* Los sets son **colecciones no ordenadas y sin duplicados**.
* Pueden crearse vacíos, con elementos o a partir de listas.
* **Analogía final:** Un set es como **una caja de fichas únicas**, perfecta para asegurarte de que no se repita ninguna.
* Conexión: [[Operaciones con sets]], [[Crear listas]], [[List Comprehension]] y [[Mutabilidad vs inmutabilidad]].

---
