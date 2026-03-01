---
title: Concatenación en Python
description: Cómo unir cadenas en Python usando +, print(), f-strings y el operador *.
tags: [Python, str, cadenas, concatenación, f-strings]
date: 2026-02-28
---

# 🐍 Concatenación en Python

La **concatenación** es el proceso de **unir cadenas de texto** para formar una nueva.  
En Python se puede hacer de varias formas.

---

## 🧠 Analogía mental

Imagina que cada cadena es como una pieza de LEGO 🧱.  
Concatenar es simplemente **encajar piezas** para construir una frase más grande.

---

## 🔹 1️⃣ Concatenación con el operador +

Es la forma más básica.

```python id="concatenacion2"
nombre = "Angel"
saludo = "Hola " + nombre

print(saludo)
````

### ▶ Resultado:

```text id="concatenacion3"
Hola Angel
```

⚠️ Solo funciona si ambos valores son `str`.

---

## ❌ Error común

```python id="concatenacion4"
edad = 34
mensaje = "Tienes " + edad + " años"
```

### ▶ Resultado:

```text id="concatenacion5"
TypeError: can only concatenate str (not "int") to str
```

---

## ✅ Solución: convertir a str()

```python id="concatenacion6"
edad = 34
mensaje = "Tienes " + str(edad) + " años"

print(mensaje)
```

### ▶ Resultado:

```text id="concatenacion7"
Tienes 34 años
```

---

## 🔹 2️⃣ Concatenación con coma en print()

```python id="concatenacion8"
nombre = "Angel"
edad = 34

print("Nombre:", nombre, "Edad:", edad)
```

### ▶ Resultado:

```text id="concatenacion9"
Nombre: Angel Edad: 34
```

Python añade espacios automáticamente.

---

## 🔹 3️⃣ Usando f-strings (RECOMENDADO ⭐)

Forma moderna y más limpia:

```python id="concatenacion10"
nombre = "Angel"
edad = 34

mensaje = f"{nombre} tiene {edad} años"
print(mensaje)
```

### ▶ Resultado:

```text id="concatenacion11"
Angel tiene 34 años
```

✔ Más legible
✔ Más potente
✔ Permite expresiones dentro de `{}`

---

## 🔹 4️⃣ Concatenación con *

Puedes repetir cadenas:

```python id="concatenacion12"
print("Hola " * 3)
```

### ▶ Resultado:

```text id="concatenacion13"
Hola Hola Hola 
```

---

## 📌 Importante

Las cadenas son [[Mutabilidad vs inmutabilidad|inmutables]].
Cada vez que concatenas con `+`, Python crea una nueva cadena en memoria.

---

## 🔗 Conecta con

* [[str]]
* [[Crear cadenas]]
* [[Conversión de tipos]]
* [[f-strings]]
* [[print()]]

---
