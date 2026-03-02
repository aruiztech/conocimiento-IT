---
title: Módulo sys — Interacción con el intérprete de Python
description: Uso del módulo sys en Python para interactuar con el intérprete, manejar argumentos de línea de comandos y rutas de módulos.
tags: [python, modulos, sys, automatizacion, ciberseguridad, analogía]
date: 2026-03-01
---

# Módulo sys en Python

El módulo `sys` permite interactuar directamente con el **intérprete de Python** y su entorno:

- Argumentos de línea de comandos
- Rutas de búsqueda de módulos
- Salida y errores estándar
- Finalizar programas
- Información del intérprete

> Relacionado con [[Importar módulos]], [[Módulo os]], [[Definir funciones]].

---

## 1. Importar el módulo

```python
import sys
````

---

## 2. Argumentos de línea de comandos — `sys.argv`

```python id="sys1a2b"
import sys

print(sys.argv)
```

**Salida (ejemplo al ejecutar `python script.py hola 123`):**

```python id="sys1r0k"
['script.py', 'hola', '123']
```

> **Analogía mental:** Es como recibir los parámetros que alguien te pasa al ejecutar tu script.

Relacionado con [[Definir funciones]] y [[Parámetros y argumentos]].

---

## 3. Salida estándar — `sys.stdout`

```python id="sys2a3b"
import sys

sys.stdout.write("Hola mundo\n")
```

**Salida:**

```
Hola mundo
```

> **Analogía:** Es como imprimir en la pantalla sin usar `print()`, control total sobre la salida.

---

## 4. Error estándar — `sys.stderr`

```python id="sys3a4b"
import sys

sys.stderr.write("¡Error detectado!\n")
```

**Salida (ejemplo):**

```
¡Error detectado!
```

> Útil para logs de errores o scripts profesionales.

---

## 5. Finalizar programa — `sys.exit()`

```python id="sys4a5b"
import sys

if len(sys.argv) < 2:
    sys.exit("Debes pasar al menos un argumento")
```

* Termina el script con mensaje opcional
* Retorna código de error al sistema

> **Analogía:** Es como apagar el script de forma controlada antes de que siga ejecutándose.

---

## 6. Rutas de búsqueda de módulos — `sys.path`

```python id="sys5a6b"
import sys

print(sys.path)
```

**Salida (ejemplo abreviado):**

```python id="sys5r2k"
['/home/angel/proyecto', '/usr/lib/python3.11', ...]
```

* Muestra dónde busca Python los módulos importables.
* Útil para depurar errores de importación.

> Relacionado con [[Importar módulos]] y [[Módulo os]].

---

## 7. Información del intérprete — `sys.version` y `sys.platform`

```python id="sys6a7b"
import sys

print(sys.version)
print(sys.platform)
```

**Salida (ejemplo):**

```
3.11.5 (tags/v3.11.5:abcdef, Mar 15 2026, 10:00:00) [MSC v.1933 64 bit (AMD64)]
linux
```

* Saber la versión de Python y el sistema operativo.
* Fundamental para scripts multiplataforma.

---

## 8. Ejemplo práctico — Script con argumentos

```python id="sys7a8b"
import sys

def main():
    if len(sys.argv) < 3:
        sys.exit("Uso: script.py num1 num2")
    num1 = int(sys.argv[1])
    num2 = int(sys.argv[2])
    print(f"Suma: {num1 + num2}")

if __name__ == "__main__":
    main()
```

**Salida al ejecutar `python script.py 5 7`:**

```
Suma: 12
```

> Conexión: [[Definir funciones]], [[Return]], [[Parámetros y argumentos]].

---

## Buenas prácticas

* Validar siempre `sys.argv`.
* Usar `sys.exit()` para terminar programas correctamente.
* No modificar `sys.path` salvo que sea necesario.
* Documentar scripts con [[Docstrings]].

---

## Resumen

* `sys` permite controlar la ejecución y entorno de Python.
* Maneja argumentos, salida, errores y rutas de módulos.
* Esencial en automatización avanzada, scripts de seguridad y desarrollo profesional.
* **Analogía final:** El módulo `sys` es como tener acceso al **panel de control interno del intérprete de Python**, pudiendo inspeccionar, modificar y gestionar la ejecución del programa.

Conexión: [[Importar módulos]], [[Módulo os]], [[Definir funciones]].

---
