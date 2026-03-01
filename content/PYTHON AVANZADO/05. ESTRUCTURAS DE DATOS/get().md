---
title: get() — Métodos de diccionarios en Python
description: Explicación del método get() para acceder a valores en diccionarios de forma segura, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, diccionarios, métodos, analogía]
date: 2026-03-01
---

# get() — Método de diccionarios en Python

El método `get()` permite **acceder al valor asociado a una clave** de un diccionario de manera **segura**, evitando errores si la clave no existe.

---

## 1. Uso básico de `get()`

```python
usuario = {"nombre": "Ángel", "edad": 34}
nombre = usuario.get("nombre")
print(nombre)
````

**Salida:**

```python id="r7h2qv"
Ángel
```

> **Analogía mental:** Es como buscar una ficha en un archivo: si la ficha existe, la abres; si no, simplemente no pasa nada.
> Relacionado con [[Acceso a claves]] y [[Crear diccionarios]].

---

## 2. Valor por defecto

```python
ciudad = usuario.get("ciudad", "No especificada")
print(ciudad)
```

**Salida:**

```python id="t5k8bn"
No especificada
```

> **Analogía:** Buscar la ficha, pero con un **plan B** preparado si no se encuentra la ficha.
> Conecta con [[Métodos de diccionarios]] y [[Desempaquetado]] para manejar valores opcionales.

---

## 3. Uso en condicionales

```python
if usuario.get("edad"):
    print("La edad está registrada")
else:
    print("No hay registro de edad")
```

**Salida:**

```python id="p3f7qd"
La edad está registrada
```

> **Analogía mental:** Como **consultar la ficha antes de abrirla**, asegurando que la información existe.
> Relacionado con [[Condicionales if]] del MOC Python/Pre-ASIR.

---

## 4. Comparación con acceso directo

```python
# Acceso directo
# print(usuario["ciudad"])  # Esto daría KeyError

# Acceso seguro
print(usuario.get("ciudad", "Desconocida"))
```

**Salida:**

```python id="v8n2jr"
Desconocida
```

> **Analogía:** `get()` es tu **red de seguridad**, mientras que el acceso directo es como abrir una ficha sin comprobar si existe, arriesgándote a un error.
> Conecta con [[Acceso a claves]] y [[Métodos de diccionarios]].

---

## Buenas prácticas

* Usar `get()` **para evitar errores de clave inexistente**.
* Combinar con condicionales para manejar valores opcionales.
* Ideal para trabajar con **datos externos**, JSON o APIs (relacionado con [[JSON y APIs REST]]).

---

## Resumen

* `get()` permite **acceder a un valor de diccionario de forma segura**.
* Puedes definir un **valor por defecto** si la clave no existe.
* **Analogía final:** `get()` es tu **plan B al abrir fichas en un archivo**; garantiza que siempre tendrás un resultado, aunque la ficha no exista.
* Conexión: [[Crear diccionarios]], [[Acceso a claves]], [[Desempaquetado]] y [[Métodos de diccionarios]].

---

