---
title: Elif y else en Python
description: Guía sobre el uso de elif y else en Python para manejar múltiples condiciones y casos por defecto.
tags: [python, condicionales, elif, else, programación]
date: 2026-03-01
---

En Python, además del `if`, se usan **`elif`** y **`else`** para manejar múltiples condiciones y casos por defecto.  
- `elif` → “else if”, se evalúa **solo si las condiciones anteriores fueron falsas**.  
- `else` → se ejecuta **si todas las condiciones anteriores son falsas**.  
Se basan en **expresiones booleanas** [[Expresiones booleanas]] y **operadores de comparación/lógicos**.

## Sintaxis básica
```python id="elifres0"
if condición1:
    # bloque si condición1 es True
elif condición2:
    # bloque si condición1 es False y condición2 es True
else:
    # bloque si todas las anteriores son False
````

## Ejemplo simple

```python id="elifres1"
nota = 85

if nota >= 90:
    print("Sobresaliente")
elif nota >= 70:
    print("Aprobado")
else:
    print("Suspenso")
```

Resultado:

```id="elifres1r"
Aprobado
```

Explicación:

1. `nota >= 90` → False
2. `nota >= 70` → True → se ejecuta este bloque y **salta el else**

## Ejemplo con varias condiciones

```python id="elifres2"
edad = 25

if edad < 13:
    print("Niño")
elif edad < 20:
    print("Adolescente")
elif edad < 65:
    print("Adulto")
else:
    print("Adulto mayor")
```

Resultado:

```id="elifres2r"
Adulto
```

⚡ Python evalúa de **arriba hacia abajo** y **solo ejecuta la primera condición verdadera**.

## Uso con expresiones booleanas

```python id="elifres3"
usuario_valido = True
edad = 17
tiene_permiso = True

if usuario_valido and edad >= 18:
    print("Acceso permitido")
elif usuario_valido and tiene_permiso:
    print("Acceso condicional permitido")
else:
    print("Acceso denegado")
```

Resultado:

```id="elifres3r"
Acceso condicional permitido
```

Explicación paso a paso:

1. `usuario_valido and edad >= 18` → `True and False = False`
2. `usuario_valido and tiene_permiso` → `True and True = True` → se ejecuta este bloque

## Buenas prácticas

1. Siempre termina con `else` si quieres un **caso por defecto**.
2. `elif` permite **simplificar múltiples `if` anidados**, evitando indentaciones profundas.
3. Mantén las **expresiones booleanas claras y legibles** [[Expresiones booleanas]].

## Ejemplo práctico

Asignación de rol según edad:

```python id="elifres4"
edad = 40

if edad < 18:
    rol = "Joven"
elif edad < 30:
    rol = "Adulto joven"
elif edad < 60:
    rol = "Adulto"
else:
    rol = "Adulto mayor"

print(rol)
```

Resultado:

```id="elifres4r"
Adulto
```

## Mini ejercicios

1️⃣ ¿Qué imprime?

```python id="elifres5"
x = 15

if x < 10:
    print("Menor que 10")
elif x < 20:
    print("Menor que 20")
else:
    print("Mayor o igual a 20")
```

Resultado:

```id="elifres5r"
Menor que 20
```

2️⃣ ¿Qué imprime?

```python id="elifres6"
nota = 55

if nota >= 90:
    print("Sobresaliente")
elif nota >= 70:
    print("Aprobado")
else:
    print("Suspenso")
```

Resultado:

```id="elifres6r"
Suspenso
```

## Notas relacionadas

* [[Condicionales if]]
* [[Expresiones booleanas]]
* [[Operadores lógicos]]
* [[Operadores de comparación]]

