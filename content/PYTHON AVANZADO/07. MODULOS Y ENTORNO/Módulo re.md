---
title: Módulo re — Expresiones regulares en Python
description: Uso del módulo re en Python para buscar, validar y manipular texto mediante expresiones regulares.
tags: [python, modulos, re, expresiones_regulares, automatizacion, ciberseguridad, analisis, analogía]
date: 2026-03-02
---

# Módulo re en Python

El módulo `re` permite trabajar con **expresiones regulares**, una herramienta poderosa para:

- Buscar patrones en cadenas
- Validar entradas
- Extraer información
- Reemplazar texto

> Relacionado con [[Importar módulos]], [[Definir funciones]], [[Lectura y escritura]].

---

## 1. Importar el módulo

```python
import re
````

---

## 2. Buscar patrones — `re.search()`

```python id="re1a2b"
import re

texto = "Mi correo es angel@example.com"
resultado = re.search(r"\w+@\w+\.\w+", texto)
print(resultado.group() if resultado else "No encontrado")
```

**Salida:**

```python id="re1r0k"
angel@example.com
```

> **Analogía mental:** Es como un detector de metales que solo suena con patrones específicos (en este caso, correos).

Relacionado con [[Funciones como argumentos]] y [[Definir funciones]].

---

## 3. Encontrar todas las coincidencias — `re.findall()`

```python id="re2a3b"
import re

texto = "Mis números son 123, 456 y 789"
numeros = re.findall(r"\d+", texto)
print(numeros)
```

**Salida:**

```python id="re2r1k"
['123', '456', '789']
```

> **Analogía:** Como recoger todas las monedas de un tipo específico del suelo.

---

## 4. Reemplazar texto — `re.sub()`

```python id="re3a4b"
import re

texto = "La contraseña es 1234"
nuevo_texto = re.sub(r"\d+", "****", texto)
print(nuevo_texto)
```

**Salida:**

```python id="re3r2k"
La contraseña es ****
```

> Útil para enmascarar datos sensibles (ciberseguridad).

---

## 5. Dividir cadenas por patrón — `re.split()`

```python id="re4a5b"
import re

texto = "manzana,pera,naranja;platano"
frutas = re.split(r"[,;]", texto)
print(frutas)
```

**Salida:**

```python id="re4r3k"
['manzana', 'pera', 'naranja', 'platano']
```

> **Analogía:** Como cortar un hilo de lana donde haya comas o puntos y coma.

---

## 6. Compilar expresiones — `re.compile()`

```python id="re5a6b"
import re

patron = re.compile(r"\d+")
texto = "Teléfonos: 555-1234 y 555-5678"
print(patron.findall(texto))
```

**Salida:**

```python id="re5r4k"
['555', '1234', '555', '5678']
```

> **Analogía:** Preparas tu detector de metales para usarlo varias veces sin reescribir el patrón.

---

## 7. Ejemplo práctico — Validación de correo

```python id="re6a7b"
import re

def validar_correo(correo):
    patron = r"^[\w\.-]+@[\w\.-]+\.\w+$"
    return bool(re.match(patron, correo))

print(validar_correo("angel@example.com"))
print(validar_correo("angel@.com"))
```

**Salida:**

```python id="re6r5k"
True
False
```

Conexión: [[Definir funciones]], [[Return]], [[Funciones como argumentos]].

---

## Buenas prácticas

* Usar `r"..."` para cadenas crudas y evitar conflictos con `\`.
* Compilar patrones cuando se usan repetidamente (`re.compile()`).
* Documentar patrones complejos con comentarios.
* Validar entradas de usuario críticas con expresiones regulares.

---

## Resumen

* `re` permite manipular texto y encontrar patrones.
* Fundamental para validaciones, extracción de datos y enmascaramiento.
* **Analogía final:** `re` es como un **detector de metales inteligente para texto**, que encuentra exactamente lo que quieres según el patrón que definas.

Conexión: [[Importar módulos]], [[Definir funciones]], [[Lectura y escritura]].

---

