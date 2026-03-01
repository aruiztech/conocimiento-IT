---
title: Funciones lambda — Python
description: Explicación de funciones lambda en Python para crear funciones anónimas, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, lambda, funciones_anonimas, analogía]
date: 2026-03-01
---

# Funciones lambda en Python

Las **funciones lambda** son funciones **pequeñas y anónimas** que se definen en una sola línea.  
Se usan para tareas **simples y rápidas** sin necesidad de declarar una función completa con `def`.

> Relacionado con [[Definir funciones]], [[Parámetros y argumentos]], [[Return]], [[Múltiples valores de retorno]].

---

## 1. Sintaxis básica

```python
# lambda argumentos: expresión
suma = lambda a, b: a + b

resultado = suma(4, 7)
print(resultado)
````

**Salida:**

```python id="lmb1r0k"
11
```

> **Analogía mental:** Una función lambda es como **un micro-cuchillo** que hace cortes rápidos sin necesidad de usar toda la cocina; es útil para tareas puntuales.

---

## 2. Uso con listas y funciones como argumento

```python
numeros = [1, 2, 3, 4, 5]
cuadrados = list(map(lambda x: x**2, numeros))
print(cuadrados)
```

**Salida:**

```python id="lmb2r1k"
[1, 4, 9, 16, 25]
```

> **Analogía:** La función lambda es como **una máquina pequeña que transforma cada ingrediente** de la lista sin necesidad de escribir un proceso completo.

> Relacionado con [[List Comprehension]] y [[Funciones como argumentos]].

---

## 3. Uso con `filter` y `reduce`

```python
from functools import reduce

# Filtrar números pares
pares = list(filter(lambda x: x % 2 == 0, numeros))
print(pares)

# Sumar todos los números usando reduce
suma_total = reduce(lambda a, b: a + b, numeros)
print(suma_total)
```

**Salida:**

```python id="lmb3r2k"
[2, 4]
15
```

> **Analogía:** Lambda funciona como **pequeños ayudantes especializados** que realizan tareas específicas en la lista sin declarar funciones completas.

---

## 4. Buenas prácticas

* Usar lambda para **funciones pequeñas y simples**.
* Evitar lambdas complejas que reduzcan la legibilidad del código.
* Siempre que necesites múltiples líneas, usa `def` ([Definir funciones]).
* Útil junto con [[Map, Filter, Reduce]] y [[List Comprehension]].

---

## Resumen

* Lambda = función pequeña, rápida y anónima.
* Sintaxis: `lambda argumentos: expresión`.
* Perfecta para **operaciones puntuales**, especialmente al combinar con [[Funciones como argumentos]], [[Map]], [[Filter]] y [[List Comprehension]].
* **Analogía final:** Es como **una navaja multiuso pequeña y rápida** que hace cortes precisos sin necesidad de preparar toda la cocina.
* Conexión: [[Definir funciones]], [[Return]], [[Parámetros y argumentos]], [[Múltiples valores de retorno]], [[Funciones como argumentos]], [[List Comprehension]].

---

