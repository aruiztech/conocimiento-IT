---
title: Funciones como argumentos — Python
description: Explicación de cómo pasar funciones como argumentos a otras funciones en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, argumentos, funciones_como_parametros, lambda, analogía]
date: 2026-03-01
---

# Funciones como argumentos en Python

En Python, las funciones son **objetos de primera clase**, lo que significa que se pueden **pasar como argumentos a otras funciones**, asignar a variables o devolver desde otras funciones.

> Relacionado con [[Definir funciones]], [[Funciones lambda]], [[Return]], [[Parámetros y argumentos]], [[List Comprehension]].

---

## 1. Ejemplo básico

```python
def aplicar_funcion(f, valor):
    return f(valor)

def cuadrado(x):
    return x ** 2

resultado = aplicar_funcion(cuadrado, 5)
print(resultado)
````

**Salida:**

```python id="fca1r0k"
25
```

> **Analogía mental:** Es como **darle una receta a un ayudante**, donde el ayudante sigue la receta sobre un ingrediente específico.
> Relacionado con [[Funciones lambda]] para recetas rápidas.

---

## 2. Uso con funciones lambda

```python
resultado = aplicar_funcion(lambda x: x + 10, 7)
print(resultado)
```

**Salida:**

```python id="fca2r1k"
17
```

> **Analogía:** Aquí la receta es **una nota rápida escrita en un papel** (lambda), que el ayudante aplica al ingrediente.

---

## 3. Uso con listas y `map()`

```python
numeros = [1, 2, 3, 4, 5]

def aplicar_a_lista(func, lista):
    return list(map(func, lista))

cuadrados = aplicar_a_lista(lambda x: x**2, numeros)
print(cuadrados)
```

**Salida:**

```python id="fca3r2k"
[1, 4, 9, 16, 25]
```

> **Analogía:** Cada ingrediente de la lista pasa por un **mini ayudante especializado**, que aplica la receta a cada uno.
> Relacionado con [[List Comprehension]] y [[Funciones lambda]].

---

## 4. Buenas prácticas

* Útil para **generalizar operaciones** sobre datos sin duplicar código.
* Combina bien con [[Funciones lambda]] para tareas rápidas.
* Prefiere **nombres claros** para funciones pasadas como argumento.
* Evitar funciones muy complejas como argumentos; mejor usar `def`.

---

## Resumen

* Las funciones pueden **recibir otras funciones como argumentos** y aplicar su lógica.
* Permite **automatizar y generalizar procesos** sin repetir código.
* **Analogía final:** Darle a un ayudante una receta (función) para que la aplique a un ingrediente (dato), ya sea individual o en lista.
* Conexión: [[Definir funciones]], [[Funciones lambda]], [[Return]], [[Parámetros y argumentos]], [[List Comprehension]].

---

