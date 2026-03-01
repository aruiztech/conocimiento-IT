---
title: update() — Métodos de diccionarios en Python
description: Explicación del método update() para modificar o añadir pares clave-valor en un diccionario en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, diccionarios, métodos, analogía]
date: 2026-03-01
---

# update() — Método de diccionarios en Python

El método `update()` permite **añadir o modificar múltiples pares clave-valor** de un diccionario de manera eficiente.  
Si una clave ya existe, su valor se actualiza; si no existe, se añade.

---

## 1. Uso básico de `update()`

```python
usuario = {"nombre": "Ángel", "edad": 34}
usuario.update({"edad": 35, "ciudad": "Granada"})
print(usuario)
````

**Salida:**

```python id="k7v6rp"
{'nombre': 'Ángel', 'edad': 35, 'ciudad': 'Granada'}
```

> **Analogía mental:** Como **revisar fichas en un archivo y actualizar información vieja o añadir nuevas fichas**.
> Relacionado con [[Crear diccionarios]], [[get()]] y [[items()]].

---

## 2. Añadir un solo par

```python id="54b4p3"
usuario.update({"profesion": "Ingeniero"})
print(usuario)
```

**Salida:**

```python id="d9x3jm"
{'nombre': 'Ángel', 'edad': 35, 'ciudad': 'Granada', 'profesion': 'Ingeniero'}
```

> **Analogía:** Añadir **una nueva ficha al archivo** sin tocar las anteriores.
> Conecta con [[Acceso a claves]] y [[Desempaquetado]] si quieres procesar el diccionario después.

---

## 3. Usando argumentos de palabras clave

```python id="nb600v"
usuario.update(telefono="123456789", email="angel@mail.com")
print(usuario)
```

**Salida:**

```python id="p7q9kt"
{'nombre': 'Ángel', 'edad': 35, 'ciudad': 'Granada', 'profesion': 'Ingeniero', 'telefono': '123456789', 'email': 'angel@mail.com'}
```

> **Analogía:** Es como **anotar directamente la información adicional en cada ficha** sin usar un sobre extra.
> Relacionado con [[List Comprehension]] para filtrar o transformar pares actualizados.

---

## Buenas prácticas

* Usar `update()` para **modificaciones múltiples o añadir datos** de manera clara y legible.
* Combinar con `get()` para verificar valores antes de actualizar.
* Muy útil en **procesamiento de JSON o datos externos** (relacionado con [[JSON y APIs REST]]).

---

## Resumen

* `update()` **modifica o añade pares clave-valor** en un diccionario.
* Es más eficiente que asignar uno por uno.
* **Analogía final:** `update()` es tu **lápiz para actualizar fichas antiguas y añadir nuevas fichas** en un archivo.
* Conexión: [[Crear diccionarios]], [[Acceso a claves]], [[get()]], [[items()]] y [[keys()]].

---

