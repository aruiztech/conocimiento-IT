---
title: Función input() en Python
description: Cómo pedir datos al usuario desde la terminal usando la función input() en Python.
tags: [Python, input, entrada de usuario, variables, conversión de tipos]
date: 2026-02-28
---

# Función: input()

La función **`input()`** permite **pedir datos al usuario** desde la terminal.  
Siempre devuelve una **cadena de texto (`str`)**, incluso si el usuario escribe un número.

---

## 🔹 Uso básico

```python
nombre = input("Introduce tu nombre: ")
print("Hola", nombre)
````

### ▶ Ejemplo de ejecución:

```
Introduce tu nombre: Angel
Hola Angel
```

---

## 🔹 Convertir la entrada a otros tipos

Como `input()` devuelve un **str**, a veces necesitamos convertirlo:

```python
edad = int(input("Introduce tu edad: "))
print("Tu edad es:", edad)

altura = float(input("Introduce tu altura en metros: "))
print("Tu altura es:", altura)
```

### ▶ Ejemplo de ejecución:

```
Introduce tu edad: 34
Tu edad es: 34
Introduce tu altura en metros: 1.80
Tu altura es: 1.8
```

⚠️ Si el usuario escribe algo que no se puede convertir, se produce un **ValueError**.

---

## 🔹 Concatenar con f-strings

```python
nombre = input("Nombre: ")
edad = int(input("Edad: "))
print(f"{nombre} tiene {edad} años")
```

### ▶ Ejemplo de ejecución:

```
Nombre: Angel
Edad: 34
Angel tiene 34 años
```

---

## 🔹 Entrada múltiple en una sola línea

```python
x, y = input("Introduce dos números separados por espacio: ").split()
x = int(x)
y = int(y)
print("Suma:", x + y)
```

### ▶ Ejemplo de ejecución:

```
Introduce dos números separados por espacio: 5 7
Suma: 12
```

---

## 🔗 Conecta con

* [[Variables]]
* [[Tipos de datos]]
* [[Conversión de tipos]]
* [[int]]
* [[float]]
* [[str]]

---

## 🧩 Analogía mental

`input()` es como hacer una pregunta y esperar respuesta:

* Tú preguntas: "¿Cuántos años tienes?"
* El usuario responde.
* Guardas esa respuesta en una caja (variable).
* Luego decides qué hacer con esa información.


