---
title: REPL de Python
description: Explicación sobre el REPL de Python, cómo abrirlo, ejemplos básicos y diferencias con scripts.
tags: [Python, REPL, intérprete, interactivo]
date: 2026-02-28
---

# REPL de Python

El **REPL** es el intérprete interactivo de Python.  

REPL significa:

Read → Eval → Print → Loop  
(Leer → Evaluar → Imprimir → Repetir)  

Permite ejecutar código línea por línea sin necesidad de crear un archivo `.py`.

---

## Conceptos clave

- Es ideal para hacer pruebas rápidas.  
- Ejecuta el código inmediatamente.  
- Devuelve el resultado automáticamente.  
- Es muy útil para aprender y experimentar.

---

## Cómo abrir el REPL

Desde la terminal escribe:

```bash
python
````

O en algunos sistemas:

```bash id="j92tcn"
python3
```

Si todo está correcto, verás algo como:

```text
Python 3.12.0
>>>
```

El símbolo `>>>` indica que estás dentro del intérprete.

---

## Ejemplos básicos en el REPL

### Operaciones matemáticas

```python
>>> 2 + 2
4
```

---

### Crear variables

```python
>>> nombre = "Angel"
>>> nombre
'Angel'
```

---

### Usar funciones

```python
>>> print("Hola mundo")
Hola mundo
```

---

### Consultar tipo de dato

```python
>>> edad = 34
>>> type(edad)
<class 'int'>
```

---

## Cómo salir del REPL

Puedes salir usando:

```python
exit()
```

O presionando:

* `Ctrl + Z` y luego Enter (Windows)
* `Ctrl + D` (macOS/Linux)

---

## Diferencia entre REPL y script

| REPL                    | Archivo `.py`           |
| ----------------------- | ----------------------- |
| Ejecuta línea por línea | Ejecuta todo el archivo |
| Ideal para pruebas      | Ideal para proyectos    |
| Resultados inmediatos   | Flujo estructurado      |

---

## Errores comunes

* Intentar pegar bloques grandes con mala indentación.
* Olvidar cerrar paréntesis o comillas.
* Confundir que lo escrito en el REPL no se guarda automáticamente.

---

## Conecta con

* [[Uso de la terminal]]
* [[Cómo ejecutar un archivo .py]]
* [[Variables]]
* [[Tipos de datos]]
* [[Conversión de tipos]]

---

## Analogía mental

El REPL es como una **calculadora avanzada interactiva**:

* Escribes algo.
* Python responde.
* Puedes probar ideas sin riesgo.
* No necesitas crear archivos.

