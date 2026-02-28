---
title: Errores de sintaxis
description: Explicación sobre los errores de sintaxis en Python, ejemplos comunes y cómo interpretarlos.
tags: [Python, errores, sintaxis, depuración]
date: 2026-02-28
---

# Errores de sintaxis

Un **error de sintaxis** ocurre cuando el código no sigue las reglas del lenguaje Python.  

Es como cometer un error gramatical en un idioma: el intérprete no puede entender lo que escribiste.  

Python detecta estos errores **antes de ejecutar el programa**.

---

## Conceptos clave

- Se producen cuando el código está mal escrito.  
- Impiden que el programa se ejecute.  
- Python muestra un mensaje indicando:  
  - El tipo de error  
  - La línea donde ocurrió  
  - Una pista del problema

---

## Ejemplo 1: Falta de dos puntos

```python id="q8x7fu"
if 5 > 3
    print("Cinco es mayor que tres")
````

### Resultado:

```text id="x2h9vm"
SyntaxError: expected ':'
```

Python esperaba `:` al final del `if`.

---

## Ejemplo 2: Paréntesis sin cerrar

```python id="g6p8vw"
print("Hola mundo"
```

### Resultado:

```text id="f7l3dj"
SyntaxError: '(' was never closed
```

---

## Ejemplo 3: Mala indentación

```python id="t4n2pc"
if 5 > 3:
print("Correcto")
```

### Resultado:

```text id="z1v5qh"
IndentationError: expected an indented block
```

Después de un `if`, el bloque debe ir indentado.

---

## Ejemplo 4: Palabra clave mal escrita

```python id="h3k7yb"
pritn("Hola")
```

### Resultado:

```text id="p9r4xt"
NameError: name 'pritn' is not defined
```

⚠️ Esto no es estrictamente un SyntaxError, pero es un error común relacionado con escritura incorrecta.

---

## Cómo leer un error de sintaxis

Cuando aparece un error, observa:

1. Tipo de error (`SyntaxError`, `IndentationError`)
2. Línea del problema
3. Flecha `^` indicando el punto exacto

Ejemplo:

```text id="m2g8qv"
  File "archivo.py", line 2
    if 5 > 3
           ^
SyntaxError: expected ':'
```

---

## Analogía mental

Un error de sintaxis es como escribir:

> "Yo casa ir mañana"

La estructura es incorrecta, por eso no se entiende.

Python necesita que respetes su “gramática”.

---

## Errores más comunes en principiantes

* Olvidar `:` después de `if`, `for`, `while`, `def`.
* No cerrar comillas.
* No cerrar paréntesis.
* Mala indentación.
* Escribir mal funciones (`pritn` en vez de `print`).

---

## Conecta con

* [[Cómo leer errores]]
* [[Indentación en Python]]
* [[Condicionales if]]
* [[Bucles for]]
* [[Funciones]]

