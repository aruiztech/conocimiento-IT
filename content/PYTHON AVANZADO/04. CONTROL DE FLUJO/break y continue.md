---
title: "break y continue en Python"
description: "Explicación y ejemplos del uso de break y continue en bucles Python"
tags: ["Python", "Bucles", "break", "continue"]
date: 2026-03-01
---

# break y continue en Python
`break` y `continue` son instrucciones que permiten **controlar el flujo de los bucles** (`for` y `while`).

Se usan dentro de:
- [[Bucles for]]
- [[Bucles while]]

# break
`break` **detiene completamente el bucle**, aunque la condición siga siendo verdadera.

## Ejemplo con for
```python
for numero in range(1, 6):
    if numero == 4:
        break
    print(numero)
````

Resultado:

```
1
2
3
```

Explicación:

* Cuando `numero == 4`, el bucle se detiene.
* No se imprime el 4 ni el 5.
  Relacionado con [[range()]].

## Ejemplo con while

```python
contador = 1

while True:
    if contador == 4:
        break
    print(contador)
    contador += 1
```

Resultado:

```
1
2
3
```

El bucle es infinito (`while True`), pero `break` lo detiene.

# continue

`continue` **salta la iteración actual** y pasa a la siguiente.
No detiene el bucle.

## Ejemplo con for

```python
for numero in range(1, 6):
    if numero == 3:
        continue
    print(numero)
```

Resultado:

```
1
2
4
5
```

El 3 se omite.

## Ejemplo con while

```python
contador = 0

while contador < 5:
    contador += 1
    if contador == 3:
        continue
    print(contador)
```

Resultado:

```
1
2
4
5
```

# Diferencia clave

| Instrucción | Qué hace                       |
| ----------- | ------------------------------ |
| `break`     | Termina el bucle completamente |
| `continue`  | Salta solo la iteración actual |

# Ejemplo práctico: Buscar elemento

```python
numeros = [10, 20, 30, 40]

for numero in numeros:
    if numero == 30:
        print("Encontrado")
        break
```

Resultado:

```
Encontrado
```

El bucle se detiene al encontrar el valor.

# Ejemplo práctico: Filtrar números pares

```python
for numero in range(1, 8):
    if numero % 2 != 0:
        continue
    print(numero)
```

Resultado:

```
2
4
6
```

Relacionado con [[Operadores aritméticos]].

# Buenas prácticas

1. Usa `break` cuando ya no necesites seguir iterando.
2. Usa `continue` para evitar bloques `if` muy anidados.
3. No abuses de ellos, pueden dificultar la lectura si se usan mal.

# Mini ejercicios

1️⃣ ¿Qué imprime?

```python
for i in range(5):
    if i == 2:
        break
    print(i)
```

Resultado:

```
0
1
```

2️⃣ ¿Qué imprime?

```python
for i in range(5):
    if i % 2 == 0:
        continue
    print(i)
```

Resultado:

```
1
3
```

# Notas relacionadas

* [[Bucles for]]
* [[Bucles while]]
* [[range()]]
* [[else en bucles]]
* [[Expresiones booleanas]]

