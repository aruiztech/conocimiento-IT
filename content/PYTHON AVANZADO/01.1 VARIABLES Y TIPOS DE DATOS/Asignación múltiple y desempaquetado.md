---
title: Asignación múltiple y desempaquetado en Python
description: Explicación de cómo asignar valores a varias variables a la vez y cómo desempaquetar listas o tuplas.
tags: [Python, Variables, Asignación, Desempaquetado, Listas, Tuplas]
date: 2026-02-28
---

# 🐍 Asignación múltiple y desempaquetado

En Python puedes **asignar valores a varias variables en una sola línea** y también **desempaquetar colecciones** (listas, tuplas) directamente en variables.

---

## 🧠 Analogía mental

Imagina que tienes varias **cajas alineadas** y una **cesta con objetos**:

- Cada caja es una variable.
- La cesta tiene los objetos que quieres distribuir.
- El **desempaquetado** es repartir cada objeto de la cesta a su caja correspondiente, **uno a uno**.

```text id="asignacion_multiples2"
a, b, c = 1, 2, 3
# → 1 va a a, 2 va a b, 3 va a c
````

---

## 🔹 Asignación múltiple básica

```python id="asignacion_multiples3"
x, y, z = 10, 20, 30
print(x, y, z)
```

### ▶ Resultado:

```text id="asignacion_multiples4"
10 20 30
```

---

## 🔹 Intercambiar valores usando asignación múltiple

```python id="asignacion_multiples5"
a = 5
b = 10

a, b = b, a
print(a, b)
```

### ▶ Resultado:

```text id="asignacion_multiples6"
10 5
```

> Forma elegante de intercambiar valores sin usar variable temporal.

---

## 🔹 Desempaquetar listas o tuplas

```python id="asignacion_multiples7"
valores = [1, 2, 3]
a, b, c = valores
print(a, b, c)
```

### ▶ Resultado:

```text id="asignacion_multiples8"
1 2 3
```

También funciona con tuplas:

```python id="asignacion_multiples9"
datos = (10, 20, 30)
x, y, z = datos
print(x, y, z)
```

### ▶ Resultado:

```text id="asignacion_multiples10"
10 20 30
```

---

## 🔹 Desempaquetado con `*` (resto de elementos)

```python id="asignacion_multiples11"
valores = [1, 2, 3, 4, 5]
a, b, *resto = valores
print(a, b, resto)
```

### ▶ Resultado:

```text id="asignacion_multiples12"
1 2 [3, 4, 5]
```

* `a` recibe el primer elemento
* `b` recibe el segundo
* `resto` recibe una **lista con los elementos restantes**

---

## 🔗 Conecta con

* [[Asignación en Python]]
* [[Variables]]
* [[Listas]]
* [[Tuplas]]

---
