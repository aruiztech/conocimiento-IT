---
title: Módulo json — Manipulación de datos en formato JSON
description: Uso del módulo json en Python para leer, escribir y procesar datos en formato JSON. Ideal para APIs y almacenamiento de información estructurada.
tags: [python, modulos, json, datos, api, automatizacion, ciberseguridad, analogía]
date: 2026-03-02
---

# Módulo json en Python

El módulo `json` permite trabajar con **datos en formato JSON**, un estándar de intercambio de información muy usado en:

- APIs web
- Configuración de aplicaciones
- Almacenamiento ligero
- Intercambio de datos entre sistemas

> Relacionado con [[Importar módulos]], [[Módulo re]], [[Lectura y escritura]], [[Sockets]].

---

## 1. Importar el módulo

```python
import json
````

---

## 2. Convertir objeto Python a JSON — `json.dumps()`

```python id="json1a2b"
import json

data = {"nombre": "Ángel", "edad": 34, "activo": True}
json_str = json.dumps(data)
print(json_str)
```

**Salida:**

```python id="json1r0k"
{"nombre": "Ángel", "edad": 34, "activo": true}
```

> **Analogía mental:** `dumps` es como empacar tus objetos Python en una **caja estándar que otros sistemas pueden abrir**.

Relacionado con [[Módulo datetime]] y [[Lectura y escritura]].

---

## 3. Convertir JSON a objeto Python — `json.loads()`

```python id="json2a3b"
import json

json_str = '{"nombre": "Ángel", "edad": 34, "activo": true}'
data = json.loads(json_str)
print(data)
print(type(data))
```

**Salida:**

```python id="json2r1k"
{'nombre': 'Ángel', 'edad': 34, 'activo': True}
<class 'dict'>
```

> **Analogía:** Abrir la caja y tener tus objetos listos para usar en Python.

---

## 4. Leer JSON desde archivo — `json.load()`

```python id="json3a4b"
import json
from pathlib import Path

archivo = Path("data.json")
archivo.write_text('{"pais": "España", "ciudad": "Granada"}')

with archivo.open("r") as f:
    datos = json.load(f)

print(datos)
```

**Salida:**

```python id="json3r2k"
{'pais': 'España', 'ciudad': 'Granada'}
```

> Conexión: [[Módulo pathlib]], [[Lectura y escritura]].

---

## 5. Escribir JSON a archivo — `json.dump()`

```python id="json4a5b"
import json
from pathlib import Path

data = {"usuario": "angel", "nivel": "experto"}
archivo = Path("output.json")

with archivo.open("w") as f:
    json.dump(data, f)
```

* Crea o sobrescribe `output.json` con la información de `data`.

> Analógico a empacar tus objetos en una **caja y guardarla en un estante (archivo)**.

---

## 6. Formato legible — `indent`

```python id="json5a6b"
import json

data = {"nombre": "Ángel", "edad": 34, "activo": True}
json_str = json.dumps(data, indent=4)
print(json_str)
```

**Salida:**

```python id="json5r3k"
{
    "nombre": "Ángel",
    "edad": 34,
    "activo": true
}
```

> Hace que el JSON sea más fácil de leer por humanos.

---

## 7. Ejemplo práctico — API simulada

```python id="json6a7b"
import json
from pathlib import Path

respuesta_api = '{"status": "ok", "result": [1, 2, 3, 4]}'
datos = json.loads(respuesta_api)
print(f"Status: {datos['status']}")
print(f"Resultados: {datos['result']}")
```

**Salida:**

```python id="json6r4k"
Status: ok
Resultados: [1, 2, 3, 4]
```

Conexión: [[Sockets]], [[Requests]], [[JSON y APIs REST]].

---

## Buenas prácticas

* Validar JSON antes de procesar.
* Usar `indent` para archivos de configuración legibles.
* Manejar excepciones con `try-except` para errores de parsing.
* Combinar con [[Módulo re]] para validar patrones en datos.

---

## Resumen

* `json` es esencial para trabajar con datos estructurados en Python.
* Facilita el intercambio de información entre sistemas y APIs.
* **Analogía final:** El módulo `json` es como una **caja estandarizada de objetos Python** que cualquier otro sistema puede abrir y entender.

Conexión: [[Importar módulos]], [[Módulo re]], [[Lectura y escritura]], [[Sockets]], [[Módulo pathlib]].

---

