---
title: Conversión de tipos en Python
description: Explicación sobre cómo convertir valores entre tipos en Python usando type casting.
tags: [Python, type casting, conversión de tipos]
date: 2026-02-28
---

# Conversión de tipos (Type Casting)

En Python, puedes convertir un valor de un tipo a otro usando **funciones integradas** como `int()`, `float()`, `str()`, `bool()`.  
Esto se llama **type casting** o **conversión de tipos**.

---

## Convertir a int

```python id="int01"
# De float a int
x = int(3.7)
print(x)

# De str a int
y = int("15")
print(y)

# De bool a int
a = int(True)
b = int(False)
print(a, b)
````

### Resultado:

```text id="int02"
3
15
1 0
```

⚠️ `int()` trunca decimales, no redondea.
Cadenas deben representar números, de lo contrario da error.

---

## Convertir a float

```python id="float01"
# De int a float
x = float(10)
print(x)

# De str a float
y = float("3.14")
print(y)

# De bool a float
a = float(True)
b = float(False)
print(a, b)
```

### Resultado:

```text id="float02"
10.0
3.14
1.0 0.0
```

---

## Convertir a str

```python id="str01"
# De int a str
x = str(123)
print(x, type(x))

# De float a str
y = str(3.14)
print(y, type(y))

# De bool a str
z = str(True)
print(z, type(z))
```

### Resultado:

```text id="str02"
123 <class 'str'>
3.14 <class 'str'>
True <class 'str'>
```

---

## Convertir a bool

```python id="bool01"
# Números
print(bool(0))       # False
print(bool(42))      # True

# Cadenas
print(bool(""))      # False
print(bool("Python"))# True

# None
print(bool(None))    # False
```

### Resultado:

```text id="bool02"
False
True
False
True
False
```

---

## Conversiones entre estructuras de datos

```python id="struct01"
# Lista a set
lista = [1, 2, 2, 3]
conjunto = set(lista)
print(conjunto)

# Tupla a lista
tupla = (4, 5, 6)
lista2 = list(tupla)
print(lista2)

# Diccionario a lista de claves
dic = {"a": 1, "b": 2}
claves = list(dic)
print(claves)
```

### Resultado:

```text id="struct02"
{1, 2, 3}
[4, 5, 6]
['a', 'b']
```

---

## Conecta con

* [[Tipos de datos]]
* [[int]]
* [[float]]
* [[str]]
* [[bool]]
* [[None]]
* [[type()]]
