---
title: args y kwargs — Funciones en Python
description: Explicación de cómo usar *args y **kwargs para recibir múltiples argumentos en funciones Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, args, kwargs, argumentos, analogía]
date: 2026-03-01
---

# *args y **kwargs en funciones Python

- `*args` permite pasar **una cantidad variable de argumentos posicionales** a una función.  
- `**kwargs` permite pasar **una cantidad variable de argumentos con nombre** (diccionario).  

> Relacionado con [[Parámetros y argumentos]], [[Argumentos por defecto]], [[Definir funciones]] y [[Return]].

---

## 1. Uso básico de *args

```python
def sumar(*numeros):
    total = sum(numeros)
    print(f"Suma: {total}")

sumar(1, 2, 3)
sumar(5, 10, 15, 20)
````

**Salida:**

```python id="ak1r0k"
Suma: 6
Suma: 50
```

> **Analogía mental:** `*args` es como **una bolsa donde puedes meter cualquier cantidad de ingredientes** y la función los procesa todos juntos.
> Conecta con [[Parámetros y argumentos]] y [[Argumentos por defecto]].

---

## 2. Uso básico de **kwargs

```python
def mostrar_info(**info):
    for clave, valor in info.items():
        print(f"{clave}: {valor}")

mostrar_info(nombre="Ángel", edad=34)
```

**Salida:**

```python id="ak2r1k"
nombre: Ángel
edad: 34
```

> **Analogía:** `**kwargs` es como **una lista de ingredientes etiquetados**: cada ingrediente tiene su nombre y su cantidad, y la función puede leerlos todos.
> Relacionado con [[Dict Comprehension]] y [[Métodos de diccionarios]].

---

## 3. Combinación de parámetros, *args y **kwargs

```python
def presentacion(titulo, *nombres, **edades):
    print(f"Título: {titulo}")
    print("Nombres:", nombres)
    print("Edades:", edades)

presentacion("Clase Python", "Ángel", "Laura", Ángel=34, Laura=25)
```

**Salida:**

```python id="ak3r2k"
Título: Clase Python
Nombres: ('Ángel', 'Laura')
Edades: {'Ángel': 34, 'Laura': 25}
```

> **Analogía:** La función recibe **ingredientes obligatorios**, luego una **bolsa de ingredientes extra** (`*args`) y finalmente **ingredientes etiquetados** (`**kwargs`) que se pueden usar según se necesite.

---

## Buenas prácticas

* Siempre colocar **parámetros normales primero**, luego `*args`, y finalmente `**kwargs`.
* Útil para funciones **muy flexibles y reutilizables**.
* Evitar conflictos de nombres: no usar `args` o `kwargs` como nombres de variables dentro de la función si ya se usan los argumentos.

---

## Resumen

* `*args` → recibe **cualquier cantidad de argumentos posicionales**.
* `**kwargs` → recibe **cualquier cantidad de argumentos con nombre**.
* **Analogía final:** Es como **tener una receta flexible** que acepta ingredientes normales, adicionales sin etiqueta y otros etiquetados.
* Conexión: [[Parámetros y argumentos]], [[Argumentos por defecto]], [[Definir funciones]], [[Dict Comprehension]], [[Métodos de diccionarios]].

---

