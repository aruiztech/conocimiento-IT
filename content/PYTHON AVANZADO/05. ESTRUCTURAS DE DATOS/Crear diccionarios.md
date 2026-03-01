---
title: Crear diccionarios — Estructuras de datos en Python
description: Explicación de cómo crear diccionarios en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, diccionarios, estructuras, analogía]
date: 2026-03-01
---

# Crear diccionarios — Estructuras de datos en Python

Un **diccionario** es una colección **no ordenada de pares clave-valor**.  
Se usa cuando quieres **asociar un identificador único (clave) a un valor** y acceder rápidamente a él.

---

## Sintaxis básica

```python
usuario = {"nombre": "Ángel", "edad": 34, "ciudad": "Granada"}
print(usuario)
````

**Salida:**

```python id="dxp1v8"
{'nombre': 'Ángel', 'edad': 34, 'ciudad': 'Granada'}
```

> **Analogía mental:** Imagina un **archivo de fichas**: cada clave es el título de la ficha y el valor es el contenido.
> Relacionado con [[Crear tuplas]] y [[Uso de tuplas]] cuando usas tuplas como claves.

---

## Crear diccionarios vacíos y agregar elementos

```python id="s5p9fn"
datos = {}
datos["nombre"] = "Ángel"
datos["edad"] = 34
print(datos)
```

**Salida:**

```python id="h3t8vm"
{'nombre': 'Ángel', 'edad': 34}
```

> **Analogía:** Comenzar con un **archivo vacío** y luego ir agregando fichas según lo necesites.
> Conecta con [[append()]] y [[insert()]] para listas si quieres almacenar varios diccionarios.

---

## Usando la función `dict()`

```python id="ln8bqv"
producto = dict(nombre="Teclado", precio=29.99, stock=100)
print(producto)
```

**Salida:**

```python id="p0v4yx"
{'nombre': 'Teclado', 'precio': 29.99, 'stock': 100}
```

> **Analogía:** Es como rellenar un **formulario** que automáticamente crea el registro completo.
> Relacionado con [[Asignación múltiple y desempaquetado]] para inicializar varios valores a la vez.

---

## Diccionarios con claves inmutables

```python id="bvz2nj"
coordenadas = {(10, 20): "ubicación A", (30, 40): "ubicación B"}
print(coordenadas)
```

**Salida:**

```python id="m9k8fs"
{(10, 20): 'ubicación A', (30, 40): 'ubicación B'}
```

> **Analogía:** Cada tupla funciona como un **código de referencia seguro**, garantizando que la clave no cambie.
> Conecta con [[Tuplas]] y [[Uso de tuplas]].

---

## Resumen de buenas prácticas

* Usar diccionarios para **asociar claves únicas a valores**.
* Las claves deben ser **inmutables**: cadenas, números o tuplas.
* Pueden almacenar **listas, diccionarios o tuplas** como valores.
* Perfecto para **modelar objetos reales**, como usuarios, productos o registros de red (relacionado con [[Sockets]] o [[JSON y APIs REST]] en MOC Python/Redes).

---

## Resumen

* Los diccionarios son **colecciones rápidas y flexibles de pares clave-valor**.
* Permiten un **acceso inmediato** a los datos mediante la clave.
* **Analogía final:** Un diccionario es tu **archivo de fichas inteligentes**: cada ficha tiene un título único (clave) y contenido confiable (valor).
* Conexión: [[Crear listas]], [[Tuplas]] y [[Desempaquetado]] son herramientas complementarias para manipular estructuras complejas de datos.

---

