---
title: "logging"
description: "Módulo de Python para registrar eventos, errores y mensajes informativos en aplicaciones, facilitando depuración y monitoreo."
tags: ["Python", "Avanzado", "Depuración", "Logging", "Concurrencia"]
date: 2026-03-02
---

# Módulo logging

El **módulo `logging`** permite **registrar mensajes, errores y eventos** en Python, siendo esencial para:
- Depuración de programas complejos  
- Seguimiento de hilos ([[threading]]) y procesos ([[multiprocessing]])  
- Automatización y monitoreo de sistemas  

Se conecta con:
- [[Threading]] y [[Multiprocessing]] para rastrear ejecución concurrente  
- [[try y except]] y [[Raise]] para registrar excepciones  
- [[Funciones]] para logging modular  

---

## Conceptos clave

- **Logger**: objeto principal que emite mensajes.  
- **Handler**: define dónde se envían los mensajes (consola, archivo, etc.).  
- **Formatter**: define el formato de los mensajes.  
- **Niveles de logging**: DEBUG, INFO, WARNING, ERROR, CRITICAL  

---

## Ejemplo básico

```python id="logging01"
import logging

logging.basicConfig(level=logging.INFO)
logging.debug("Esto es un mensaje DEBUG")
logging.info("Esto es un mensaje INFO")
logging.warning("Esto es un mensaje WARNING")
logging.error("Esto es un mensaje ERROR")
logging.critical("Esto es un mensaje CRITICAL")
````

**Salida:**

```text id="logging02"
INFO:root:Esto es un mensaje INFO
WARNING:root:Esto es un mensaje WARNING
ERROR:root:Esto es un mensaje ERROR
CRITICAL:root:Esto es un mensaje CRITICAL
```

* Observa que **DEBUG** no se muestra porque el nivel configurado es `INFO`.

---

## Ejemplo con archivo de registro

```python id="logging03"
import logging

logging.basicConfig(
    filename="app.log",
    level=logging.DEBUG,
    format="%(asctime)s - %(levelname)s - %(message)s"
)

logging.info("Inicio del programa")
logging.error("Ocurrió un error")
```

* Esto crea un archivo `app.log` con mensajes estructurados y timestamp.
* Útil para monitoreo y auditoría en producción.

---

## Ejemplo combinado con try y except

```python id="logging04"
import logging

logging.basicConfig(level=logging.INFO)

try:
    x = 10 / 0
except ZeroDivisionError as e:
    logging.error("Error al dividir: %s", e)
```

**Salida:**

```text id="logging05"
ERROR:root:Error al dividir: division by zero
```

* Permite registrar errores sin detener la ejecución del programa.

---

## Analogía mental

* Piensa en `logging` como un **cuaderno de bitácora de un barco**:

  * Cada evento relevante (info, warning, error) se escribe con fecha y hora.
  * Ayuda a entender qué pasó en el sistema y cuándo.
  * Ideal para sistemas con múltiples cocineros (hilos o procesos) trabajando al mismo tiempo.

---

## Buenas prácticas

✔ Configura `basicConfig` al inicio de tu programa.
✔ Usa distintos niveles según la importancia del mensaje.
✔ Combina con [[Threading]] y [[Multiprocessing]] para depurar concurrencia.
✔ Evita usar `print()` en producción; usa `logging`.
✔ Guarda registros críticos en archivos con `RotatingFileHandler` si el programa es largo.

---

## Idea clave final

`logging` es la **herramienta profesional de Python** para registrar la ejecución de programas, errores y eventos.

* Facilita depuración, auditoría y mantenimiento.
* Es indispensable en proyectos concurrentes o automatizados donde [[print()]] no es suficiente.
* Funciona como columna vertebral para **observabilidad y trazabilidad** en cualquier aplicación Python.

