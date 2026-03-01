---
title: values() — Métodos de diccionarios en Python
description: Explicación del método values() para obtener los valores de un diccionario en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, diccionarios, métodos, analogía]
date: 2026-03-01
---

# values() — Método de diccionarios en Python

El método `values()` devuelve una **vista de todos los valores** de un diccionario.  
Permite **acceder y recorrer** únicamente los contenidos, sin necesidad de las claves.

---

## 1. Uso básico de `values()`

```python
usuario = {"nombre": "Ángel", "edad": 34, "ciudad": "Granada"}
valores = usuario.values()
print(valores)
````

**Salida:**

```python id="n3v6rp"
dict_values(['Ángel', 34, 'Granada'])
```

> **Analogía mental:** Cada valor es como **el contenido de una ficha en tu archivo**; `values()` te da **todos los contenidos sin los títulos**.
> Relacionado con [[keys()]] y [[Acceso a claves]].

---

## 2. Iterar sobre los valores

```python
for valor in usuario.values():
    print(valor)
```

**Salida:**

```python id="d9w2jm"
Ángel
34
Granada
```

> **Analogía:** Revisar todos los **contenidos de las fichas** uno por uno, sin preocuparte por los títulos.
> Conecta con [[List Comprehension]] para crear listas de valores filtrados o transformados.

---

## 3. Convertir los valores en lista

```python
lista_valores = list(usuario.values())
print(lista_valores)
```

**Salida:**

```python id="p7q8ks"
['Ángel', 34, 'Granada']
```

> **Analogía:** Sacar todos los contenidos y **ponerlos en un cuaderno** para analizarlos o procesarlos fácilmente.
> Relacionado con [[keys()]] y [[items()]] para ver claves o pares completos.

---

## Buenas prácticas

* Usar `values()` cuando necesites **procesar solo los valores** de un diccionario.
* Combinar con List Comprehension o bucles para **filtrar, modificar o transformar datos**.
* Ideal para trabajar con diccionarios anidados o datos de APIs (relacionado con [[JSON y APIs REST]] y [[Sockets]]).

---

## Resumen

* `values()` devuelve **todos los valores de un diccionario** como una vista dinámica.
* Puedes iterar sobre ellos, convertirlos en lista o combinarlos con condicionales.
* **Analogía final:** `values()` te permite **ver todos los contenidos de las fichas** sin abrir los títulos.
* Conexión: [[Crear diccionarios]], [[Acceso a claves]], [[get()]], [[keys()]] y [[items()]].

---
