---
title: "else en bucles Python"
description: "Explicación y ejemplos del uso de else en bucles for y while en Python"
tags: ["Python", "Bucles", "else", "for", "while"]
date: 2026-03-01
---

# else en bucles (for y while)
En Python, los bucles `for` y `while` pueden tener un bloque `else`.  
El `else` se ejecuta **solo si el bucle termina normalmente**, es decir, **sin usar `break`**.  
Esta es una característica poco conocida pero muy poderosa.

Relacionado con:
- [[Bucles for]]
- [[Bucles while]]
- [[break y continue]]

# Sintaxis
## Con for
```python
for elemento in iterable:
    # bloque principal
else:
    # se ejecuta si NO hubo break
````

## Con while

```python
while condición:
    # bloque principal
else:
    # se ejecuta si NO hubo break
```

# Ejemplos

## Ejemplo 1: for sin break

```python
for i in range(3):
    print(i)
else:
    print("Bucle terminado correctamente")
```

Resultado:

```
0
1
2
Bucle terminado correctamente
```

El bucle terminó normalmente → se ejecuta `else`.

## Ejemplo 2: for con break

```python
for i in range(5):
    if i == 3:
        break
    print(i)
else:
    print("Bucle terminado correctamente")
```

Resultado:

```
0
1
2
```

No se ejecuta el `else` porque hubo `break`.

## Ejemplo 3: while sin break

```python
contador = 1

while contador <= 3:
    print(contador)
    contador += 1
else:
    print("While terminado correctamente")
```

Resultado:

```
1
2
3
While terminado correctamente
```

## Ejemplo 4: while con break

```python
contador = 1

while contador <= 5:
    if contador == 4:
        break
    print(contador)
    contador += 1
else:
    print("While terminado correctamente")
```

Resultado:

```
1
2
3
```

No se ejecuta el `else`.

# Casos prácticos

## Buscar un elemento sin éxito

```python
numeros = [10, 20, 30, 40]

for numero in numeros:
    if numero == 50:
        print("Encontrado")
        break
else:
    print("No encontrado")
```

Resultado:

```
No encontrado
```

El `else` actúa como “no se encontró nada”.

## Buscar un elemento con éxito

```python
numeros = [10, 20, 30, 40]

for numero in numeros:
    if numero == 30:
        print("Encontrado")
        break
else:
    print("No encontrado")
```

Resultado:

```
Encontrado
```

No se ejecuta el `else` porque hubo `break`.

# Regla mental clave

> El `else` en bucles significa:
>
> “Se ejecuta si el bucle NO fue interrumpido por `break`”.

# Buenas prácticas

1. Úsalo principalmente en búsquedas.
2. Evita usarlo si puede generar confusión.
3. No lo confundas con el `else` de los [[Condicionales if]].

# Mini ejercicios

1️⃣ ¿Qué imprime?

```python
for i in range(3):
    if i == 5:
        break
else:
    print("Finalizado")
```

Resultado:

```
Finalizado
```

(No hubo `break`)

2️⃣ ¿Qué imprime?

```python
i = 0

while i < 5:
    if i == 3:
        break
    i += 1
else:
    print("Terminado")
```

Resultado:

```
(no imprime nada)
```

# Notas relacionadas

* [[Bucles for]]
* [[Bucles while]]
* [[break y continue]]
* [[range()]]
* [[Expresiones booleanas]]

