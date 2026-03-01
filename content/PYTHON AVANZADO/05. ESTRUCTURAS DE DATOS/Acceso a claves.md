---
title: Acceso a claves — Diccionarios en Python
description: Cómo acceder a los valores de un diccionario mediante sus claves, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, diccionarios, estructuras, analogía]
date: 2026-03-01
---

# Acceso a claves — Diccionarios en Python

Para acceder a los valores de un diccionario en Python, usamos las **claves**.  
Esto permite recuperar información de manera rápida y confiable.

---

## Acceso directo mediante la clave

```python
usuario = {"nombre": "Ángel", "edad": 34, "ciudad": "Granada"}
print(usuario["nombre"])
print(usuario["edad"])
````

**Salida:**

```python id="v3j4q1"
Ángel
34
```

> **Analogía mental:** Cada clave es como un **título de ficha** en un archivo; usar la clave es abrir directamente la ficha y leer el contenido.
> Relacionado con [[Crear diccionarios]] y [[Uso de tuplas]] (cuando se usan tuplas como claves).

---

## Uso del método `get()`

```python
usuario = {"nombre": "Ángel", "edad": 34}
print(usuario.get("nombre"))
print(usuario.get("ciudad", "No especificada"))
```

**Salida:**

```python id="x9k2bn"
Ángel
No especificada
```

> **Analogía mental:** `get()` es como **abrir una ficha con opción de plan B** si la ficha no existe, evitando errores.
> Conecta con [[Métodos de diccionarios]] y [[Desempaquetado]] si quieres extraer varios valores a la vez.

---

## Verificación de existencia de la clave

```python
if "edad" in usuario:
    print("La edad está registrada")
else:
    print("No hay registro de edad")
```

**Salida:**

```python id="p7f1cs"
La edad está registrada
```

> **Analogía:** Es como **revisar si la ficha existe** antes de abrirla, para no perder tiempo ni causar problemas.
> Relacionado con [[Condicionales if]] del MOC Python/Pre-ASIR.

---

## Acceso a claves en diccionarios anidados

```python
datos = {"persona": {"nombre": "Ángel", "edad": 34}}
print(datos["persona"]["nombre"])
```

**Salida:**

```python id="k2q9dx"
Ángel
```

> **Analogía mental:** Abrir **caja dentro de caja**, accediendo paso a paso a la información sin modificar nada.
> Conecta con [[Tuplas anidadas]] y [[List Comprehension]] si quieres iterar sobre múltiples diccionarios o tuplas anidadas.

---

## Buenas prácticas

* Usar `get()` para **evitar errores de clave inexistente**.
* Verificar la existencia de la clave antes de acceder con condicionales.
* Aprovechar diccionarios **anidados** para representar datos complejos, como JSON de APIs (relacionado con [[JSON y APIs REST]] y [[Sockets]]).

---

## Resumen

* El acceso a claves es **la forma principal de obtener información en un diccionario**.
* Se puede hacer de manera directa (`dict["clave"]`) o segura (`dict.get("clave")`).
* **Analogía final:** Cada diccionario es tu **archivo de fichas inteligentes**, y cada clave es el **título que abre la ficha correcta**.
* Conexión: [[Crear diccionarios]], [[Uso de tuplas]], [[Desempaquetado]] y [[List Comprehension]] permiten trabajar con estructuras más complejas de manera fluida.

---

