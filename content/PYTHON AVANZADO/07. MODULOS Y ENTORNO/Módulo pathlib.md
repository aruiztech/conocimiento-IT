---
title: Módulo pathlib — Manejo de rutas de forma moderna
description: Uso del módulo pathlib en Python para trabajar con rutas y archivos de manera más intuitiva y multiplataforma.
tags: [python, modulos, pathlib, archivos, rutas, automatizacion, analogía, ciberseguridad]
date: 2026-03-02
---

# Módulo pathlib en Python

El módulo `pathlib` permite trabajar con **rutas y archivos** de forma orientada a objetos:

- Rutas multiplataforma
- Crear, mover y eliminar archivos y carpetas
- Inspeccionar propiedades de archivos
- Leer y escribir contenido

> Relacionado con [[Módulo os]], [[Importar módulos]], [[Módulo datetime]], [[Definir funciones]].

---

## 1. Importar el módulo

```python
from pathlib import Path
````

---

## 2. Crear un objeto Path

```python id="pl1a2b"
from pathlib import Path

ruta = Path("carpeta/archivo.txt")
print(ruta)
```

**Salida:**

```python id="pl1r0k"
carpeta/archivo.txt
```

> **Analogía mental:** `Path` es como un **GPS para archivos**, que sabe manejar rutas según el sistema operativo.

---

## 3. Obtener directorio actual

```python id="pl2a3b"
from pathlib import Path

cwd = Path.cwd()
print(cwd)
```

**Salida (ejemplo):**

```python id="pl2r1k"
/home/angel/proyecto
```

> Similar a `os.getcwd()` pero en forma de objeto `Path`.

---

## 4. Verificar existencia de archivos y carpetas

```python id="pl3a4b"
from pathlib import Path

archivo = Path("datos.txt")
print(archivo.exists())
print(archivo.is_file())
print(archivo.is_dir())
```

**Salida (ejemplo):**

```python id="pl3r2k"
True
True
False
```

> **Analogía:** Es como preguntar: "¿Está este archivo realmente en esta carpeta?"

---

## 5. Crear y eliminar directorios

```python id="pl4a5b"
from pathlib import Path

carpeta = Path("nueva_carpeta")
carpeta.mkdir(exist_ok=True)  # Crea la carpeta si no existe
carpeta.rmdir()               # Elimina carpeta vacía
```

> Recomendado usar `exist_ok=True` para evitar errores si la carpeta ya existe.

---

## 6. Listar contenido de una carpeta

```python id="pl5a6b"
from pathlib import Path

for item in Path(".").iterdir():
    print(item)
```

**Salida (ejemplo):**

```python id="pl5r3k"
script.py
datos.txt
nueva_carpeta
```

> **Analogía:** Es como abrir la carpeta y ver cada elemento como un objeto `Path`.

---

## 7. Leer y escribir archivos

```python id="pl6a7b"
from pathlib import Path

archivo = Path("ejemplo.txt")

# Escribir
archivo.write_text("Hola mundo\n")

# Leer
contenido = archivo.read_text()
print(contenido)
```

**Salida:**

```python id="pl6r4k"
Hola mundo
```

> Más seguro y limpio que usar `open()` manualmente.

---

## 8. Combinar rutas — `/` operador

```python id="pl7a8b"
from pathlib import Path

base = Path("/home/angel")
archivo = base / "documentos" / "info.txt"
print(archivo)
```

**Salida:**

```python id="pl7r5k"
/home/angel/documentos/info.txt
```

> **Analogía:** Es como usar un GPS que sabe unir correctamente calles y avenidas (carpetas y archivos) según el país (sistema operativo).

---

## 9. Ejemplo práctico — Log con timestamp

```python id="pl8a9b"
from pathlib import Path
from datetime import datetime

def crear_log():
    logs = Path("logs")
    logs.mkdir(exist_ok=True)
    archivo = logs / f"log_{datetime.now().strftime('%Y%m%d_%H%M%S')}.txt"
    archivo.write_text("Inicio del sistema")
    return archivo

print(crear_log())
```

**Salida (ejemplo):**

```python id="pl8r6k"
logs/log_20260302_191245.txt
```

Conexión: [[Módulo datetime]], [[Definir funciones]], [[Return]].

---

## Buenas prácticas

* Usar objetos `Path` en lugar de cadenas de texto para rutas.
* Evitar concatenar rutas manualmente.
* Usar métodos de `Path` (`exists()`, `mkdir()`, `iterdir()`, etc.) para mayor seguridad.
* Documentar scripts con [[Docstrings]].

---

## Resumen

* `pathlib` moderniza la manipulación de archivos y rutas.
* Compatible multiplataforma, orientado a objetos.
* Simplifica lectura, escritura y gestión de directorios.
* **Analogía final:** `pathlib` es como un **GPS + caja de herramientas** para tus archivos en Python.

Conexión: [[Módulo os]], [[Módulo datetime]], [[Importar módulos]], [[Definir funciones]].

---

