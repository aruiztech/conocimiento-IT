---
title: Expresiones booleanas
description: Guía sobre expresiones booleanas en Python con ejemplos, combinaciones de operadores y mini ejercicios.
tags: [python, boolean, operadores, programación]
date: 2026-03-01
---

Las **expresiones booleanas** son **combinaciones de valores y operadores que devuelven `True` o `False`**.  
Son esenciales en:
- [[Condicionales if]]
- [[Bucles while]]
- [[Validaciones de datos]]
- [[Operadores lógicos]]

## Componentes
1. **Valores booleanos:** `True`, `False`
2. **Operadores de comparación:** `==`, `!=`, `<`, `>`, `<=`, `>=` [[Operadores de comparación]]
3. **Operadores lógicos:** `and`, `or`, `not` [[Operadores lógicos]]
4. **Paréntesis** para controlar precedencia [[Precedencia de operadores]]

## Ejemplos básicos
```python id="boole2"
x = 10
y = 5

print(x > y)
print(x == y)
print(x != y)
````

Resultado:

```id="boole2r"
True
False
True
```

## Combinación con and

```python id="boole4"
edad = 20
tiene_dni = True

print(edad >= 18 and tiene_dni)
```

Resultado:

```id="boole4r"
True
```

⚡ Se cumple si **ambas condiciones son verdaderas**.

## Combinación con or

```python id="boole6"
es_admin = False
es_moderador = True

print(es_admin or es_moderador)
```

Resultado:

```id="boole6r"
True
```

⚡ Se cumple si **al menos una condición es verdadera**.

## Combinación con not

```python id="boole8"
activo = False
print(not activo)
```

Resultado:

```id="boole8r"
True
```

⚡ Invierte el valor lógico.

## Ejemplo completo con varios operadores

```python id="boole10"
edad = 22
ingresos = 2000
usuario_valido = True

print((usuario_valido and edad >= 18) or ingresos > 5000)
```

Resultado:

```id="boole10r"
True
```

Evaluación paso a paso:

1. `usuario_valido and edad >= 18` → `True and True = True`
2. `(True) or ingresos > 5000` → `True or False = True`

## Comparaciones encadenadas

```python id="boole12"
x = 5
print(1 < x < 10)
```

Resultado:

```id="boole12r"
True
```

Python permite **comparaciones encadenadas** como atajo de `1 < x and x < 10`.

## Ejemplo práctico

Validación de acceso a un sistema:

```python id="boole14"
usuario = "admin"
password = "1234"
activo = True

acceso = usuario == "admin" and password == "1234" and activo
print(acceso)
```

Resultado:

```id="boole14r"
True
```

## Tips importantes

1. Usa **paréntesis** para aclarar la intención en expresiones complejas.
2. Recuerda la **precedencia de operadores** [[Precedencia de operadores]]: `not > and > or`
3. Las expresiones booleanas pueden ser **asignadas a variables**:

```python id="boole15"
puede_entrar = edad >= 18 and tiene_dni
```

## Mini ejercicios

1️⃣ ¿Qué devuelve?

```python id="boole17"
print(not (5 > 3) or 2 < 1)
```

Resultado:

```id="boole17r"
False
```

2️⃣ ¿Qué devuelve?

```python id="boole19"
x = 10
y = 5
z = 20
print(x > y and y < z or z < x)
```

Resultado:

```id="boole19r"
True
```

Evaluación paso a paso:

* `x > y and y < z` → `True and True = True`
* `True or z < x` → `True or False = True`

## Notas relacionadas

* [[Operadores de comparación]]
* [[Operadores lógicos]]
* [[Precedencia de operadores]]
* [[Condicionales if]]
* [[Expresiones booleanas en bucles]]
