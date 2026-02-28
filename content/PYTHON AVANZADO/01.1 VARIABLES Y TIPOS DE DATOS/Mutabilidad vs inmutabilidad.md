---
title: Mutabilidad vs Inmutabilidad en Python
description: Explicación de los objetos mutables e inmutables en Python y cómo afecta a la memoria y variables compartidas.
tags: [Python, Variables, Mutabilidad, Inmutabilidad, Memoria, Listas, Tuplas, Diccionarios]
date: 2026-02-28
---

# 🐍 Mutabilidad vs Inmutabilidad

En Python, los objetos pueden ser:

- 🔁 **Mutables** → Se pueden modificar después de crearse.  
- 🔒 **Inmutables** → No se pueden modificar; cualquier cambio crea un nuevo objeto.  

Entender esto es CLAVE para comprender cómo funciona la memoria en Python.

---

## 🧠 Analogía mental

Imagina dos tipos de objetos:

- 🧱 **Inmutable** → Como una piedra tallada.  
  Si quieres cambiarla, debes romperla y hacer otra nueva.

- 🧩 **Mutable** → Como plastilina.  
  Puedes moldearla sin crear una nueva.

---

# 🔒 Tipos INMUTABLES

- [[int]]  
- [[float]]  
- [[str]]  
- [[bool]]  
- [[None]]  
- [[tuple]]  

---

## 🔹 Ejemplo con int (inmutable)

```python id="mutabilidad_inmutabilidad2"
x = 10
print(id(x))

x = x + 5
print(id(x))
````

### ▶ Resultado:

```text id="mutabilidad_inmutabilidad3"
140421837921456
140421837921616
```

📌 La dirección en memoria cambia. Se creó un nuevo objeto.

---

## 🔹 Ejemplo con str (inmutable)

```python id="mutabilidad_inmutabilidad4"
texto = "Hola"
print(id(texto))

texto = texto + " Mundo"
print(id(texto))
```

### ▶ Resultado:

```text id="mutabilidad_inmutabilidad5"
140421838020848
140421838021168
```

Se creó un nuevo string.

---

# 🔁 Tipos MUTABLES

* [[list]]
* [[dict]]
* [[set]]

---

## 🔹 Ejemplo con list (mutable)

```python id="mutabilidad_inmutabilidad6"
numeros = [1, 2, 3]
print(id(numeros))

numeros.append(4)
print(id(numeros))
```

### ▶ Resultado:

```text id="mutabilidad_inmutabilidad7"
140421838055168
140421838055168
```

📌 La dirección en memoria es la misma. La lista se modificó sin crear una nueva.

---

## ⚠️ Efecto en variables compartidas

```python id="mutabilidad_inmutabilidad8"
a = [1, 2, 3]
b = a

b.append(4)

print(a)
print(b)
```

### ▶ Resultado:

```text id="mutabilidad_inmutabilidad9"
[1, 2, 3, 4]
[1, 2, 3, 4]
```

Ambas variables apuntan al mismo objeto en memoria.

---

## 🔹 Copias y problemas comunes

Para evitar modificar el objeto original:

```python id="mutabilidad_inmutabilidad10"
a = [1, 2, 3]
b = a.copy()

b.append(4)

print(a)
print(b)
```

### ▶ Resultado:

```text id="mutabilidad_inmutabilidad11"
[1, 2, 3]
[1, 2, 3, 4]
```

---

## 🧠 ¿Por qué es importante?

Porque afecta a:

* Funciones
* Paso de argumentos
* Errores difíciles de detectar
* Rendimiento
* Manipulación de datos complejos

---

## 🔗 Conecta con

* [[Variables]]
* [[Asignación en Python]]
* [[Listas]]
* [[Tuplas]]
* [[Funciones]]

---
