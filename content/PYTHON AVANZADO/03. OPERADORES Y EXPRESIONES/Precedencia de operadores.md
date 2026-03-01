---
title: Precedencia de operadores
description: Guía sobre la precedencia de operadores en Python con ejemplos prácticos y ejercicios.
tags: [python, operadores, programación]
date: 2026-03-01
---

La **precedencia de operadores** determina **el orden en que Python evalúa las expresiones**.  
Si no entendemos esto, podemos obtener resultados inesperados.

## Orden general de precedencia (de mayor a menor)
1. `()` → Paréntesis (siempre se evalúa primero)
2. `**` → Potencia
3. `+x`, `-x`, `~x` → Unarios (positivo, negativo, complemento bit a bit)
4. `*`, `/`, `//`, `%` → Multiplicación, división, módulo
5. `+`, `-` → Suma y resta
6. `<<`, `>>` → Desplazamiento de bits
7. `&` → AND bit a bit
8. `^` → XOR bit a bit
9. `|` → OR bit a bit
10. Comparaciones: `==`, `!=`, `>`, `<`, `>=`, `<=`
11. `not` → Lógico NOT
12. `and` → Lógico AND
13. `or` → Lógico OR
14. `:=` → Asignación (walrus operator)

## Ejemplos con números
```python id="opres1"
x = 2 + 3 * 4
print(x)
````

Resultado:

```id="opres1r"
14
```

Explicación:

* `3 * 4 = 12`
* `2 + 12 = 14`

```python id="opres2"
x = (2 + 3) * 4
print(x)
```

Resultado:

```id="opres2r"
20
```

Paréntesis cambian la prioridad.

```python id="opres3"
x = 2 ** 3 * 4
print(x)
```

Resultado:

```id="opres3r"
32
```

Explicación:

* `2 ** 3 = 8`
* `8 * 4 = 32`

```python id="opres4"
x = -3 ** 2
print(x)
```

Resultado:

```id="opres4r"
-9
```

⚠ Atención: la potencia tiene **mayor precedencia que el negativo**.
Equivalente a: `-(3 ** 2)`

## Comparaciones y lógicos

```python id="opres5"
print(True or False and False)
```

Resultado:

```id="opres5r"
True
```

Evaluación:

* `and` tiene mayor precedencia que `or`
* `False and False = False`
* `True or False = True`

```python id="opres6"
x = 5
y = 10
z = 15

print(x < y and y < z)
```

Resultado:

```id="opres6r"
True
```

Equivalente a:

```python id="opres6b"
print((x < y) and (y < z))
```

## Comparaciones encadenadas

```python id="opres8"
print(1 < 5 < 10)
```

Resultado:

```id="opres8r"
True
```

Python permite **comparaciones encadenadas** como un atajo.

Relacionado con:

* [[Operadores de comparación]]
* [[Operadores lógicos]]

## Ejemplo práctico combinado

```python id="opres9"
edad = 20
ingresos = 3000
usuario_valido = True

print(usuario_valido and edad >= 18 or ingresos > 5000)
```

Resultado:

```id="opres9r"
True
```

Evaluación paso a paso:

1. `usuario_valido and edad >= 18` → `True and True = True`
2. `True or ingresos > 5000` → `True or False = True`

⚠ Sin paréntesis, `and` se evalúa antes que `or`.

## Notas relacionadas

* [[Operadores aritméticos]]
* [[Operadores de comparación]]
* [[Operadores lógicos]]
* [[Expresiones booleanas]]

## Mini ejercicios

1️⃣ ¿Qué devuelve?

```python id="opres10"
print(2 + 3 * 2 ** 2)
```

Resultado:

```id="opres10r"
14
```

Explicación: `2 ** 2 = 4`, `3 * 4 = 12`, `2 + 12 = 14`

2️⃣ ¿Qué devuelve?

```python id="opres11"
print(True or False and not False)
```

Resultado:

```id="opres11r"
True
```

Evaluación:

* `not False = True`
* `False and True = False`
* `True or False = True`

