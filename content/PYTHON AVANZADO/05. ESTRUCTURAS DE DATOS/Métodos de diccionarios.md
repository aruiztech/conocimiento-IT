---
title: Métodos de diccionarios — Estructuras de datos en Python
description: Explicación de los métodos más importantes de los diccionarios en Python, con ejemplos, resultados, analogías mentales y enlaces a notas relacionadas.
tags: [python, diccionarios, estructuras, analogía]
date: 2026-03-01
---

# Métodos de diccionarios — Estructuras de datos en Python

Los diccionarios en Python cuentan con **métodos incorporados** que facilitan **consultar, modificar y manipular** los datos de manera eficiente.  

---

## 1. `get()`

```python
usuario = {"nombre": "Ángel", "edad": 34}
print(usuario.get("nombre"))
print(usuario.get("ciudad", "No especificada"))
````

**Salida:**

```python id="gtx3p1"
Ángel
No especificada
```

> **Analogía mental:** Como buscar una ficha en un archivo, pero con la opción de tener un **plan B** si no existe.
> Conecta con [[Acceso a claves]] y [[Crear diccionarios]].

---

## 2. `keys()` y `values()`

```python
usuario = {"nombre": "Ángel", "edad": 34, "ciudad": "Granada"}
print(usuario.keys())
print(usuario.values())
```

**Salida:**

```python id="p9k4xj"
dict_keys(['nombre', 'edad', 'ciudad'])
dict_values(['Ángel', 34, 'Granada'])
```

> **Analogía mental:** `keys()` son los **títulos de fichas**, `values()` son los **contenidos**.
> Relacionado con [[List Comprehension]] para procesar listas de claves o valores.

---

## 3. `items()`

```python
print(usuario.items())
```

**Salida:**

```python id="w2q8ev"
dict_items([('nombre', 'Ángel'), ('edad', 34), ('ciudad', 'Granada')])
```

> **Analogía:** Es como revisar **todas las fichas con sus títulos y contenidos** a la vez.
> Conecta con [[Desempaquetado]] si quieres extraer clave y valor en un bucle:

```python
for clave, valor in usuario.items():
    print(clave, valor)
```

---

## 4. `update()`

```python
usuario.update({"edad": 35, "profesion": "Ingeniero"})
print(usuario)
```

**Salida:**

```python id="h8k1bf"
{'nombre': 'Ángel', 'edad': 35, 'ciudad': 'Granada', 'profesion': 'Ingeniero'}
```

> **Analogía mental:** Como **modificar fichas existentes y agregar nuevas** en tu archivo sin eliminar las anteriores.
> Relacionado con [[Asignación múltiple y desempaquetado]].

---

## 5. `pop()`

```python
edad = usuario.pop("edad")
print(edad)
print(usuario)
```

**Salida:**

```python id="x2f7pz"
35
{'nombre': 'Ángel', 'ciudad': 'Granada', 'profesion': 'Ingeniero'}
```

> **Analogía:** Sacar una ficha del archivo **y guardarla en otra parte**.
> Conecta con [[pop()]] de listas.

---

## 6. `popitem()`

```python
ultimo = usuario.popitem()
print(ultimo)
print(usuario)
```

**Salida:**

```python id="z5v9kc"
('profesion', 'Ingeniero')
{'nombre': 'Ángel', 'ciudad': 'Granada'}
```

> **Analogía:** Quitar la **última ficha añadida** de tu archivo automáticamente.

---

## 7. `clear()`

```python
usuario.clear()
print(usuario)
```

**Salida:**

```python id="y1p3tr"
{}
```

> **Analogía:** Vaciar completamente tu archivo de fichas.

---

## Buenas prácticas

* Usar `get()` para acceder **sin riesgo de error** si la clave no existe.
* `update()` es útil para **modificar varios valores a la vez**.
* `pop()` y `popitem()` ayudan a **extraer elementos** de forma controlada.
* `keys()`, `values()`, `items()` facilitan **iteraciones y List Comprehension** sobre diccionarios.
* Conecta con [[Crear diccionarios]], [[Acceso a claves]] y [[Desempaquetado]].

---

## Resumen

* Los métodos de diccionarios permiten **consultar, modificar y eliminar** elementos de manera eficiente.
* **Analogía final:** Un diccionario es tu **archivo inteligente**, y los métodos son las herramientas para **leer, actualizar o reorganizar las fichas** rápidamente.

---

