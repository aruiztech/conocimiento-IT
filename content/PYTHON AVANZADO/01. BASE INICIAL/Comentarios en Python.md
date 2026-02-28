---
title: Comentarios en Python
description: Explicación sobre cómo usar comentarios en Python, con ejemplos y buenas prácticas.
tags: [Python, comentarios, programación]
date: 2026-02-28
---

# Comentarios en Python

Los **comentarios** son líneas de texto en el código que **Python ignora al ejecutar**.  
Sirven para explicar el código, dejar recordatorios o aclarar conceptos.

---

## Conceptos clave

- Python **ignora** todo lo que está después de un `#` en la línea.  
- Los comentarios **no afectan la ejecución** del programa.  
- Ayudan a que tú o cualquier otra persona **entienda el código** en el futuro.  
- Se pueden usar para **desactivar temporalmente** partes del código.

---

## Ejemplos mínimos funcionales

### Comentario de una línea

```python
# Esto es un comentario
print("Hola Mundo")  # Esto también es un comentario
````

### Comentario de varias líneas

```python
"""
Esto es un comentario
de varias líneas
útil para explicar funciones completas o módulos
"""
print("Hola Mundo")
```

---

## Qué está pasando

* La línea con `#` no se ejecuta.
* La cadena triple `"""` también puede usarse como comentario multilínea (aunque técnicamente es un docstring).

---

## Errores comunes

* Olvidar cerrar las comillas triples en un comentario multilínea.
* Escribir comentarios irrelevantes o confusos.
* Usar comentarios para “esconder” errores en lugar de corregirlos.

---

## Conecta con

* [[¿Qué es Python?]] → Para entender dónde se colocan los comentarios.
* [[Variables]] → Comenta variables complejas para recordar su uso.
* [[Funciones]] → Se recomienda documentar funciones con comentarios o docstrings.

---

## Analogía mental

Un comentario es como una **nota adhesiva en tu código**:

* No afecta el funcionamiento de la computadora.
* Te recuerda a ti o a otros por qué hiciste algo o cómo funciona.
