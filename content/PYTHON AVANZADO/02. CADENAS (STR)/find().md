---
title: find()
description: Método find() del tipo str para buscar subcadenas en Python y obtener su posición.
tags: [Python, str, métodos, búsqueda, index]
date: 2026-02-28
---

# find()

El método `find()` busca una subcadena dentro de una cadena y devuelve la **posición (índice)** donde aparece por primera vez.  
Pertenece al tipo [[str]].

---

## Analogía mental

Imagina que tu texto es un libro 📖.  
`find()` es como buscar una palabra y que te digan el **número de página exacto** donde aparece por primera vez.

---

## Sintaxis

```python
cadena.find(subcadena)
````

Devuelve:

* 📍 El índice donde empieza la coincidencia.
* ❌ `-1` si no la encuentra.

---

## Ejemplo básico

```python id="p4x9mz"
texto = "Hola mundo"

print(texto.find("mundo"))
```

Resultado:

```text id="q7t2lw"
5
```

---

## Cuando no encuentra nada

```python id="v3k8rn"
texto = "Hola mundo"

print(texto.find("Python"))
```

Resultado:

```text id="m1z6px"
-1
```

---

## Buscar desde una posición específica

```python id="t8q4vs"
texto = "uno dos uno dos"

print(texto.find("uno", 4))
```

Resultado:

```text id="c5n9wy"
8
```

---

## Buscar dentro de un rango

```python id="r2m7kd"
texto = "Python es potente"

print(texto.find("es", 0, 10))
```

Resultado:

```text id="x4p8jt"
7
```

Sintaxis completa:

```python
cadena.find(subcadena, inicio, fin)
```

---

## Diferencia con "in"

```python id="z6v1qh"
texto = "Hola mundo"

print("mundo" in texto)
```

Resultado:

```text id="w9k3mx"
True
```

📌 Diferencia clave:

* `find()` → devuelve posición.
* `in` → devuelve True o False.

---

## Ejemplo práctico

```python id="y5t2nr"
email = "usuario@gmail.com"

if email.find("@") != -1:
    print("Email válido")
```

Resultado:

```text id="k8m4pz"
Email válido
```

---

## Uso en programación y ciberseguridad

Muy útil para:

* Detectar patrones en texto
* Validar emails
* Analizar logs
* Buscar palabras clave
* Filtrar información

---

## Importante

`find()` distingue mayúsculas y minúsculas.

```python id="n3q7vx"
texto = "Python"

print(texto.find("python"))
```

Resultado:

```text id="d6t1kw"
-1
```

Puedes combinarlo con [[lower()]]:

```python id="n8t2lz"
print(texto.lower().find("python"))
```

---

## Resumen mental

* Devuelve índice.
* Devuelve `-1` si no encuentra.
* Sensible a mayúsculas.
* No modifica la cadena.

---

## Conecta con

* [[str]]
* [[Indexación y slicing]]
* [[lower()]]
* [[Métodos de cadenas]]
* [[replace()]]

---
