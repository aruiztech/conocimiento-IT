---
title: Match Case en Python
description: Guía sobre el uso de match case en Python 3.10+ para simplificar condicionales múltiples y patrones.
tags: [python, match, case, condicionales, control de flujo, patrones]
date: 2026-03-01
---

El **`match case`** es una **estructura de control de flujo moderna** que permite **comparar valores** de forma clara, similar a un “switch” en otros lenguajes.  

Se usa para **casos múltiples y patrones complejos**.  
Se basa en **comparación de valores**, **desestructuración** y **expresiones booleanas** [[Expresiones booleanas]].

## Sintaxis básica
```python id="matchres0"
match variable:
    case valor1:
        # bloque si variable == valor1
    case valor2:
        # bloque si variable == valor2
    case _:
        # bloque por defecto (similar a else)
````

⚡ `_` es el **comodín**, se ejecuta si ningún caso coincide.

## Ejemplo simple

```python id="matchres1"
dia = "lunes"

match dia:
    case "lunes":
        print("Inicio de semana")
    case "viernes":
        print("Fin de semana casi")
    case _:
        print("Día normal")
```

Resultado:

```id="matchres1r"
Inicio de semana
```

## Ejemplo con varios casos

```python id="matchres2"
estado = "activo"

match estado:
    case "activo":
        print("Usuario activo")
    case "inactivo":
        print("Usuario inactivo")
    case "pendiente":
        print("Usuario pendiente de verificación")
    case _:
        print("Estado desconocido")
```

Resultado:

```id="matchres2r"
Usuario activo
```

## Uso con múltiples valores en un caso

```python id="matchres3"
nota = 85

match nota:
    case 90 | 100:
        print("Sobresaliente")
    case 70 | 80:
        print("Aprobado")
    case _:
        print("Suspenso")
```

Resultado:

```id="matchres3r"
Suspenso
```

⚡ El operador `|` permite **unir múltiples valores** en un mismo caso.

## Ejemplo con desestructuración de tuplas

```python id="matchres4"
coordenada = (0, 5)

match coordenada:
    case (0, y):
        print(f"Eje Y: {y}")
    case (x, 0):
        print(f"Eje X: {x}")
    case (x, y):
        print(f"Coordenada: {x}, {y}")
```

Resultado:

```id="matchres4r"
Eje Y: 5
```

⚡ Permite **extraer valores directamente del patrón**.

## Ejemplo práctico: menú de opciones

```python id="matchres5"
opcion = 2

match opcion:
    case 1:
        print("Iniciar sesión")
    case 2:
        print("Registrarse")
    case 3:
        print("Salir")
    case _:
        print("Opción inválida")
```

Resultado:

```id="matchres5r"
Registrarse
```

## Buenas prácticas

1. Usar `_` como **caso por defecto**.
2. Aprovechar **desestructuración y patrones** para simplificar condicionales complejas.
3. Evitar condicionales anidados largos si `match case` puede simplificar el flujo.

## Mini ejercicios

1️⃣ ¿Qué imprime?

```python id="matchres6"
color = "azul"

match color:
    case "rojo":
        print("Color rojo")
    case "verde":
        print("Color verde")
    case _:
        print("Otro color")
```

Resultado:

```id="matchres6r"
Otro color
```

2️⃣ ¿Qué imprime?

```python id="matchres7"
coordenada = (3, 0)

match coordenada:
    case (0, y):
        print(f"Eje Y: {y}")
    case (x, 0):
        print(f"Eje X: {x}")
    case (x, y):
        print(f"Coordenada: {x}, {y}")
```

Resultado:

```id="matchres7r"
Eje X: 3
```

## Notas relacionadas

* [[Condicionales if]]
* [[elif y else]]
* [[Condicionales anidados]]
* [[Expresiones booleanas]]
* [[Operadores lógicos]]
* [[Operadores de comparación]]
