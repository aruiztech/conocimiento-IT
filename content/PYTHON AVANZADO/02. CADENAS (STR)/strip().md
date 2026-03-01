---
title: strip()
description: Método strip() del tipo str para eliminar espacios y caracteres al inicio y al final de una cadena en Python.
tags: [Python, str, métodos, cadenas]
date: 2026-02-28
---

# strip()

El método `strip()` elimina los **espacios en blanco al inicio y al final** de una cadena.  
Pertenece al tipo [[str]].  

No modifica la cadena original (las cadenas son [[Mutabilidad vs inmutabilidad|inmutables]]).

---

## Analogía mental

Imagina que tu texto es una hoja con márgenes sucios.  
`strip()` limpia los bordes, pero no toca el contenido del centro.

---

## Sintaxis

```python
cadena.strip()
````

Devuelve una nueva cadena sin espacios al inicio ni al final.

---

## Ejemplo básico

```python id="x8k2pz"
texto = "   Hola mundo   "
print(texto.strip())
```

Resultado:

```text id="q1v7mn"
Hola mundo
```

---

## La original no cambia

```python id="z4r9tw"
texto = "   Python   "

nuevo = texto.strip()

print(texto)
print(nuevo)
```

Resultado:

```text id="b3y6kc"
   Python   
Python
```

---

## Elimina más que espacios

También elimina:

* Saltos de línea `\n`
* Tabulaciones `\t`

```python id="n5t1vs"
texto = "\n\tHola\t\n"
print(texto.strip())
```

Resultado:

```text id="c8m4qx"
Hola
```

---

## Especificar qué caracteres eliminar

Puedes indicar qué caracteres quitar:

```python id="p7w2jd"
texto = "###Python###"
print(texto.strip("#"))
```

Resultado:

```text id="r6k9hb"
Python
```

Elimina esos caracteres solo del inicio y final, no del centro.

---

## Variantes

### lstrip() → izquierda

```python id="u3f8ly"
texto = "   Hola"
print(texto.lstrip())
```

Resultado:

```text id="e2v5zn"
Hola
```

---

### rstrip() → derecha

```python id="k9d4qs"
texto = "Hola   "
print(texto.rstrip())
```

Resultado:

```text id="w1m7tx"
Hola
```

---

## Uso práctico

Muy útil cuando trabajas con:

* [[Entrada de usuario input()]]
* Lectura de archivos
* Procesamiento de logs
* Validación de datos

Ejemplo típico:

```python id="t6p3va"
usuario = input("Usuario: ").strip()

if usuario == "admin":
    print("Acceso permitido")
```

Evita errores por espacios invisibles.

---

## Resumen mental

* `strip()` → limpia ambos lados
* `lstrip()` → limpia izquierda
* `rstrip()` → limpia derecha
* Devuelve nueva cadena
* No modifica la original

---

## Conecta con

* [[str]]
* [[Métodos de cadenas]]
* [[split()]]
* [[lower()]]
* [[Entrada de usuario input()]]

---