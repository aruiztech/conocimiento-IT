---
title: Tipos de datos en Python
description: Explicación sobre los tipos de datos en Python, incluyendo numéricos, cadenas, booleanos y estructuras básicas.
tags: [Python, tipos de datos, programación]
date: 2026-02-28
---

# Tipos de datos

En Python, un **tipo de dato** indica la clase de valor que almacena una variable.  

Python es **dinámicamente tipado**, por lo que no es necesario declarar el tipo: se asigna automáticamente según el valor.

---

## Tipos numéricos

### int (enteros)

```python
edad = 34
print(edad)
print(type(edad))
````

### Resultado:

```text
34
<class 'int'>
```

---

### float (decimales)

```python
precio = 19.99
print(precio)
print(type(precio))
```

### Resultado:

```text
19.99
<class 'float'>
```

---

### Operaciones numéricas

```python
a = 10
b = 3
print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a // b)  # división entera
print(a % b)   # módulo (resto)
print(a ** b)  # potencia
```

### Resultado:

```text
13
7
30
3.3333333333333335
3
1
1000
```

---

## str (cadenas de texto)

```python
nombre = "Angel"
print(nombre)
print(type(nombre))
```

### Resultado:

```text
Angel
<class 'str'>
```

* Se pueden usar comillas simples `'texto'` o dobles `"texto"`.
* Permiten concatenar con `+` y repetir con `*`.

```python
saludo = "Hola " + nombre
eco = "Eco! " * 3
print(saludo)
print(eco)
```

### Resultado:

```text
Hola Angel
Eco! Eco! Eco! 
```

---

## bool (booleanos)

Solo pueden tomar **True** o **False**.

```python
activo = True
print(activo)
print(type(activo))
```

### Resultado:

```text
True
<class 'bool'>
```

---

## Estructuras de datos básicas

### list (listas)

```python
numeros = [1, 2, 3]
print(numeros)
print(type(numeros))
```

### Resultado:

```text
[1, 2, 3]
<class 'list'>
```

---

### tuple (tuplas)

```python
coordenadas = (10, 20)
print(coordenadas)
print(type(coordenadas))
```

### Resultado:

```text
(10, 20)
<class 'tuple'>
```

---

### dict (diccionarios)

```python
persona = {"nombre": "Angel", "edad": 34}
print(persona)
print(type(persona))
```

### Resultado:

```text
{'nombre': 'Angel', 'edad': 34}
<class 'dict'>
```

---

### set (conjuntos)

```python
numeros = {1, 2, 3}
print(numeros)
print(type(numeros))
```

### Resultado:

```text
{1, 2, 3}
<class 'set'>
```

---

## Tipado dinámico

Una variable puede cambiar de tipo durante la ejecución:

```python
x = 10
print(type(x))

x = "Hola"
print(type(x))
```

### Resultado:

```text
<class 'int'>
<class 'str'>
```

---

## Errores comunes: mezclar tipos

```python
edad = 34
texto = "Edad: " + edad
```

### Resultado:

```text
TypeError: can only concatenate str (not "int") to str
```

Solución: convertir el tipo con `str()`:

```python
edad = 34
texto = "Edad: " + str(edad)
print(texto)
```

### Resultado:

```text
Edad: 34
```

---

## Conecta con

* [[Variables]]
* [[Conversión de tipos]]
* [[Mutabilidad vs inmutabilidad]]
* [[Listas]]
* [[Diccionarios]]

