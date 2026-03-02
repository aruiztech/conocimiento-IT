---
title: Módulo csv — Trabajar con archivos CSV en Python
description: Uso del módulo csv en Python para leer, escribir y manipular datos en archivos CSV de manera eficiente y segura.
tags: [python, modulos, csv, datos, archivos, automatizacion, ciberseguridad, analogía]
date: 2026-03-02
---

# Módulo csv en Python

El módulo `csv` permite trabajar con archivos **CSV (Comma Separated Values)**, ampliamente usados para:

- Exportar e importar datos tabulares
- Analizar información de hojas de cálculo
- Intercambio de datos entre sistemas
- Preparación de datasets para proyectos

> Relacionado con [[Importar módulos]], [[Módulo json]], [[Módulo pathlib]], [[Lectura y escritura]].

---

## 1. Importar el módulo

```python
import csv
from pathlib import Path
````

---

## 2. Leer un archivo CSV

```python id="csv1a2b"
archivo = Path("datos.csv")
archivo.write_text("nombre,edad,ciudad\nÁngel,34,Granada\nLaura,28,Madrid")

with archivo.open(newline='') as f:
    lector = csv.reader(f)
    for fila in lector:
        print(fila)
```

**Salida:**

```python id="csv1r0k"
['nombre', 'edad', 'ciudad']
['Ángel', '34', 'Granada']
['Laura', '28', 'Madrid']
```

> **Analogía mental:** Cada fila es como una **fila de celdas en una hoja de cálculo**, que el lector recorre una por una.

Conexión: [[Módulo pathlib]], [[Lectura y escritura]].

---

## 3. Leer CSV como diccionarios — `csv.DictReader`

```python id="csv2a3b"
with archivo.open(newline='') as f:
    lector = csv.DictReader(f)
    for fila in lector:
        print(fila)
```

**Salida:**

```python id="csv2r1k"
{'nombre': 'Ángel', 'edad': '34', 'ciudad': 'Granada'}
{'nombre': 'Laura', 'edad': '28', 'ciudad': 'Madrid'}
```

> **Analogía:** Cada fila se convierte en un **objeto con etiquetas (keys)**, muy similar a [[Módulo json]].

---

## 4. Escribir un archivo CSV

```python id="csv3a4b"
datos = [
    ['producto', 'precio', 'stock'],
    ['Teclado', 25, 50],
    ['Ratón', 15, 120]
]

archivo_salida = Path("productos.csv")
with archivo_salida.open("w", newline='') as f:
    escritor = csv.writer(f)
    escritor.writerows(datos)
```

> Crea `productos.csv` con todas las filas.
> **Analogía:** Es como llenar una hoja de cálculo fila por fila usando Python.

---

## 5. Escribir CSV como diccionarios — `csv.DictWriter`

```python id="csv4a5b"
campos = ['producto', 'precio', 'stock']
datos_dict = [
    {'producto': 'Monitor', 'precio': 150, 'stock': 20},
    {'producto': 'Teclado', 'precio': 25, 'stock': 50}
]

archivo_dict = Path("inventario.csv")
with archivo_dict.open("w", newline='') as f:
    escritor = csv.DictWriter(f, fieldnames=campos)
    escritor.writeheader()
    escritor.writerows(datos_dict)
```

**Salida en el archivo:**

```text
producto,precio,stock
Monitor,150,20
Teclado,25,50
```

> Muy útil para datos que ya tienen etiquetas, conectable con [[Módulo json]].

---

## 6. Ejemplo práctico — Analizar CSV y filtrar

```python id="csv6a7b"
from pathlib import Path
import csv

archivo = Path("inventario.csv")

with archivo.open(newline='') as f:
    lector = csv.DictReader(f)
    productos_bajos = [p['producto'] for p in lector if int(p['stock']) < 30]

print("Productos con stock bajo:", productos_bajos)
```

**Salida:**

```python id="csv6r4k"
Productos con stock bajo: ['Monitor']
```

Conexión: [[List Comprehension]], [[Módulo pathlib]], [[Dict Comprehension]].

---

## Buenas prácticas

* Usar `newline=''` para evitar problemas de formato en diferentes sistemas.
* Validar los tipos de datos al leer CSV.
* Preferir `DictReader` y `DictWriter` si se necesitan etiquetas.
* Combinar con [[Módulo json]] o [[Módulo pathlib]] para pipelines de datos complejos.

---

## Resumen

* `csv` permite trabajar con datos tabulares de manera flexible.
* Compatible con listas de Python y diccionarios.
* **Analogía final:** El módulo `csv` es como un **asistente que traduce hojas de cálculo a objetos Python y viceversa**, listo para análisis, automatización o integración con APIs.

Conexión: [[Importar módulos]], [[Módulo json]], [[Módulo pathlib]], [[List Comprehension]], [[Dict Comprehension]].

---

