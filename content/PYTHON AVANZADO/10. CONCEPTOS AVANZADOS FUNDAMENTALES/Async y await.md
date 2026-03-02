---
title: "Async y await"
description: "Conceptos de programación asíncrona en Python que permiten manejar tareas concurrentes sin bloquear la ejecución del programa."
tags: ["Python", "Avanzado", "Asíncrono", "Asyncio", "Concurrencia"]
date: 2026-03-02
---

# Async y await

En Python, **async** y **await** permiten escribir **código asíncrono** que puede ejecutar varias tareas **concurrentemente** sin bloquear el flujo principal del programa.  
Se conectan con:
- [[Funciones]]
- [[Generadores]] (conceptualmente similar en el manejo de pausas)
- [[Threading]] y [[Multiprocessing]] (para comparación de concurrencia)
- [[Logging]] (para registrar tareas asíncronas)

---

## Conceptos clave

- **async def**: define una función asíncrona (coroutine).  
- **await**: pausa la ejecución de la coroutine hasta que la tarea esperada finalice.  
- Se usan comúnmente con **asyncio**, la librería estándar de Python para asincronía.

---

## Ejemplo básico

```python id="async01"
import asyncio

async def saludar(nombre: str):
    print(f"Hola {nombre}")
    await asyncio.sleep(1)  # Simula una tarea que tarda 1 segundo
    print(f"Adiós {nombre}")

async def main():
    await saludar("Ángel")
    await saludar("María")

asyncio.run(main())
````

**Salida aproximada:**

```text id="async02"
Hola Ángel
Adiós Ángel
Hola María
Adiós María
```

* Cada `await` permite que otras coroutines se ejecuten mientras se espera.

---

## Ejecutando tareas concurrentes con `gather`

```python id="async03"
import asyncio

async def tarea(n):
    await asyncio.sleep(n)
    return f"Tarea {n} completada"

async def main():
    resultados = await asyncio.gather(
        tarea(2),
        tarea(1),
        tarea(3)
    )
    print(resultados)

asyncio.run(main())
```

**Salida (aproximada según tiempos de espera):**

```text id="async04"
['Tarea 2 completada', 'Tarea 1 completada', 'Tarea 3 completada']
```

* `asyncio.gather` permite **ejecutar varias coroutines al mismo tiempo** y esperar a que todas terminen.

---

## Analogía mental

* Imagina que eres un **chef en la cocina**:

  * Preparas varios platos a la vez (coroutines).
  * Mientras un plato se hornea (`await`), puedes preparar otro.
  * No necesitas esperar que un plato termine para empezar con otro.

---

## Buenas prácticas

✔ Usa async/await solo cuando haya tareas que **tarden en completarse**, como operaciones de red o I/O.
✔ Evita usar `time.sleep()` en coroutines; usa `asyncio.sleep()`.
✔ Combina con `asyncio.gather()` para ejecutar varias tareas concurrentes.
✔ No mezclar código síncrono pesado dentro de coroutines (puede bloquear el event loop).

---

## Idea clave final

**Async y await** permiten escribir programas que hacen varias cosas al mismo tiempo sin bloquear la ejecución principal. Es fundamental para:

* Programación de servicios web
* Automatización de tareas de red
* Manejo eficiente de I/O
  Se conecta con [[Funciones]], [[Generadores]] y [[Threading]] para un entendimiento completo de concurrencia en Python.

