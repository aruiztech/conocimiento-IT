---
title: lower()
description: Método lower() del tipo str para convertir texto a minúsculas en Python.
tags: [Python, str, métodos, cadenas]
date: 2026-02-28
---

# lower()

El método `lower()` convierte todos los caracteres de una cadena a **minúsculas**.  
Pertenece al tipo de dato [[str]].

---

## Analogía mental

Imagina que tienes un texto escrito con letras mezcladas:

"PyThOn"

`lower()` es como pulsar un botón que dice:  
"Todo en minúsculas"

---

## Sintaxis

```python
cadena.lower()
````

Devuelve una **nueva cadena** en minúsculas.

Recuerda: las cadenas son [[Mutabilidad vs inmutabilidad|inmutables]].

---

## Ejemplo básico

```python
texto = "PYTHON"
print(texto.lower())
```

Resultado:

```text
python
```

---

## No modifica la original

```python
texto = "PYTHON"

nuevo = texto.lower()

print(texto)
print(nuevo)
```

Resultado:

```text
PYTHON
python
```

La variable original no cambia.

---

## Uso común: comparar texto

Muy útil cuando quieres comparar texto sin importar mayúsculas/minúsculas.

```python
usuario = "Admin"

if usuario.lower() == "admin":
    print("Acceso concedido")
```

Resultado:

```text
Acceso concedido
```

Esto evita errores por diferencias de capitalización.

---

## Con input()

```python
respuesta = input("¿Continuar? (si/no): ")

if respuesta.lower() == "si":
    print("Continuando...")
```

Permite aceptar:
"Si", "SI", "sI", "si"

---

## ¿Por qué es importante?

En programación y ciberseguridad se usa para:

* Normalizar datos
* Validar entradas de usuario
* Procesar logs
* Comparar credenciales
* Evitar errores por mayúsculas

---

## Relación con otros métodos

* [[upper()]]
* [[capitalize()]]
* [[title()]]
* [[Métodos de cadenas]]

---
