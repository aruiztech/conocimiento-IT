---
title: Tipo de dato str (Cadenas de texto) en Python
description: Explicación completa del tipo str, creación, operaciones, métodos y validaciones en Python.
tags: [Python, str, cadenas, texto, tipos de datos]
date: 2026-02-28
---

# 🐍 Tipo de dato: str (Cadenas de texto)

En Python, **str** representa **texto**.  
Se usan para almacenar palabras, frases o cualquier secuencia de caracteres.

---

## 🔹 Crear cadenas

```python id="str2"
nombre = "Angel"
saludo = 'Hola Mundo'
frase = "Python es genial"
````

### ▶ Resultado:

```text id="str3"
nombre = "Angel"
saludo = "Hola Mundo"
frase = "Python es genial"
```

---

## 🔤 Operaciones básicas con cadenas

### 🔹 Concatenar (unir) cadenas

```python id="str4"
nombre = "Angel"
mensaje = "Hola " + nombre
print(mensaje)
```

### ▶ Resultado:

```text id="str5"
Hola Angel
```

---

### 🔹 Repetir cadenas

```python id="str6"
eco = "Hola! " * 3
print(eco)
```

### ▶ Resultado:

```text id="str7"
Hola! Hola! Hola! 
```

---

### 🔹 Indexación

```python id="str8"
texto = "Python"
print(texto[0])  # primer carácter
print(texto[-1]) # último carácter
```

### ▶ Resultado:

```text id="str9"
P
n
```

---

### 🔹 Slicing (subcadenas)

```python id="str10"
texto = "Python"
print(texto[0:4])   # caracteres 0 a 3
print(texto[2:])    # desde el índice 2 hasta el final
print(texto[:3])    # desde el inicio hasta el índice 2
```

### ▶ Resultado:

```text id="str11"
Pyth
thon
Pyt
```

---

### 🔹 Métodos útiles de str

```python id="str12"
mensaje = "  Hola Mundo  "

print(mensaje.lower())     # todo minúsculas
print(mensaje.upper())     # todo mayúsculas
print(mensaje.strip())     # elimina espacios al inicio y final
print(mensaje.replace("Mundo", "Python"))  # reemplaza palabra
print(mensaje.split())     # convierte en lista de palabras
```

### ▶ Resultado:

```text id="str13"
  hola mundo  
  HOLA MUNDO  
Hola Mundo
  Hola Python  
['Hola', 'Mundo']
```

---

### 🔹 Validaciones

```python id="str14"
texto = "12345"
print(texto.isdigit())  # True si solo tiene dígitos
print(texto.isalpha())  # True si solo tiene letras
```

### ▶ Resultado:

```text id="str15"
True
False
```

---

## 🔗 Conecta con

* [[Tipos de datos]]
* [[Variables]]
* [[f-strings]]
* [[Indexación y slicing]]
* [[Métodos de cadenas]]

---
