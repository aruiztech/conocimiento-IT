---
title: "range() en Python"
description: "Explicación y ejemplos del uso de range() en Python"
tags: ["Python", "Bucles", "range"]
date: 2026-03-01
---

# range() en Python
`range()` es una función integrada que genera una **secuencia de números enteros**.
Se usa principalmente con [[Bucles for]] para repetir acciones un número determinado de veces.

## Sintaxis
```python
range(stop)
range(start, stop)
range(start, stop, step)
````

### Parámetros

* `start` → Número inicial (incluido)
* `stop` → Número final (**no incluido**)
* `step` → Incremento (o decremento)

## Ejemplo 1: Solo stop

```python
for i in range(5):
    print(i)
```

Resultado:

```id="rangeres1"
0
1
2
3
4
```

Empieza en 0 por defecto y termina antes de 5.

## Ejemplo 2: start y stop

```python
for i in range(2, 6):
    print(i)
```

Resultado:

```id="rangeres2"
2
3
4
5
```

Empieza en 2 y termina antes de 6.

## Ejemplo 3: Con step

```python
for i in range(1, 10, 2):
    print(i)
```

Resultado:

```id="rangeres3"
1
3
5
7
9
```

Avanza de 2 en 2.

## Paso negativo

```python
for i in range(5, 0, -1):
    print(i)
```

Resultado:

```id="rangeres4"
5
4
3
2
1
```

Permite contar hacia atrás.

## Convertir range() en lista

`range()` no devuelve una lista directamente, pero se puede convertir:

```python
numeros = list(range(5))
print(numeros)
```

Resultado:

```id="rangeres5"
[0, 1, 2, 3, 4]
```

## Uso práctico: Tabla de multiplicar

```python
numero = 3

for i in range(1, 11):
    print(numero * i)
```

Resultado:

```id="rangeres6"
3
6
9
12
15
18
21
24
27
30
```

## Uso común con índices

```python
frutas = ["manzana", "banana", "cereza"]

for i in range(len(frutas)):
    print(i, frutas[i])
```

Resultado:

```id="rangeres7"
0 manzana
1 banana
2 cereza
```

Aunque esto funciona, muchas veces es mejor iterar directamente:

```python
for fruta in frutas:
    print(fruta)
```

Relacionado con [[Bucles for]].

## Errores comunes

1. Pensar que el `stop` está incluido (❌ no lo está).
2. Usar `step` negativo sin que `start > stop`.
3. Olvidar convertir a lista si se necesita ver el contenido completo.

## Mini ejercicios

1️⃣ ¿Qué imprime?

```python
for i in range(0, 10, 3):
    print(i)
```

Resultado:

```id="rangeres8"
0
3
6
9
```

2️⃣ ¿Qué imprime?

```python
print(list(range(3, 8)))
```

Resultado:

```id="rangeres9"
[3, 4, 5, 6, 7]
```

# Notas relacionadas

* [[Bucles for]]
* [[break y continue]]
* [[else en bucles]]
* [[List Comprehension]]
* [[Condicionales if]]
