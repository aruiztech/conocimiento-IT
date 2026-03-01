---
title: keys() — Métodos de diccionarios en Python
description: Explicación del método keys() para obtener las claves de un diccionario en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, diccionarios, métodos, analogía]
date: 2026-03-01
---

# keys() — Método de diccionarios en Python

El método `keys()` devuelve una **vista de todas las claves** de un diccionario.  
Permite **recorrer, inspeccionar o iterar** sobre los títulos de los elementos sin acceder directamente a los valores.

---

## 1. Uso básico de `keys()`

```python
usuario = {"nombre": "Ángel", "edad": 34, "ciudad": "Granada"}
claves = usuario.keys()
print(claves)
````

**Salida:**

```python id="k3v5rp"
dict_keys(['nombre', 'edad', 'ciudad'])
```

> **Analogía mental:** Cada clave es como el **título de una ficha en un archivo**; `keys()` te da **la lista de todos los títulos disponibles**.
> Relacionado con [[Crear diccionarios]] y [[Acceso a claves]].

---

## 2. Iterar sobre las claves

```python
for clave in usuario.keys():
    print(clave)
```

**Salida:**

```python id="f8w2jm"
nombre
edad
ciudad
```

> **Analogía:** Como **recorrer los títulos de fichas uno por uno** para ver qué información tienes disponible.
> Conecta con [[List Comprehension]] para crear listas de claves filtradas o transformadas.

---

## 3. Convertir las claves en lista

```python
lista_claves = list(usuario.keys())
print(lista_claves)
```

**Salida:**

```python id="p9q7ks"
['nombre', 'edad', 'ciudad']
```

> **Analogía:** Sacar los títulos de fichas y **ponerlos en un cuaderno** para trabajar con ellos cómodamente.
> Relacionado con [[values()]] y [[items()]] para ver valores o pares completos.

---

## Buenas prácticas

* Usar `keys()` cuando necesites **iterar o verificar la existencia de claves**.
* Combinar con condicionales y List Comprehension para **filtrar o transformar claves**.
* Ideal para trabajar con diccionarios anidados, JSON o APIs (relacionado con [[JSON y APIs REST]] y [[Sockets]]).

---

## Resumen

* `keys()` devuelve **todas las claves de un diccionario** como una vista dinámica.
* Puedes iterar sobre ellas, convertirlas en lista o combinarlas con condicionales.
* **Analogía final:** `keys()` es tu **índice de fichas** en un archivo; te muestra qué información está disponible sin abrir las fichas.
* Conexión: [[Crear diccionarios]], [[Acceso a claves]], [[get()]], [[values()]] y [[items()]].

---

