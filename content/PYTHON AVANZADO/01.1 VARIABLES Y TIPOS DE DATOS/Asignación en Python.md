---
title: Asignación en Python
description: Explicación completa de la asignación de valores a variables, ejemplos básicos, reasignación, asignación múltiple e intercambio de valores.
tags: [Python, Variables, Asignación, Operadores, Buenas prácticas]
date: 2026-02-28
---

# 🐍 Asignación en Python

La **asignación** es el proceso de **guardar un valor en una variable** usando el símbolo `=`.  
Se le llama **operador de asignación** y siempre pone el valor **del lado derecho** dentro de la variable **del lado izquierdo**.

---

## 🧠 Analogía mental

Piensa en la asignación como **poner cosas en cajas**:  

- La **variable** es la caja (por ejemplo, `edad`).  
- El **valor** es lo que guardas dentro de la caja (por ejemplo, `34`).  
- `=` es el gesto de **colocar el objeto dentro de la caja**.  

```text id="asignacion2"
edad = 34
# → "Coloca el número 34 dentro de la caja llamada 'edad'"
````

---

## 🔹 Ejemplos básicos

```python id="asignacion3"
# Números
edad = 34
altura = 1.80

# Texto
nombre = "Angel"
saludo = "Hola Mundo"

# Booleanos
activo = True
```

### ▶ Resultado:

```text id="asignacion4"
edad = 34
altura = 1.8
nombre = "Angel"
saludo = "Hola Mundo"
activo = True
```

---

## 🔹 Reasignación de variables

```python id="asignacion5"
x = 10
print(x)

x = 20   # Cambiamos el valor
print(x)
```

### ▶ Resultado:

```text id="asignacion6"
10
20
```

> Nota: Python **no requiere declarar el tipo** de la variable. Se asigna automáticamente según el valor.

---

## 🔹 Asignación múltiple

Puedes asignar varios valores a varias variables en una sola línea:

```python id="asignacion7"
a, b, c = 1, 2, 3
print(a, b, c)
```

### ▶ Resultado:

```text id="asignacion8"
1 2 3
```

---

## 🔹 Asignación múltiple con el mismo valor

```python id="asignacion9"
x = y = z = 100
print(x, y, z)
```

### ▶ Resultado:

```text id="asignacion10"
100 100 100
```

---

## 🔹 Intercambiar valores entre variables

```python id="asignacion11"
a = 5
b = 10
a, b = b, a
print(a, b)
```

### ▶ Resultado:

```text id="asignacion12"
10 5
```

> Esta es una forma muy **Pythonica** de intercambiar valores sin usar una variable temporal.

---

## 🔗 Conecta con

* [[Variables]]
* [[Tipos de datos]]
* [[Entrada de usuario input()]]
* [[Conversión de tipos]]

---
