---
title: Crear cadenas (str) en Python
description: Cómo crear cadenas en Python, uso de comillas, multilínea, escape, conversión y f-strings.
tags: [Python, str, cadenas, texto, tipos de datos]
date: 2026-02-28
---

# 🐍 Crear cadenas (str)

Una **cadena** (`str`) es una secuencia de caracteres usada para almacenar texto.  
En Python, las cadenas son **inmutables**, lo que significa que no pueden modificarse después de crearse.

---

## 🧠 Analogía mental

Imagina que una cadena es como una **frase impresa en papel**:

- Puedes leerla.  
- Puedes copiarla.  
- Pero si quieres cambiar algo, debes **imprimir una nueva versión**.

---

## 🔹 1️⃣ Crear cadenas con comillas

Puedes usar comillas simples o dobles:

```python id="crear_cadenas2"
nombre = "Angel"
saludo = 'Hola Mundo'

print(nombre)
print(saludo)
````

### ▶ Resultado:

```text id="crear_cadenas3"
Angel
Hola Mundo
```

No hay diferencia funcional entre `' '` y `" "`.

---

## 🔹 2️⃣ Usar comillas dentro de cadenas

Si tu texto contiene comillas, puedes alternar:

```python id="crear_cadenas4"
frase = "Ella dijo 'Hola'"
print(frase)
```

### ▶ Resultado:

```text id="crear_cadenas5"
Ella dijo 'Hola'
```

O escapar las comillas con `\`:

```python id="crear_cadenas6"
frase = "Ella dijo \"Hola\""
print(frase)
```

### ▶ Resultado:

```text id="crear_cadenas7"
Ella dijo "Hola"
```

---

## 🔹 3️⃣ Cadenas multilínea

Usa triple comilla (`'''` o `"""`) para texto en varias líneas:

```python id="crear_cadenas8"
mensaje = """Hola
Esto es
Python"""
print(mensaje)
```

### ▶ Resultado:

```text id="crear_cadenas9"
Hola
Esto es
Python
```

---

## 🔹 4️⃣ Crear cadenas vacías

```python id="crear_cadenas10"
texto = ""
print(texto)
print(type(texto))
```

### ▶ Resultado:

```text id="crear_cadenas11"
<class 'str'>
```

---

## 🔹 5️⃣ Convertir otros tipos a cadena

```python id="crear_cadenas12"
edad = 34
texto = str(edad)
print(texto)
print(type(texto))
```

### ▶ Resultado:

```text id="crear_cadenas13"
34
<class 'str'>
```

---

## 🔹 6️⃣ Cadenas con f-strings (recomendado)

```python id="crear_cadenas14"
nombre = "Angel"
edad = 34

mensaje = f"{nombre} tiene {edad} años"
print(mensaje)
```

### ▶ Resultado:

```text id="crear_cadenas15"
Angel tiene 34 años
```

Las **f-strings** son la forma moderna y más clara de crear cadenas dinámicas.

---

## 🔗 Conecta con

* [[str]]
* [[Tipos de datos]]
* [[Conversión de tipos]]
* [[Entrada de usuario input()]]
* [[f-strings]]

---