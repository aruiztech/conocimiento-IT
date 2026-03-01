---
title: startswith() y endswith()
description: Métodos startswith() y endswith() del tipo str para verificar el inicio o final de una cadena en Python.
tags: [Python, str, métodos, cadenas, bool]
date: 2026-02-28
---

# startswith() y endswith()

Los métodos `startswith()` y `endswith()` permiten verificar si una cadena:

- 🔹 Empieza con cierto texto.  
- 🔹 Termina con cierto texto.  

Pertenecen al tipo [[str]].  
Devuelven un valor [[bool]] → `True` o `False`.

---

## Analogía mental

Imagina que una cadena es una carta 📩:

- `startswith()` mira el **remitente** (inicio).  
- `endswith()` mira la **firma final** (final).

---

## 1️⃣ startswith()

### Sintaxis

```python
cadena.startswith(prefijo)
````

Devuelve `True` si la cadena comienza con ese texto.

### Ejemplo básico

```python id="p4k8mz"
texto = "Python es potente"

print(texto.startswith("Python"))
```

Resultado:

```text id="q6t3lw"
True
```

### Caso negativo

```python id="v3k9rn"
print(texto.startswith("python"))
```

Resultado:

```text id="m2z6px"
False
```

📌 Es sensible a mayúsculas.

---

## 2️⃣ endswith()

### Sintaxis

```python
cadena.endswith(sufijo)
```

Devuelve `True` si la cadena termina con ese texto.

### Ejemplo básico

```python id="r2m8kd"
texto = "archivo.pdf"

print(texto.endswith(".pdf"))
```

Resultado:

```text id="x4p9jt"
True
```

Otro ejemplo:

```python id="tjgbtr"
print(texto.endswith(".txt"))
```

Resultado:

```text id="n8t3lz"
False
```

---

## Buscar dentro de un rango

Ambos métodos permiten indicar posición de inicio y fin:

```python id="b5t4nr"
texto = "Python es potente"

print(texto.startswith("es", 7))
```

Resultado:

```text id="k8m4pz"
True
```

Sintaxis completa:

```python
cadena.startswith(texto, inicio, fin)
cadena.endswith(texto, inicio, fin)
```

---

## Uso práctico

Muy usados en:

* Validar extensiones de archivos
* Verificar URLs
* Comprobar prefijos de comandos
* Filtrar datos
* Análisis de logs

Ejemplo práctico:

```python id="y5t2nr"
archivo = "reporte.csv"

if archivo.endswith(".csv"):
    print("Archivo válido")
```

---

## Comparación con otras opciones

En lugar de hacer:

```python
if texto[:6] == "Python":
```

Es mejor:

```python
if texto.startswith("Python"):
```

✔ Más claro
✔ Más legible
✔ Más seguro

---

## Resumen mental

* `startswith()` → ¿empieza con…?
* `endswith()` → ¿termina con…?
* Devuelven `True` o `False`
* Sensibles a mayúsculas
* No modifican la cadena

---

## Conecta con

* [[str]]
* [[bool]]
* [[find()]]
* [[Indexación y slicing]]
* [[Métodos de cadenas]]

---
