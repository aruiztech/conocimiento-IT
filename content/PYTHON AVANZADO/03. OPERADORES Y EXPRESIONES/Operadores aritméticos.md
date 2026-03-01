---
title: Operadores aritméticos
description: Operadores matemáticos básicos en Python para int y float, con ejemplos prácticos.
tags: [Python, operadores, aritmética, int, float]
date: 2026-03-01
---

# ➗ Operadores aritméticos

Los **operadores aritméticos** permiten realizar operaciones matemáticas en Python.  
Se usan principalmente con:

- `int`  
- `float`

---

## 📌 Operadores básicos

|Operador|Nombre|Ejemplo|Resultado|
|---|---|---|---|
|`+`|Suma|`5 + 3`|`8`|
|`-`|Resta|`5 - 3`|`2`|
|`*`|Multiplicación|`5 * 3`|`15`|
|`/`|División|`5 / 2`|`2.5`|
|`//`|División entera|`5 // 2`|`2`|
|`%`|Módulo|`5 % 2`|`1`|
|`**`|Potencia|`2 ** 3`|`8`|

---

## 🧮 Ejemplos prácticos

```python id="ex-arit1"
a = 10
b = 3

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a // b)
print(a % b)
print(a ** b)
````

Resultado:

```
13
7
30
3.3333333333333335
3
1
1000
```

---

## 🔎 Diferencia entre `/` y `//`

```python id="ex-arit2"
print(7 / 2)
print(7 // 2)
```

Resultado:

```
3.5
3
```

Con negativos:

```python id="ex-arit3"
print(-7 // 2)
```

Resultado:

```
-4
```

⚠ `//` redondea hacia abajo (floor), no hacia cero.

---

## 🎯 Uso del operador módulo `%`

### 🔹 Saber si un número es par

```python id="ex-mod1"
numero = 8
print(numero % 2)
```

Resultado:

```
0
```

Como el resto es `0`, es par.

---

### 🔹 Ejemplo con número impar

```python id="ex-mod2"
numero = 7
print(numero % 2)
```

Resultado:

```
1
```

---

## 🔥 Potencias con `**`

```python id="ex-pot1"
print(2 ** 4)
print(9 ** 0.5)
```

Resultado:

```
16
3.0
```

---

## ⚠ Error común: división entre cero

```python id="ex-err1"
print(10 / 0)
```

Resultado:

```
ZeroDivisionError: division by zero
```

Relacionado con:

* [[try y except]]
* [[Errores comunes]]

---

## 🧠 Conversión automática de tipos

```python id="ex-tipo1"
print(5 + 2.0)
```

Resultado:

```
7.0
```

Python convierte automáticamente a `float`.
Relacionado con:

* [[Tipos de datos]]
* [[Conversión de tipos]]

---

## 📚 Ejemplo práctico más real

```python id="ex-real1"
precio = 100
cantidad = 3
subtotal = precio * cantidad
impuesto = subtotal * 0.21
total = subtotal + impuesto

print(total)
```

Resultado:

```
363.0
```

---

## 🔗 Notas relacionadas

* [[Operadores de comparación]]
* [[Operadores lógicos]]
* [[Operadores de asignación ampliada]]
* [[Precedencia de operadores]]
* [[Expresiones booleanas]]

---

## 🧪 Mini ejercicios (con resultado esperado)

1️⃣ Convertir 125 minutos en horas y minutos:

```python id="ex-mini1"
minutos = 125
horas = minutos // 60
resto = minutos % 60

print(horas)
print(resto)
```

Resultado:

```
2
5
```

---