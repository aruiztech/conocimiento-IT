---
title: f-strings en Python
description: Uso de f-strings para formatear cadenas en Python, insertar variables, expresiones y formatear números.
tags: [Python, str, f-strings, formateo, cadenas]
date: 2026-02-28
---

# 🐍 f-strings en Python

Las **f-strings** (formatted string literals) son la forma más moderna y recomendada de insertar variables dentro de cadenas de texto.  
Se introdujeron en Python 3.6.

---

## 🧠 Analogía mental

Imagina que una f-string es como una **plantilla inteligente** 🧾.  
Escribes el texto normal y dentro colocas espacios `{}` donde quieres que Python inserte valores automáticamente.

---

## 🔹 Sintaxis básica

Se coloca una `f` antes de las comillas y se usan `{}` para insertar variables.

```python id="fstrings2"
nombre = "Angel"
edad = 34

mensaje = f"{nombre} tiene {edad} años"
print(mensaje)
````

### ▶ Resultado:

```text id="fstrings3"
Angel tiene 34 años
```

---

## 🔹 Insertar expresiones

Dentro de `{}` puedes escribir operaciones.

```python id="fstrings4"
a = 10
b = 5

print(f"La suma es {a + b}")
```

### ▶ Resultado:

```text id="fstrings5"
La suma es 15
```

No solo variables: ¡también cálculos!

---

## 🔹 Llamar funciones dentro

```python id="fstrings6"
nombre = "angel"

print(f"En mayúsculas: {nombre.upper()}")
```

### ▶ Resultado:

```text id="fstrings7"
En mayúsculas: ANGEL
```

---

## 🔹 Formatear números

### Decimales

```python id="fstrings8"
precio = 19.9876

print(f"Precio: {precio:.2f}")
```

### ▶ Resultado:

```text id="fstrings9"
Precio: 19.99
```

`.2f` → 2 decimales.

---

### Separador de miles

```python id="fstrings10"
numero = 1000000

print(f"{numero:,}")
```

### ▶ Resultado:

```text id="fstrings11"
1,000,000
```

---

## 🔹 Alineación

```python id="fstrings12"
texto = "Python"

print(f"|{texto:>10}|")
print(f"|{texto:<10}|")
print(f"|{texto:^10}|")
```

### ▶ Resultado:

```text id="fstrings13"
|    Python|
|Python    |
|  Python  |
```

* `>` derecha
* `<` izquierda
* `^` centrado

---

## 🔥 Comparación con otras formas

### Concatenación clásica

```python id="fstrings14"
nombre = "Angel"
edad = 34

print("Nombre: " + nombre + " Edad: " + str(edad))
```

Menos limpio ❌

---

### Método format()

```python id="fstrings15"
print("Nombre: {} Edad: {}".format(nombre, edad))
```

Funciona, pero es más antiguo.

---

### f-strings (mejor opción)

```python id="fstrings16"
print(f"Nombre: {nombre} Edad: {edad}")
```

Más legible ✔
Más rápido ✔
Más moderno ✔

---

## ⚠️ Errores comunes

❌ Olvidar la `f`:

```python id="fstrings17"
nombre = "Angel"
print("{nombre}")
```

Resultado:

```text id="fstrings18"
{nombre}
```

---

## 📌 ¿Por qué son importantes?

* Son el estándar actual
* Se usan mucho en automatización
* Muy comunes en scripts de ciberseguridad
* Facilitan logs y mensajes dinámicos

---

## 🔗 Conecta con

* [[str]]
* [[Concatenación]]
* [[Conversión de tipos]]
* [[print()]]
* [[Entrada de usuario input()]]

---
