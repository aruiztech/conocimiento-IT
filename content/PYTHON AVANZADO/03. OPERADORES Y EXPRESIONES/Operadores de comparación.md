---
title: Operadores de comparación
description: Guía completa sobre operadores de comparación en Python con ejemplos y notas relacionadas.
tags: [python, operadores, programación]
date: 2026-03-01
---

Los **operadores de comparación** se utilizan para comparar valores.  
El resultado siempre es un valor booleano:
- `True`
- `False`

Son fundamentales para:
- [[Condicionales if]]
- [[Expresiones booleanas]]
- [[Bucles while]]
- Validaciones

## Operadores básicos

|Operador|Significado|Ejemplo|Resultado|
|---|---|---|---|
|`==`|Igual a|`5 == 5`|`True`|
|`!=`|Diferente de|`5 != 3`|`True`|
|`>`|Mayor que|`5 > 3`|`True`|
|`<`|Menor que|`5 < 3`|`False`|
|`>=`|Mayor o igual|`5 >= 5`|`True`|
|`<=`|Menor o igual|`5 <= 4`|`False`|

## Ejemplos básicos
```python
print(10 == 10)
print(10 != 5)
print(7 > 3)
print(2 < 1)
print(5 >= 5)
print(4 <= 2)
````

Resultado:

```
True
True
True
False
True
False
```

## Diferencia entre `=` y `==`

* `=` → Asignación
* `==` → Comparación

Error común:

```python
if 5 = 5:
    print("Hola")
```

Resultado:

```
SyntaxError
```

Correcto:

```python
if 5 == 5:
    print("Hola")
```

Resultado:

```
Hola
```

Relacionado con:

* [[Asignación en Python]]
* [[Condicionales if]]

## Comparación con cadenas

```python
print("hola" == "hola")
print("hola" == "Hola")
print("python" != "java")
```

Resultado:

```
True
False
True
```

⚠ Python distingue mayúsculas y minúsculas.

## Comparaciones encadenadas

Python permite comparaciones múltiples:

```python
print(1 < 5 < 10)
print(1 < 5 > 10)
```

Resultado:

```
True
False
```

Es equivalente a:

```python
print(1 < 5 and 5 < 10)
```

Resultado:

```
True
```

Relacionado con:

* [[Operadores lógicos]]

## Comparación entre tipos diferentes

```python
print(5 == 5.0)
```

Resultado:

```
True
```

Pero:

```python
print(5 == "5")
```

Resultado:

```
False
```

Python no convierte automáticamente strings a números.
Relacionado con:

* [[Conversión de tipos]]

## Comparación con listas

```python
print([1, 2] == [1, 2])
print([1, 2] == [2, 1])
```

Resultado:

```
True
False
```

La comparación verifica:

* Orden
* Contenido

## Operador `is` (comparación de identidad)

⚠ No compara valor, sino si es el mismo objeto en memoria.

```python
a = [1, 2]
b = [1, 2]

print(a == b)
print(a is b)
```

Resultado:

```
True
False
```

`==` → compara contenido
`is` → compara identidad

Relacionado con:

* [[Mutabilidad vs inmutabilidad]]

## Ejemplo práctico real

Validación de contraseña:

```python
password = "admin123"

print(password == "admin123")
print(password == "Admin123")
```

Resultado:

```
True
False
```

## Notas relacionadas

* [[Operadores lógicos]]
* [[Expresiones booleanas]]
* [[Condicionales if]]
* [[Mutabilidad vs inmutabilidad]]
* [[Conversión de tipos]]

## Mini ejercicios

1️⃣ ¿Qué devuelve?

```python
print(10 > 5 > 2)
```

Resultado:

```
True
```

2️⃣ ¿Qué devuelve?

```python
print("10" == 10)
```

Resultado:

```
False
```

