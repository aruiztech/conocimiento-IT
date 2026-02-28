---
title: Tipo de dato float (Decimales) en Python
description: Explicación completa del tipo float, creación, operaciones, conversiones y errores comunes en Python.
tags: [Python, float, decimales, tipos de datos, aritmética]
date: 2026-02-28
---

# 🐍 Tipo de dato: float (Decimales)

En Python, **float** representa números con decimales.  
Se usa para cálculos precisos, mediciones, porcentajes y cualquier operación que requiera fracciones.

---

## 🔢 Crear floats

```python id="float2"
precio = 19.99
altura = 1.80
saldo = -250.75
````

### ▶ Resultado:

```text id="float3"
precio = 19.99
altura = 1.8
saldo = -250.75
```

---

## 🧮 Operaciones con floats

```python id="float4"
a = 10.5
b = 2.0

print(a + b)   # suma
print(a - b)   # resta
print(a * b)   # multiplicación
print(a / b)   # división
print(a // b)  # división entera
print(a % b)   # módulo (resto)
print(a ** b)  # potencia
```

### ▶ Resultado:

```text id="float5"
12.5
8.5
21.0
5.25
5.0
0.5
110.25
```

---

## 🔄 Conversión a float

Se puede convertir otros tipos a float usando `float()`:

```python id="float6"
x = float(3)        # int → float
y = float("15.7")   # str → float
print(x, y)
```

### ▶ Resultado:

```text id="float7"
3.0 15.7
```

⚠️ No se puede convertir una cadena que no represente un número:

```python id="float8"
z = float("hola")
```

### ▶ Resultado:

```text id="float9"
ValueError: could not convert string to float: 'hola'
```

---

## 🧠 Nota importante

* Dividir enteros con `/` produce siempre un **float**:

```python id="float10"
print(10 / 3)
```

### ▶ Resultado:

```text id="float11"
3.3333333333333335
```

* Usar `//` con floats devuelve la parte entera:

```python id="float12"
print(10.5 // 3)
```

### ▶ Resultado:

```text id="float13"
3.0
```

---

## 🔗 Conecta con

* [[Tipos de datos]]
* [[int]]
* [[str]]
* [[Conversión de tipos]]
* [[Operadores aritméticos]]

---
