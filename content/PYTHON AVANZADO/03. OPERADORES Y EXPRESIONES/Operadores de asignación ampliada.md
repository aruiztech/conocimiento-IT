---
title: Operadores de asignación ampliada
description: Explicación de operadores de asignación ampliada en Python con ejemplos para números, strings y listas.
tags: [python, operadores, programación]
date: 2026-03-01
---

Los **operadores de asignación ampliada** permiten **modificar una variable usando su valor actual** de forma más compacta.  
Son una combinación de:
```python id="q2v7la"
variable = variable operador valor
````

Forma abreviada:

```python id="p5r3jd"
variable operador= valor
```

## Operadores disponibles

| Operador | Equivalente a | Ejemplo   | Resultado           |
| -------- | ------------- | --------- | ------------------- |
| `+=`     | `x = x + y`   | `x += 3`  | Suma y asigna       |
| `-=`     | `x = x - y`   | `x -= 2`  | Resta y asigna      |
| `*=`     | `x = x * y`   | `x *= 4`  | Multiplica y asigna |
| `/=`     | `x = x / y`   | `x /= 2`  | Divide y asigna     |
| `//=`    | `x = x // y`  | `x //= 2` | División entera     |
| `%=`     | `x = x % y`   | `x %= 3`  | Módulo              |
| `**=`    | `x = x ** y`  | `x **= 2` | Potencia            |

## Ejemplos básicos

```python id="f6k3lp"
x = 10

x += 5
print(x)

x -= 3
print(x)

x *= 2
print(x)

x /= 4
print(x)
```

Resultado:

```id="t9b1cq"
15
12
24
6.0
```

## Ejemplo paso a paso

Forma tradicional:

```python id="r4n2sa"
x = 8
x = x + 2
print(x)
```

Resultado:

```id="g7m3pd"
10
```

Forma abreviada:

```python id="h8l0fq"
x = 8
x += 2
print(x)
```

Resultado:

```id="v1p9rm"
10
```

## Ejemplo con módulo y potencia

```python id="k2c6vs"
x = 10
x %= 3
print(x)

y = 2
y **= 3
print(y)
```

Resultado:

```id="b3n8pt"
1
8
```

## También funcionan con strings

```python id="m9t4la"
texto = "Hola"
texto += " Mundo"
print(texto)
```

Resultado:

```id="d6k1pr"
Hola Mundo
```

## Funcionan con listas

```python id="q4j8nc"
numeros = [1, 2]
numeros += [3, 4]
print(numeros)
```

Resultado:

```id="p5h7gm"
[1, 2, 3, 4]
```

⚠ Con listas, `+=` modifica la lista original (es mutable).

Relacionado con:

* [[Mutabilidad vs inmutabilidad]]
* [[Listas]]

## Diferencia importante con tipos mutables

```python id="y2f3rq"
a = [1, 2]
b = a

a += [3]

print(a)
print(b)
```

Resultado:

```id="s8l9kt"
[1, 2, 3]
[1, 2, 3]
```

Porque ambas variables apuntan al mismo objeto.

## Ejemplo práctico real

Contador de intentos:

```python id="m7p4dq"
intentos = 0

intentos += 1
intentos += 1

print(intentos)
```

Resultado:

```id="f9h2pc"
2
```

Muy usado en:

* Bucles
* Contadores
* Acumuladores
* Scripts de automatización

## Notas relacionadas

* [[Operadores aritméticos]]
* [[Operadores de comparación]]
* [[Operadores lógicos]]
* [[Asignación en Python]]
* [[Mutabilidad vs inmutabilidad]]

## Mini ejercicios

1️⃣ ¿Qué devuelve?

```python id="t3k6jf"
x = 5
x *= 3
print(x)
```

Resultado:

```id="d8p1rq"
15
```

2️⃣ ¿Qué devuelve?

```python id="b4h9vc"
x = 7
x //= 2
print(x)
```

Resultado:

```id="k2l5nm"
3
```

