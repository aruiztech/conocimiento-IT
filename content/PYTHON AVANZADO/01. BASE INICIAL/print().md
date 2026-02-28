---
title: print() en Python
description: Explicación de la función `print()` en Python, sintaxis, ejemplos y buenas prácticas.
tags: [Python, print, funciones, depuración]
date: 2026-02-28
---

# print() en Python

`print()` es la función que permite **mostrar información en pantalla**.  
Es una de las funciones más usadas cuando estás aprendiendo Python.

---

## Analogía mental

Imagina que `print()` es como un **megáfono**:  
Todo lo que pongas dentro de los paréntesis será anunciado en la consola.

---

## Sintaxis básica

```python id="b7q2hv"
print("Hola mundo")
````

### Resultado:

```text id="c9k4lp"
Hola mundo
```

---

## Imprimir variables

```python id="d8r3tx"
nombre = "Angel"
print(nombre)
```

### Resultado:

```text id="e2v7sw"
Angel
```

---

## Imprimir múltiples valores

Puedes separar valores con comas:

```python id="f3y6ju"
nombre = "Angel"
edad = 34

print("Nombre:", nombre, "Edad:", edad)
```

### Resultado:

```text id="g1n9zr"
Nombre: Angel Edad: 34
```

Python añade espacios automáticamente entre los argumentos.

---

## Personalizar el separador (`sep`)

Por defecto, `print()` separa con un espacio.
Puedes cambiarlo con `sep=`:

```python id="h2t4qi"
print("2026", "02", "23", sep="-")
```

### Resultado:

```text id="i7k5ow"
2026-02-23
```

---

## Evitar salto de línea (`end`)

Por defecto, `print()` añade un salto de línea al final.
Puedes modificarlo con `end=`:

```python id="j3m1pc"
print("Hola", end=" ")
print("Mundo")
```

### Resultado:

```text id="k6b8lv"
Hola Mundo
```

---

## Usar print con f-strings

```python id="l4q2zd"
nombre = "Angel"
edad = 34

print(f"{nombre} tiene {edad} años")
```

### Resultado:

```text id="m9t7vw"
Angel tiene 34 años
```

---

## Imprimir tipos de datos

```python id="n3y6js"
numero = 10
print(type(numero))
```

### Resultado:

```text id="o1r4kp"
<class 'int'>
```

---

## Usos importantes de print()

* Depurar código
* Verificar valores de variables
* Mostrar resultados al usuario
* Crear mensajes en scripts
* Generar logs básicos

---

## Errores comunes

Olvidar paréntesis:

```python id="p7v9dr"
print "Hola"
```

Resultado:

```text id="q3t5lf"
SyntaxError
```

> En Python 3, `print` siempre necesita paréntesis.

---

## Resumen mental

* `print()` = mostrar información
* `sep=` = cómo separar
* `end=` = cómo terminar

---

## Conecta con

* [[Variables]]
* [[f-strings]]
* [[Entrada de usuario input()]]
* [[type()]]
* [[Estructura básica de un script]]

