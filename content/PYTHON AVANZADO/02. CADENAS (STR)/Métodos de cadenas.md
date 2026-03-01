---
title: Métodos de cadenas (str)
description: Métodos principales del tipo str en Python para transformar, analizar y procesar texto.
tags: [Python, str, métodos, cadenas, procesamiento de texto]
date: 2026-02-28
---

# Métodos de cadenas (str)

Los **métodos de cadenas** son funciones integradas que permiten **modificar, analizar o transformar texto**.

Se usan con la sintaxis:

```python
variable.metodo()
````

Recuerda: las cadenas son [[Mutabilidad vs inmutabilidad|inmutables]].
Cada método devuelve **una nueva cadena**, no modifica la original.

---

## Analogía mental

Imagina que una cadena es una hoja impresa.
Los métodos son como filtros digitales: aplican cambios y te entregan una nueva versión, pero la hoja original sigue intacta.

---

## 1. Cambiar mayúsculas y minúsculas

### upper()

```python
texto = "python"
print(texto.upper())
```

Resultado:

```text
PYTHON
```

---

### lower()

```python
texto = "PYTHON"
print(texto.lower())
```

Resultado:

```text
python
```

---

### capitalize()

```python
texto = "python es genial"
print(texto.capitalize())
```

Resultado:

```text
Python es genial
```

---

### title()

```python
texto = "python es genial"
print(texto.title())
```

Resultado:

```text
Python Es Genial
```

---

## 2. Eliminar espacios

### strip()

```python
texto = "   hola   "
print(texto.strip())
```

Resultado:

```text
hola
```

---

### lstrip() y rstrip()

```python
texto = "   hola   "
print(texto.lstrip())
print(texto.rstrip())
```

Resultado:

```text
hola   
   hola
```

---

## 3. Reemplazar texto

### replace()

```python
texto = "Hola mundo"
print(texto.replace("mundo", "Python"))
```

Resultado:

```text
Hola Python
```

---

## 4. Buscar dentro de una cadena

### find()

```python
texto = "Hola mundo"
print(texto.find("mundo"))
```

Resultado:

```text
5
```

Devuelve la posición o `-1` si no lo encuentra.

---

### Operador in

```python
texto = "Hola mundo"
print("mundo" in texto)
```

Resultado:

```text
True
```

---

## 5. Dividir texto

### split()

```python
texto = "uno,dos,tres"
print(texto.split(","))
```

Resultado:

```text
['uno', 'dos', 'tres']
```

Muy usado para procesar datos.

---

## 6. Unir listas en una cadena

### join()

```python
palabras = ["Python", "es", "potente"]
print(" ".join(palabras))
```

Resultado:

```text
Python es potente
```

---

## 7. Verificar contenido

### isdigit()

```python
texto = "1234"
print(texto.isdigit())
```

Resultado:

```text
True
```

---

### isalpha()

```python
texto = "Python"
print(texto.isalpha())
```

Resultado:

```text
True
```

---

### isalnum()

```python
texto = "Python123"
print(texto.isalnum())
```

Resultado:

```text
True
```

---

## ¿Por qué es importante?

En programación y ciberseguridad los métodos de cadenas sirven para:

* Analizar contraseñas
* Limpiar datos
* Procesar logs
* Validar entradas de usuario
* Automatizar tareas

---

## Resumen mental

* Transformar → `upper()`, `lower()`
* Limpiar → `strip()`
* Buscar → `find()`, `in`
* Reemplazar → `replace()`
* Separar → `split()`
* Unir → `join()`

---

## Conecta con

* [[str]]
* [[Indexación y slicing]]
* [[Concatenación]]
* [[Entrada de usuario input()]]
* [[f-strings]]

---