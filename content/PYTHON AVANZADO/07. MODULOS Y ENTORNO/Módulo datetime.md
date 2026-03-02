---
title: Módulo datetime — Fechas y horas en Python
description: Uso del módulo datetime en Python para trabajar con fechas, horas y cálculos temporales.
tags: [python, modulos, datetime, fechas, tiempo, automatizacion, analogía]
date: 2026-03-01
---

# Módulo datetime en Python

El módulo `datetime` permite trabajar con:

- Fechas
- Horas
- Tiempos combinados
- Diferencias de tiempo
- Formateo de fechas

Es fundamental en:

- Automatización
- Logs
- Scripts
- Ciberseguridad (análisis de eventos)

> Relacionado con [[Importar módulos]], [[Definir funciones]], [[Docstrings]].

---

## 1. Importar el módulo

```python
import datetime
````

O importar clases específicas:

```python
from datetime import datetime
```

---

## 2. Fecha y hora actual — `datetime.now()`

```python id="dt1a2b"
from datetime import datetime

ahora = datetime.now()
print(ahora)
```

**Salida (ejemplo):**

```python id="dt1r0k"
2026-03-01 18:42:15.123456
```

> **Analogía mental:** Es como mirar el reloj exacto del sistema en ese momento.

---

## 3. Obtener solo la fecha

```python id="dt2a3b"
from datetime import datetime

hoy = datetime.now().date()
print(hoy)
```

**Salida (ejemplo):**

```python id="dt2r1k"
2026-03-01
```

---

## 4. Crear una fecha específica

```python id="dt3a4b"
from datetime import datetime

fecha = datetime(2025, 12, 25)
print(fecha)
```

**Salida:**

```python id="dt3r2k"
2025-12-25 00:00:00
```

> **Analogía:** Estás programando una fecha futura como si la agendaras en un calendario digital.

---

## 5. Acceder a componentes individuales

```python id="dt4a5b"
from datetime import datetime

ahora = datetime.now()

print(ahora.year)
print(ahora.month)
print(ahora.day)
```

**Salida (ejemplo):**

```python id="dt4r3k"
2026
3
1
```

---

## 6. Formatear fecha — `strftime()`

```python id="dt5a6b"
from datetime import datetime

ahora = datetime.now()
formato = ahora.strftime("%d/%m/%Y %H:%M")
print(formato)
```

**Salida (ejemplo):**

```python id="dt5r4k"
01/03/2026 18:45
```

> **Analogía:** Es como cambiar el formato del reloj según el país.

Algunos códigos comunes:

* `%Y` → año completo
* `%m` → mes
* `%d` → día
* `%H` → hora (24h)
* `%M` → minutos
* `%S` → segundos

---

## 7. Diferencia entre fechas

```python id="dt6a7b"
from datetime import datetime

fecha1 = datetime(2026, 3, 1)
fecha2 = datetime(2026, 3, 10)

diferencia = fecha2 - fecha1
print(diferencia.days)
```

**Salida:**

```python id="dt6r5k"
9
```

> **Analogía:** Es como contar cuántos días hay entre dos eventos en un calendario.

---

## 8. Uso práctico — Registro con timestamp

```python id="dt7a8b"
from datetime import datetime

def registrar_evento(mensaje):
    timestamp = datetime.now()
    return f"[{timestamp}] {mensaje}"

print(registrar_evento("Inicio del sistema"))
```

**Salida (ejemplo):**

```python id="dt7r6k"
[2026-03-01 18:50:12.654321] Inicio del sistema
```

Relacionado con [[Definir funciones]] y [[Return]].

Muy útil en análisis de logs y scripting de seguridad.

---

## Buenas prácticas

* Usar `datetime.now()` para timestamps.
* Formatear fechas antes de mostrarlas.
* Usar diferencias de fechas para cálculos temporales.
* Documentar funciones temporales con [[Docstrings]].

---

## Resumen

* `datetime` permite trabajar con fechas y horas.
* Se puede obtener fecha actual, crear fechas y calcular diferencias.
* Fundamental en automatización y análisis de eventos.
* **Analogía final:** El módulo `datetime` es como un **reloj y calendario digital integrado en Python**, listo para registrar y calcular tiempo.

Conexión: [[Importar módulos]], [[Definir funciones]], [[Docstrings]].

---
