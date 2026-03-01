---
title: "Indexación en listas"
description: "Acceso, modificación y slicing de elementos en listas de Python"
tags: ["Python", "Listas", "Indexación"]
date: 2026-03-01
---

# Indexación en listas

La **indexación** permite acceder a elementos específicos dentro de una lista usando su posición.  
Está directamente relacionada con:

- [[Crear listas]]
- [[Métodos de listas]]
- [[Bucles for]]

# Concepto clave

En Python, los índices:  
✔ Empiezan en **0**  
✔ Pueden ser **negativos**  
✔ Permiten usar rangos (slicing)

# 1. Índices positivos
```python
frutas = ["manzana", "banana", "cereza"]

print(frutas[0])
print(frutas[1])
print(frutas[2])
````

Resultado:

```
manzana
banana
cereza
```

Posiciones reales:

| Índice | Valor   |
| ------ | ------- |
| 0      | manzana |
| 1      | banana  |
| 2      | cereza  |

# 2. Índices negativos

Permiten acceder desde el final.

```python
frutas = ["manzana", "banana", "cereza"]

print(frutas[-1])
print(frutas[-2])
```

Resultado:

```
cereza
banana
```

Posiciones negativas:

| Índice | Valor   |
| ------ | ------- |
| -1     | cereza  |
| -2     | banana  |
| -3     | manzana |

# 3. Modificar usando índice

Las listas son **mutables**, por lo que podemos cambiar valores.

```python
numeros = [10, 20, 30]
numeros[1] = 99

print(numeros)
```

Resultado:

```
[10, 99, 30]
```

# 4. Slicing (rebanado)

Permite obtener una porción de la lista.
Sintaxis:

```python
lista[inicio:fin]
```

⚠ El índice `fin` **no se incluye**.

### Ejemplo básico

```python
numeros = [0, 1, 2, 3, 4, 5]

print(numeros[1:4])
```

Resultado:

```
[1, 2, 3]
```

### Desde el inicio

```python
print(numeros[:3])
```

Resultado:

```
[0, 1, 2]
```

### Hasta el final

```python
print(numeros[3:])
```

Resultado:

```
[3, 4, 5]
```

# 5. Slicing con salto (step)

Sintaxis:

```python
lista[inicio:fin:paso]
```

### Saltando de 2 en 2

```python
numeros = [0, 1, 2, 3, 4, 5]
print(numeros[::2])
```

Resultado:

```
[0, 2, 4]
```

### Invertir una lista

```python
print(numeros[::-1])
```

Resultado:

```
[5, 4, 3, 2, 1, 0]
```

⚡ Muy usado en entrevistas técnicas.

# 6. Errores comunes

### Índice fuera de rango

```python
numeros = [1, 2, 3]
print(numeros[5])
```

Error:

```
IndexError: list index out of range
```

Sucede cuando el índice no existe.

# 7. Indexación en listas anidadas

```python
matriz = [
    [1, 2],
    [3, 4]
]

print(matriz[0][1])
```

Resultado:

```
2
```

Primero accede a la fila, luego a la columna.

# Buenas prácticas

1. Usa índices negativos para acceder rápidamente al último elemento.
2. Usa slicing en lugar de bucles cuando solo necesites una porción.
3. Verifica el tamaño con `len()` antes de acceder por índice si hay riesgo de error.

# Mini ejercicios

1. ¿Qué imprime?

```python
lista = [10, 20, 30, 40]
print(lista[1:3])
```

Resultado:

```
[20, 30]
```

2. ¿Qué imprime?

```python
lista = [1, 2, 3, 4]
print(lista[-2])
```

Resultado:

```
3
```

# Notas relacionadas

* [[Crear listas]]
* [[Métodos de listas]]
* [[List Comprehension]]
* [[Bucles for]]
* [[range()]]
