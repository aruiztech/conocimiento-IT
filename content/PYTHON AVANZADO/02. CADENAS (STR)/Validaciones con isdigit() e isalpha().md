---
title: Validaciones con isdigit() e isalpha()
description: Métodos isdigit() e isalpha() del tipo str para validar contenido numérico o alfabético en Python.
tags: [Python, str, métodos, cadenas, bool, validación, input]
date: 2026-02-28
---

# Validaciones con isdigit() e isalpha()

Los métodos `isdigit()` e `isalpha()` permiten validar el contenido de una cadena.

- Pertenecen al tipo [[str]]  
- Devuelven un valor [[bool]] → `True` o `False`  
- Muy útiles cuando trabajas con [[Entrada de usuario input()]]

---

## Analogía mental

Imagina que cada cadena es como un formulario 📝:

- `isdigit()` verifica si solo contiene números  
- `isalpha()` verifica si solo contiene letras  

Es como un guardia que revisa si el contenido cumple las reglas.

---

## 1️⃣ isdigit()

Devuelve `True` si todos los caracteres son dígitos (0–9).

### Sintaxis

```python id="a1d3kx"
cadena.isdigit()
````

### Ejemplo básico

```python id="b4t6pz"
texto = "12345"
print(texto.isdigit())
```

Resultado:

```text id="c5v7mx"
True
```

### Caso negativo

```python id="d6g8nr"
texto = "123a"
print(texto.isdigit())
```

Resultado:

```text id="e7h9px"
False
```

### ⚠️ Importante

No acepta números negativos ni decimales:

```python id="f8j1tr"
print("-123".isdigit())
print("12.3".isdigit())
```

Resultado:

```text id="g9k2ls"
False
False
```

Porque contienen `-` y `.`

---

## 2️⃣ isalpha()

Devuelve `True` si todos los caracteres son letras.

### Sintaxis

```python id="h0l3mn"
cadena.isalpha()
```

### Ejemplo básico

```python id="i1m4pq"
texto = "Python"
print(texto.isalpha())
```

Resultado:

```text id="j2n5rq"
True
```

### Caso negativo

```python id="k3o6sr"
texto = "Python3"
print(texto.isalpha())
```

Resultado:

```text id="l4p7st"
False
```

Porque contiene un número.

### ⚠️ Espacios no permitidos

```python id="m5q8tu"
print("Hola Mundo".isalpha())
```

Resultado:

```text id="n6r9uv"
False
```

El espacio hace que falle.

---

## 🔥 Uso práctico con input()

Validar edad:

```python id="o7s0wx"
edad = input("Introduce tu edad: ")

if edad.isdigit():
    print("Edad válida")
else:
    print("Solo números permitidos")
```

Validar nombre:

```python id="p8t1xy"
nombre = input("Introduce tu nombre: ")

if nombre.isalpha():
    print("Nombre válido")
else:
    print("Solo letras permitidas")
```

---

## 🔁 Métodos relacionados

* `isalnum()` → letras y números
* `isspace()` → solo espacios
* [[lower()]]
* [[strip()]]

---

## 📌 Resumen mental

* `isdigit()` → solo números
* `isalpha()` → solo letras
* Devuelven `True` o `False`
* No aceptan espacios ni símbolos

---

## 🔗 Conecta con

* [[str]]
* [[bool]]
* [[Entrada de usuario input()]]
* [[Métodos de cadenas]]
* [[Conversión de tipos]]

---
