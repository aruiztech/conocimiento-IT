---
title: Función type() en Python
description: Explicación completa de la función type() para verificar tipos de datos en Python, uso con variables, valores directos y comprobaciones en condiciones.
tags: [Python, type(), tipos de datos, verificación, depuración]
date: 2026-02-28
---

# 🐍 Función: type()

La función **`type()`** devuelve el **tipo de dato** de un valor o variable en Python.  
Se usa para **verificar tipos**, depurar código y entender cómo Python interpreta los datos.

---

## 🔹 Uso básico con variables

```python id="type2"
x = 10
y = 3.14
nombre = "Angel"
activo = True
nada = None

print(type(x))
print(type(y))
print(type(nombre))
print(type(activo))
print(type(nada))
````

### ▶ Resultado:

```text id="type3"
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
<class 'NoneType'>
```

---

## 🔹 Uso con valores directos

```python id="type4"
print(type(42))
print(type(2.718))
print(type("Hola"))
print(type([1,2,3]))
print(type((10,20)))
print(type({"a":1, "b":2}))
print(type({1,2,3}))
```

### ▶ Resultado:

```text id="type5"
<class 'int'>
<class 'float'>
<class 'str'>
<class 'list'>
<class 'tuple'>
<class 'dict'>
<class 'set'>
```

---

## 🔹 Comprobación de tipo en condiciones

```python id="type6"
x = 15

if type(x) is int:
    print("x es un entero")
else:
    print("x no es un entero")
```

### ▶ Resultado:

```text id="type7"
x es un entero
```

---

## 🔹 Nota importante

* `type()` devuelve el **tipo exacto**, no un nombre simplificado.
* Para comparar tipos, es recomendable usar **`is`** en lugar de `==`.

```python id="type8"
x = 3.14
print(type(x) is float)  # True
print(type(x) == float)  # También funciona, pero less idiomático
```

### ▶ Resultado:

```text id="type9"
True
True
```

---

## 🔗 Conecta con

* [[Tipos de datos]]
* [[int]]
* [[float]]
* [[str]]
* [[bool]]
* [[None]]
* [[Conversión de tipos]]

---
