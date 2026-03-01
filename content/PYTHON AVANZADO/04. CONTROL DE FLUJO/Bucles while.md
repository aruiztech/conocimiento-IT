---
title: "Bucles while en Python"
description: "Explicación y ejemplos del uso de bucles while en Python"
tags: ["Python", "Bucles", "while"]
date: 2026-03-01
---

# Bucles while en Python
El bucle `while` se utiliza para **repetir un bloque de código mientras una condición sea verdadera (`True`)**.

A diferencia del [[Bucles for]], que itera sobre un iterable, `while` depende de una **condición lógica** basada en [[Expresiones booleanas]].

## Sintaxis básica
```python
while condición:
    # bloque de código
````

El bloque se ejecuta **mientras la condición sea True**.

## Ejemplo básico

```python
contador = 1

while contador <= 5:
    print(contador)
    contador += 1
```

Resultado:

```
1
2
3
4
5
```

Explicación:

* Se evalúa `contador <= 5`
* Se imprime el valor
* Se incrementa `contador`
* Cuando llega a 6, la condición es False y el bucle termina

Relacionado con [[Operadores de comparación]] y [[Operadores de asignación ampliada]].

## Ejemplo con condición lógica

```python
edad = 16

while edad < 18:
    print("Aún no eres mayor de edad")
    edad += 1
```

Resultado:

```
Aún no eres mayor de edad
Aún no eres mayor de edad
```

Se ejecuta mientras `edad < 18`.

## Bucle infinito

Si la condición nunca cambia, el bucle nunca termina:

```python
# NO EJECUTAR
while True:
    print("Esto es infinito")
```

Para evitar esto, normalmente usamos `break`.

## Uso de break

`break` detiene el bucle inmediatamente.

```python
numero = 1

while True:
    if numero == 5:
        break
    print(numero)
    numero += 1
```

Resultado:

```
1
2
3
4
```

Relacionado con [[break y continue]].

## Uso de continue

`continue` salta a la siguiente iteración.

```python
numero = 0

while numero < 5:
    numero += 1
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

El número 3 se omite.

## Ejemplo práctico: Validación de contraseña

```python
password_correcto = "1234"
intento = ""

while intento != password_correcto:
    intento = "1234"  # Simulación
    print("Intentando...")

print("Acceso concedido")
```

Resultado:

```
Intentando...
Acceso concedido
```

Relacionado con [[Expresiones booleanas]].

## while con else

El bloque `else` se ejecuta si el bucle termina **sin usar break**.

```python
contador = 1

while contador <= 3:
    print(contador)
    contador += 1
else:
    print("Bucle terminado correctamente")
```

Resultado:

```
1
2
3
Bucle terminado correctamente
```

Relacionado con [[else en bucles]].

## Mini ejercicios

1️⃣ ¿Qué imprime?

```python
x = 3

while x > 0:
    print(x)
    x -= 1
```

Resultado:

```
3
2
1
```

2️⃣ ¿Qué imprime?

```python
x = 0

while x < 5:
    x += 1
    if x == 4:
        break
    print(x)
```

Resultado:

```
1
2
3
```

# Notas relacionadas

* [[Expresiones booleanas]]
* [[Operadores de comparación]]
* [[Operadores de asignación ampliada]]
* [[break y continue]]
* [[else en bucles]]
* [[Bucles for]]
