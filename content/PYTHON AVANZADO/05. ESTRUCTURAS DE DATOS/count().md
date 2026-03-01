---
title: count() — Método de listas en Python
description: Explicación completa del método count() en listas de Python con ejemplos y buenas prácticas.
tags: [python, listas, métodos]
date: 2026-03-01
---

# count() — Método de listas en Python

El método `count()` se utiliza para **contar cuántas veces aparece un elemento específico** en una lista.  

Su sintaxis básica es:

```python
lista.count(elemento)
````

* `lista` → cualquier lista de Python.
* `elemento` → valor que deseas contar en la lista.
* Devuelve un **entero** con el número de apariciones.

---

## Ejemplo básico

```python id="3x9v4l"
numeros = [1, 2, 3, 2, 2, 4]
apariciones = numeros.count(2)
print(apariciones)
```

**Salida:**

```python id="5l1s7k"
3
```

> El número `2` aparece **3 veces** en la lista.

---

## Buenas prácticas

* Usar `count()` para **verificar la frecuencia de un elemento** antes de eliminar o procesar datos:

```python id="x2v7qj"
letras = ["a", "b", "c", "a", "b", "a"]
if letras.count("a") > 2:
    print("La letra 'a' aparece más de dos veces")
```

**Salida:**

```python id="f9h3lr"
La letra 'a' aparece más de dos veces
```

---

## Comparación con index()

* [[index()]] → devuelve la posición del **primer elemento** encontrado.
* [[count()]] → devuelve **cuántas veces aparece** el elemento.

---

## Conexiones con otros métodos

* [[append()]] / [[extend()]] / [[insert()]] → agregar elementos antes de contarlos.
* [[remove()]] / [[pop()]] → eliminar elementos y luego verificar frecuencia.
* [[index()]] → encontrar posiciones mientras [[count()]] cuenta ocurrencias.

---

## Resumen

* `count()` devuelve el número de apariciones de un valor en la lista.
* No modifica la lista.
* Útil para análisis de datos y verificación de elementos en listas.
* Complementa [[index()]] y [[remove()]] para trabajar con valores específicos en listas.

---

