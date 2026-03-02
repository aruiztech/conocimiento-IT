---
title: Módulo os — Interacción con el sistema operativo
description: Uso del módulo os en Python para interactuar con el sistema operativo, manejar archivos, directorios y variables de entorno.
tags: [python, modulos, os, sistema_operativo, automatizacion, ciberseguridad, analogía]
date: 2026-03-01
---

# Módulo os en Python

El módulo `os` permite interactuar con el **sistema operativo** desde Python.

Se usa para:

- Trabajar con archivos y directorios
- Obtener rutas
- Leer variables de entorno
- Automatizar tareas del sistema

Muy importante en **automatización y ciberseguridad**.

> Relacionado con [[Importar módulos]], [[Módulo datetime]], [[Definir funciones]].

---

## 1. Importar el módulo

```python
import os
````

---

## 2. Obtener directorio actual — `getcwd()`

```python id="os1a2b"
import os

print(os.getcwd())
```

**Salida (ejemplo):**

```python id="os1r0k"
/home/angel/proyecto
```

> **Analogía mental:** Es como preguntar:
> “¿En qué carpeta estoy ahora mismo?”

---

## 3. Listar archivos — `listdir()`

```python id="os2a3b"
import os

print(os.listdir())
```

**Salida (ejemplo):**

```python id="os2r1k"
['script.py', 'datos.txt', 'carpeta']
```

> **Analogía:** Es como abrir una carpeta y ver todo lo que contiene.

---

## 4. Crear y eliminar carpetas

### Crear directorio

```python id="os3a4b"
import os

os.mkdir("nueva_carpeta")
```

### Eliminar directorio vacío

```python id="os4a5b"
import os

os.rmdir("nueva_carpeta")
```

> ⚠ `rmdir()` solo funciona si la carpeta está vacía.

---

## 5. Crear rutas seguras — `os.path`

```python id="os5a6b"
import os

ruta = os.path.join("carpeta", "archivo.txt")
print(ruta)
```

**Salida (ejemplo en Linux):**

```python id="os5r2k"
carpeta/archivo.txt
```

En Windows podría mostrar:

```
carpeta\archivo.txt
```

> **Analogía:** `os.path.join()` construye rutas correctamente según el sistema, como un GPS que adapta la dirección según el país.

---

## 6. Variables de entorno — `environ`

```python id="os6a7b"
import os

print(os.environ.get("HOME"))
```

**Salida (ejemplo):**

```python id="os6r3k"
/home/angel
```

Las variables de entorno son claves en:

* Configuración
* Seguridad
* Automatización
* Scripts profesionales

---

## 7. Ejecutar comandos del sistema — `system()`

```python id="os7a8b"
import os

os.system("echo Hola mundo")
```

**Salida:**

```
Hola mundo
```

⚠ No recomendado para scripts críticos; usar `subprocess` en proyectos profesionales.

---

## 8. Ejemplo práctico — Crear log con timestamp

```python id="os8a9b"
import os
from datetime import datetime

def crear_log():
    nombre = f"log_{datetime.now().strftime('%Y%m%d_%H%M%S')}.txt"
    with open(nombre, "w") as f:
        f.write("Inicio del sistema")
    return nombre

print(crear_log())
```

**Salida (ejemplo):**

```python id="os8r4k"
log_20260301_185512.txt
```

Relacionado con [[Módulo datetime]], [[Definir funciones]], [[Return]].

---

## Uso en ciberseguridad

El módulo `os` se usa para:

* Enumeración de archivos
* Automatización de scripts
* Recolección de información
* Gestión de rutas en herramientas de pentesting
* Análisis forense básico

---

## Buenas prácticas

* Usar `os.path.join()` en vez de concatenar rutas manualmente.
* Evitar `os.system()` en entornos críticos.
* Validar permisos antes de manipular archivos.
* Documentar scripts con [[Docstrings]].

---

## Resumen

* `os` permite interactuar con el sistema operativo.
* Trabaja con rutas, carpetas, entorno y comandos.
* Es fundamental para automatización y scripting profesional.
* **Analogía final:** El módulo `os` es como tener una **terminal integrada dentro de Python**, que te permite controlar el sistema desde tu código.

Conexión: [[Importar módulos]], [[Módulo datetime]], [[Definir funciones]].

---
