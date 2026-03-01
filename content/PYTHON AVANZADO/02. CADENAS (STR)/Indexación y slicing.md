---
title: Indexación y slicing en Python
description: Cómo acceder y extraer partes de secuencias en Python usando indexación, slicing y step.
tags: [Python, indexación, slicing, str, list, tuple]
date: 2026-02-28
---

# Indexación y slicing en Python

La **indexación** permite acceder a un elemento específico de una secuencia.  
El **slicing** permite extraer una parte de esa secuencia.

Se aplica a:

- [[str]]
- [[list]]
- [[tuple]]

---

## Analogía mental

Imagina que una cadena es como un **tren de vagones**.  
Cada vagón tiene un número (índice).  

Puedes:
- Tomar un vagón específico → indexación.
- Cortar varios vagones seguidos → slicing.

---

## Indexación

Los índices comienzan en **0**.

```python
texto = "Python"

print(texto[0])
print(texto[3])
````

### Resultado:

```text
P
h
```

Posiciones:

```
P  y  t  h  o  n
0  1  2  3  4  5
```

---

## Índices negativos

Puedes contar desde el final usando números negativos.

```python
texto = "Python"

print(texto[-1])
print(texto[-2])
```

### Resultado:

```text
n
o
```

Posiciones negativas:

```
P  y  t  h  o  n
-6 -5 -4 -3 -2 -1
```

---

## Slicing (rebanado)

Sintaxis:

```python
secuencia[inicio:fin]
```

* Incluye `inicio`
* Excluye `fin`

---

### Ejemplo básico

```python
texto = "Python"

print(texto[0:4])
```

### Resultado:

```text
Pyth
```

---

### Omitir inicio o fin

```python
texto = "Python"

print(texto[:3])
print(texto[3:])
```

### Resultado:

```text
Pyt
hon
```

---

## Paso (step)

Sintaxis completa:

```python
secuencia[inicio:fin:paso]
```

---

### Saltar caracteres

```python
texto = "Python"

print(texto[::2])
```

### Resultado:

```text
Pto
```

---

### Invertir una cadena

```python
texto = "Python"

print(texto[::-1])
```

### Resultado:

```text
nohtyP
```

---

## Importante

Las cadenas son [[Mutabilidad vs inmutabilidad|inmutables]].

No puedes hacer esto:

```python
texto = "Python"
texto[0] = "J"
```

Resultado:

```text
TypeError: 'str' object does not support item assignment
```

---

## Funciona igual con listas

```python
numeros = [10, 20, 30, 40, 50]

print(numeros[1])
print(numeros[1:4])
```

### Resultado:

```text
20
[20, 30, 40]
```

---

## ¿Por qué es importante?

En ciberseguridad y programación en general sirve para:

* Analizar texto
* Extraer datos
* Manipular contraseñas
* Procesar logs
* Limpiar información

---

## Conecta con

* [[str]]
* [[list]]
* [[tuple]]
* [[Mutabilidad vs inmutabilidad]]
* [[Operaciones con cadenas]]

---
