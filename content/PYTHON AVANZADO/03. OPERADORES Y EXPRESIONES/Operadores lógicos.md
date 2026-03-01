---
title: Operadores lógicos
description: Guía completa sobre operadores lógicos en Python con ejemplos, tabla de verdad y ejercicios.
tags: [python, operadores, programación]
date: 2026-03-01
---

Los **operadores lógicos** permiten combinar expresiones booleanas.  
Trabajan con valores:
- `True`
- `False`

Son fundamentales en:
- [[Condicionales if]]
- [[Expresiones booleanas]]
- [[Bucles while]]
- Validaciones complejas

## Operadores principales

|Operador|Significado|Ejemplo|Resultado|
|---|---|---|---|
|`and`|Y lógico|`True and False`|`False`|
|`or`|O lógico|`True or False`|`True`|
|`not`|Negación|`not True`|`False`|

## Operador and
Devuelve `True` solo si **ambas condiciones son verdaderas**.
```python id="4rtxj8"
print(True and True)
print(True and False)
print(False and False)
````

Resultado:

```id="9hnxkl"
True
False
False
```

### Ejemplo práctico

```python id="k72bgr"
edad = 20
tiene_dni = True

print(edad >= 18 and tiene_dni)
```

Resultado:

```id="cd3l0q"
True
```

## Operador or

Devuelve `True` si **al menos una condición es verdadera**.

```python id="1mfyk9"
print(True or False)
print(False or False)
```

Resultado:

```id="xg92le"
True
False
```

### Ejemplo práctico

```python id="e74b9p"
es_admin = False
es_moderador = True

print(es_admin or es_moderador)
```

Resultado:

```id="f8j2ro"
True
```

## Operador not

Invierte el valor lógico.

```python id="w9l7p5"
print(not True)
print(not False)
```

Resultado:

```id="z0dqsa"
False
True
```

### Ejemplo práctico

```python id="y6b1nc"
activo = False
print(not activo)
```

Resultado:

```id="v2qld7"
True
```

## Tabla de verdad

### and

| A     | B     | Resultado |
| ----- | ----- | --------- |
| True  | True  | True      |
| True  | False | False     |
| False | True  | False     |
| False | False | False     |

### or

| A     | B     | Resultado |
| ----- | ----- | --------- |
| True  | True  | True      |
| True  | False | True      |
| False | True  | True      |
| False | False | False     |

## Evaluación de izquierda a derecha (Short-circuit)

Python usa **evaluación corta**:

* En `and`: si la primera condición es `False`, no evalúa la segunda.
* En `or`: si la primera condición es `True`, no evalúa la segunda.

Ejemplo:

```python id="p3hnk0"
print(False and 10 / 0)
```

Resultado:

```id="d4rkpl"
False
```

No genera error porque no evalúa `10 / 0`.

## Combinación de operadores

```python id="t2n4cr"
edad = 25
ingresos = 2000

print(edad > 18 and ingresos > 1500)
```

Resultado:

```id="h9q7le"
True
```

## Precedencia

Orden de evaluación:

1. `not`
2. `and`
3. `or`

Ejemplo:

```python id="l7m0qj"
print(True or False and False)
```

Resultado:

```id="x2f9wr"
True
```

Porque se evalúa como:

```python id="d3y8nc"
True or (False and False)
```

Relacionado con:

* [[Precedencia de operadores]]

## Ejemplo aplicado a ciberseguridad

Validación de acceso:

```python id="b6j4ra"
usuario = "admin"
password = "1234"

print(usuario == "admin" and password == "1234")
```

Resultado:

```id="m8t0pl"
True
```

## Notas relacionadas

* [[Operadores de comparación]]
* [[Expresiones booleanas]]
* [[Condicionales if]]
* [[Precedencia de operadores]]

## Mini ejercicios

1️⃣ ¿Qué devuelve?

```python id="v9k2pl"
print(not (5 > 3))
```

Resultado:

```id="q4m1cd"
False
```

2️⃣ ¿Qué devuelve?

```python id="t7j9rn"
print((10 > 5) and (3 < 1))
```

Resultado:

```id="f2b6hg"
False
```
