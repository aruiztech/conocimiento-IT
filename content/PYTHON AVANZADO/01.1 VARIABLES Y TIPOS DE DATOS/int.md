---
title: Tipo de dato int (Enteros) en Python
description: Explicación completa del tipo int, creación, operaciones, conversiones y errores comunes en Python.
tags: [Python, int, enteros, tipos de datos, aritmética]
date: 2026-02-28
---

# 🐍 Tipo de dato: int (Enteros)

En Python, **int** representa números enteros, positivos o negativos, sin decimales.  
Se usan para contar, calcular, índices, bucles y muchas operaciones matemáticas.

---

## 🔢 Crear enteros

```python id="int1"
edad = 34
saldo = -100
````

### ▶ Resultado:

```text id="int2"
edad = 34
saldo = -100
```

---

## 🧮 Operaciones con enteros

```python id="int3"
a = 10
b = 3

print(a + b)   # suma
print(a - b)   # resta
print(a * b)   # multiplicación
print(a // b)  # división entera
print(a % b)   # módulo (resto)
print(a ** b)  # potencia
```

### ▶ Resultado:

```text id="int4"
13
7
30
3
1
1000
```

---

## 🔄 Conversión a int

Se puede convertir otros tipos a int usando `int()`:

```python id="int5"
x = int(3.7)      # float → int
y = int("15")     # str → int
print(x, y)
```

### ▶ Resultado:

```text id="int6"
3 15
```

⚠️ `int()` **trunca** los decimales, no redondea:

```python id="int7"
x = int(7.9)
print(x)
```

### ▶ Resultado:

```text id="int8"
7
```

---

## ❌ Errores comunes

* Intentar convertir cadenas que no son números:

```python id="int9"
x = int("hola")
```

### ▶ Resultado:

```text id="int10"
ValueError: invalid literal for int() with base 10: 'hola'
```

* Dividir enteros usando `/` produce **float**, no int:

```python id="int11"
print(10 / 3)
```

### ▶ Resultado:

```text id="int12"
3.3333333333333335
```

Para obtener un entero, usar `//` (división entera).

---

## 🔗 Conecta con

* [[Tipos de datos]]
* [[float]]
* [[Conversión de tipos]]
* [[Operadores aritméticos]]

---

