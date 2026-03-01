---
title: Condicionales if
description: Explicación de los condicionales if, if-else e if-elif-else en Python con ejemplos y ejercicios.
tags: [python, condicionales, programación]
date: 2026-03-01
---

Los condicionales permiten **tomar decisiones en tu código** según se cumplan o no ciertas condiciones.  
Se basan en **expresiones booleanas** [[Expresiones booleanas]].

## Sintaxis básica
```python id="ifres0"
if condición:
    # bloque de código si la condición es True
    instrucciones
````

⚠ Python usa **indentación** para delimitar bloques de código.

## Ejemplo simple

```python id="ifres1"
edad = 20

if edad >= 18:
    print("Eres mayor de edad")
```

Resultado:

```id="ifres1r"
Eres mayor de edad
```

## Condicional if-else

Se ejecuta un bloque u otro según la condición sea `True` o `False`.

```python id="ifres2"
edad = 16

if edad >= 18:
    print("Mayor de edad")
else:
    print("Menor de edad")
```

Resultado:

```id="ifres2r"
Menor de edad
```

## Condicional if-elif-else

Para **varias condiciones**, se usa `elif`.

```python id="ifres3"
nota = 85

if nota >= 90:
    print("Sobresaliente")
elif nota >= 70:
    print("Aprobado")
else:
    print("Suspenso")
```

Resultado:

```id="ifres3r"
Aprobado
```

⚡ Python evalúa **de arriba hacia abajo** y ejecuta **solo el primer bloque verdadero**.

## Uso con expresiones booleanas

```python id="ifres4"
usuario_valido = True
edad = 20

if usuario_valido and edad >= 18:
    print("Acceso permitido")
else:
    print("Acceso denegado")
```

Resultado:

```id="ifres4r"
Acceso permitido
```

## Condicional anidado

```python id="ifres5"
edad = 25
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

```id="ifres5r"
Entrada permitida
```

## Buenas prácticas

1. Mantener **indentación consistente** (4 espacios recomendado).
2. Usar **expresiones booleanas claras** [[Expresiones booleanas]].
3. Evitar condicionales demasiado **profundos** (usar funciones si es necesario).

## Ejemplo práctico

Validación de login:

```python id="ifres6"
usuario = "admin"
password = "1234"
activo = True

if usuario == "admin" and password == "1234" and activo:
    print("Bienvenido")
else:
    print("Acceso denegado")
```

Resultado:

```id="ifres6r"
Bienvenido
```

## Mini ejercicios

1️⃣ ¿Qué imprime?

```python id="ifres7"
x = 10
y = 5

if x < y:
    print("x es menor")
else:
    print("x es mayor o igual")
```

Resultado:

```id="ifres7r"
x es mayor o igual
```

2️⃣ ¿Qué imprime?

```python id="ifres8"
edad = 17
tiene_id = False

if edad >= 18 and tiene_id:
    print("Entrada permitida")
else:
    print("Entrada denegada")
```

Resultado:

```id="ifres8r"
Entrada denegada
```

## Notas relacionadas

* [[Expresiones booleanas]]
* [[Operadores lógicos]]
* [[Operadores de comparación]]
* [[Precedencia de operadores]]
