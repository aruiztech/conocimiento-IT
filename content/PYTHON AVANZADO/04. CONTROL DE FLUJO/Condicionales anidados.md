---
title: Condicionales anidados en Python
description: Guía sobre el uso de condicionales anidados con if, elif y else en Python.
tags: [python, condicionales, if, elif, else, anidado, programación]
date: 2026-03-01
---

Los **condicionales anidados** son `if` (y opcionalmente `elif` y `else`) que se encuentran **dentro de otro condicional**.  
Se usan cuando **una decisión depende de otra**.

## Sintaxis básica
```python id="nestedres0"
if condición1:
    if condición2:
        # bloque si condición1 y condición2 son True
    else:
        # bloque si condición1 es True pero condición2 es False
else:
    # bloque si condición1 es False
````

⚠ Recuerda la **indentación** correcta, Python depende de ella.

## Ejemplo simple

```python id="nestedres1"
edad = 20
tiene_permiso = True

if edad >= 18:
    if tiene_permiso:
        print("Entrada permitida")
    else:
        print("Necesitas permiso")
else:
    print("Menor de edad")
```

Resultado:

```id="nestedres1r"
Entrada permitida
```

Explicación paso a paso:

1. `edad >= 18` → True → entra al primer bloque
2. `tiene_permiso` → True → imprime "Entrada permitida"

## Ejemplo con `elif` anidado

```python id="nestedres2"
nota = 75

if nota >= 90:
    print("Sobresaliente")
elif nota >= 60:
    if nota >= 80:
        print("Muy bien")
    else:
        print("Bien")
else:
    print("Suspenso")
```

Resultado:

```id="nestedres2r"
Bien
```

Explicación:

1. `nota >= 90` → False
2. `nota >= 60` → True → entra al `elif`
3. Dentro del `elif`, `nota >= 80` → False → ejecuta `else` interno → imprime "Bien"

## Uso con expresiones booleanas complejas

```python id="nestedres3"
usuario_valido = True
edad = 17
tiene_permiso = True

if usuario_valido:
    if edad >= 18:
        print("Acceso permitido")
    else:
        if tiene_permiso:
            print("Acceso condicional permitido")
        else:
            print("Acceso denegado")
else:
    print("Usuario inválido")
```

Resultado:

```id="nestedres3r"
Acceso condicional permitido
```

## Buenas prácticas

1. Evita **demasiados niveles de anidamiento**: considera usar funciones para simplificar.
2. Usa **expresiones booleanas claras** [[Expresiones booleanas]].
3. Siempre revisa que **cada `if`, `elif` y `else` tenga un bloque indentado**.

## Ejemplo práctico: Validación de acceso

```python id="nestedres4"
usuario = "admin"
password = "1234"
activo = True
edad = 20

if usuario == "admin" and password == "1234":
    if activo:
        if edad >= 18:
            print("Bienvenido, acceso completo")
        else:
            print("Bienvenido, acceso restringido por edad")
    else:
        print("Cuenta inactiva")
else:
    print("Usuario o contraseña incorrectos")
```

Resultado:

```id="nestedres4r"
Bienvenido, acceso completo
```

## Mini ejercicios

1️⃣ ¿Qué imprime?

```python id="nestedres5"
x = 10
y = 5

if x > 0:
    if y > 0:
        print("Ambos positivos")
    else:
        print("Solo x positivo")
else:
    print("x no es positivo")
```

Resultado:

```id="nestedres5r"
Ambos positivos
```

2️⃣ ¿Qué imprime?

```python id="nestedres6"
edad = 16
tiene_id = False

if edad >= 18:
    if tiene_id:
        print("Entrada permitida")
    else:
        print("Necesitas ID")
else:
    print("Menor de edad")
```

Resultado:

```id="nestedres6r"
Menor de edad
```

## Notas relacionadas

* [[Condicionales if]]
* [[elif y else]]
* [[Expresiones booleanas]]
* [[Operadores lógicos]]
* [[Operadores de comparación]]

