---
title: replace()
description: Método replace() del tipo str para reemplazar partes de una cadena en Python.
tags: [Python, str, métodos, reemplazo, cadenas]
date: 2026-02-28
---

# replace()

El método `replace()` permite **reemplazar una parte de una cadena por otra**.  
Pertenece al tipo [[str]].  
📌 Devuelve una nueva cadena (las cadenas son [[Mutabilidad vs inmutabilidad|inmutables]]).

---

## Analogía mental

Imagina que tienes un documento impreso 📄.  
`replace()` es como usar corrector para cambiar una palabra por otra…  
pero Python crea una **copia nueva corregida**.

---

## Sintaxis

```python
cadena.replace(viejo, nuevo)
````

* `viejo` → texto que quieres reemplazar
* `nuevo` → texto que lo sustituye

---

## Ejemplo básico

```python id="p3x9mz"
texto = "Hola mundo"

nuevo = texto.replace("mundo", "Python")

print(nuevo)
```

Resultado:

```text id="q7t2lw"
Hola Python
```

---

## La cadena original no cambia

```python id="v3k8rn"
texto = "Hola mundo"

texto.replace("mundo", "Python")

print(texto)
```

Resultado:

```text id="m1z6px"
Hola mundo
```

Si quieres guardar el cambio:

```python id="t1y9kr"
texto = texto.replace("mundo", "Python")
```

---

## Reemplaza todas las coincidencias

```python id="r2m7kd"
texto = "uno dos uno dos"

print(texto.replace("uno", "XXX"))
```

Resultado:

```text id="x4p8jt"
XXX dos XXX dos
```

---

## Limitar número de reemplazos

```python id="tjgbtq"
texto = "uno dos uno dos"

print(texto.replace("uno", "XXX", 1))
```

Resultado:

```text id="n8t2lz"
XXX dos uno dos
```

El `1` indica máximo un reemplazo.

---

## Sensible a mayúsculas

```python id="n3q7vx"
texto = "Python es potente"

print(texto.replace("python", "Java"))
```

Resultado:

```text id="d6t1kw"
Python es potente
```

No reemplaza porque distingue mayúsculas.
Puedes combinarlo con [[lower()]]:

```python id="b5t4nr"
texto = "Python es potente"

print(texto.lower().replace("python", "java"))
```

---

## Uso práctico

Muy útil para:

* Limpiar texto
* Sustituir caracteres peligrosos
* Normalizar datos
* Procesar logs
* Sanitizar entradas

Ejemplo:

```python id="k2m4pz"
comentario = "Esto es malo!!!"

limpio = comentario.replace("!", "")
print(limpio)
```

Resultado:

```text id="h8p1lx"
Esto es malo
```

---

## Combinado con otros métodos

```python id="y5t2nr"
texto = "  Hola Mundo  "

resultado = texto.strip().lower().replace("mundo", "python")

print(resultado)
```

Resultado:

```text id="k8m4pz"
hola python
```

---

## Resumen mental

* `replace()` sustituye texto.
* Devuelve nueva cadena.
* Reemplaza todas las coincidencias por defecto.
* Puede limitar reemplazos.
* Sensible a mayúsculas.

---

## Conecta con

* [[find()]]
* [[lower()]]
* [[strip()]]
* [[Métodos de cadenas]]
* [[Mutabilidad vs inmutabilidad]]

---