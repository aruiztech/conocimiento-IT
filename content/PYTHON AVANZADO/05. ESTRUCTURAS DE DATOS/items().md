---
title: items() — Métodos de diccionarios en Python
description: Explicación del método items() para obtener los pares clave-valor de un diccionario en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, diccionarios, métodos, analogía]
date: 2026-03-01
---

# items() — Método de diccionarios en Python

El método `items()` devuelve una **vista de todos los pares clave-valor** de un diccionario.  
Es útil para **iterar sobre claves y valores a la vez**, sin acceder a ellos por separado.

---

## 1. Uso básico de `items()`

```python
usuario = {"nombre": "Ángel", "edad": 34, "ciudad": "Granada"}
pares = usuario.items()
print(pares)
````

**Salida:**

```python id="j4v6rp"
dict_items([('nombre', 'Ángel'), ('edad', 34), ('ciudad', 'Granada')])
```

> **Analogía mental:** Cada par es como **una ficha completa con título y contenido**; `items()` te muestra **todas las fichas de un vistazo**.
> Relacionado con [[keys()]], [[values()]], [[Acceso a claves]] y [[Desempaquetado]].

---

## 2. Iterar sobre los pares

```python id="54b3p3"
for clave, valor in usuario.items():
    print(f"{clave}: {valor}")
```

**Salida:**

```python id="d9x2jm"
nombre: Ángel
edad: 34
ciudad: Granada
```

> **Analogía:** Recorres cada ficha **leyendo título y contenido juntos**, como inspeccionar un archivo completo.
> Conecta con [[List Comprehension]] y [[Desempaquetado]] para crear listas de pares filtrados o transformados.

---

## 3. Convertir en lista de tuplas

```python id="nb599v"
lista_pares = list(usuario.items())
print(lista_pares)
```

**Salida:**

```python id="p7q8kt"
[('nombre', 'Ángel'), ('edad', 34), ('ciudad', 'Granada')]
```

> **Analogía:** Sacar todas las fichas del archivo y **ponerlas en una lista de tuplas** para procesarlas fácilmente.
> Relacionado con [[Crear tuplas]] y [[Desempaquetado]].

---

## Buenas prácticas

* Usar `items()` cuando necesites **clave y valor simultáneamente**.
* Ideal para bucles, condicionales y List Comprehension.
* Combinar con `get()` o `update()` para modificar valores de forma controlada.
* Útil en procesamiento de datos de APIs, JSON o diccionarios complejos (relacionado con [[JSON y APIs REST]]).

---

## Resumen

* `items()` devuelve **todos los pares clave-valor de un diccionario**.
* Puedes iterar sobre ellos, convertirlos en lista o combinarlos con condicionales.
* **Analogía final:** `items()` es como **abrir todas las fichas de un archivo y ver título y contenido juntos**.
* Conexión: [[Crear diccionarios]], [[Acceso a claves]], [[get()]], [[keys()]], [[values()]] y [[Desempaquetado]].

---

