---
title: Tipo de dato bool (Booleanos) en Python
description: Explicación completa del tipo bool, creación, operaciones lógicas, comparaciones y valores implícitos en Python.
tags: [Python, bool, booleanos, tipos de datos, lógica]
date: 2026-02-28
---

# 🐍 Tipo de dato: bool (Booleanos)

En Python, **bool** representa **valores de verdad**: `True` o `False`.  
Se usan principalmente en **condicionales**, **bucles** y **operaciones lógicas**.

---

## 🔹 Crear booleanos

```python id="bool2"
activo = True
admin = False
````

### ▶ Resultado:

```text id="bool3"
activo = True
admin = False
```

---

## 🔤 Operaciones lógicas básicas

### 🔹 AND (y lógico)

```python id="bool4"
a = True
b = False
print(a and b)  # True si ambos son True
```

### ▶ Resultado:

```text id="bool5"
False
```

---

### 🔹 OR (o lógico)

```python id="bool6"
print(a or b)  # True si al menos uno es True
```

### ▶ Resultado:

```text id="bool7"
True
```

---

### 🔹 NOT (negación)

```python id="bool8"
print(not a)  # invierte el valor
print(not b)
```

### ▶ Resultado:

```text id="bool9"
False
True
```

---

## 🔹 Comparaciones que devuelven bool

Cualquier comparación devuelve un booleano:

```python id="bool10"
x = 10
y = 5

print(x > y)    # mayor que
print(x < y)    # menor que
print(x == y)   # igual a
print(x != y)   # distinto de
print(x >= y)   # mayor o igual
print(x <= y)   # menor o igual
```

### ▶ Resultado:

```text id="bool11"
True
False
False
True
True
False
```

---

## 🔹 Booleanos implícitos

En Python, ciertos valores se consideran **False**:

* `0` (int), `0.0` (float)
* `""` (cadena vacía)
* `[]` (lista vacía)
* `{}` (diccionario vacío)
* `None`

Todo lo demás se considera **True**:

```python id="bool12"
print(bool(0))
print(bool(5))
print(bool([]))
print(bool([1,2,3]))
print(bool(""))
print(bool("Python"))
```

### ▶ Resultado:

```text id="bool13"
False
True
False
True
False
True
```

---

## 🔗 Conecta con

* [[Tipos de datos]]
* [[Operadores lógicos]]
* [[Condicionales if]]
* [[Bucles while y for]]

---