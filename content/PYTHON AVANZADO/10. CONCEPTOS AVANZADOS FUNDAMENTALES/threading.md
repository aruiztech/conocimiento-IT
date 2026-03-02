---
title: "threading"
description: "Módulo de Python para crear y manejar hilos (threads) que permiten ejecutar tareas concurrentes dentro de un mismo proceso."
tags: ["Python", "Avanzado", "Concurrencia", "Hilos", "Threading"]
date: 2026-03-02
---

# Módulo threading

El **módulo `threading`** permite **ejecutar varias tareas al mismo tiempo** dentro de un mismo programa usando **hilos (threads)**.  
Se conecta con:
- [[Async y await]] (para concurrencia y multitarea)
- [[Multiprocessing]] (para procesos paralelos)
- [[Funciones]] y [[Generadores]] (como base para tareas)
- [[Logging]] (para registrar ejecución concurrente)

---

## Conceptos clave

- **Thread**: unidad de ejecución que corre dentro de un proceso.  
- **Hilos concurrentes**: varios hilos pueden ejecutarse “simultáneamente”, compartiendo memoria del proceso.  
- **Lock**: mecanismo para evitar condiciones de carrera al acceder a recursos compartidos.

---

## Ejemplo básico de threading

```python id="threading01"
import threading
import time

def saludar(nombre):
    print(f"Hola {nombre}")
    time.sleep(1)
    print(f"Adiós {nombre}")

# Crear hilos
hilo1 = threading.Thread(target=saludar, args=("Ángel",))
hilo2 = threading.Thread(target=saludar, args=("María",))

# Iniciar hilos
hilo1.start()
hilo2.start()

# Esperar a que terminen
hilo1.join()
hilo2.join()
````

**Salida aproximada:**

```text id="threading02"
Hola Ángel
Hola María
Adiós Ángel
Adiós María
```

* Los hilos se ejecutan **casi al mismo tiempo**.
* `join()` asegura que el hilo termine antes de continuar con el programa principal.

---

## Ejemplo con Lock para evitar conflictos

```python id="threading03"
import threading

contador = 0
lock = threading.Lock()

def incrementar():
    global contador
    for _ in range(100000):
        with lock:  # Bloquea acceso al contador
            contador += 1

hilos = [threading.Thread(target=incrementar) for _ in range(5)]

for h in hilos:
    h.start()
for h in hilos:
    h.join()

print(contador)
```

**Salida:**

```text id="threading04"
500000
```

* Sin `lock`, el resultado podría ser menor debido a **condiciones de carrera**.

---

## Analogía mental

* Piensa en **threading** como **varios cocineros en una cocina**:

  * Cada uno prepara un plato (hilo) al mismo tiempo.
  * Comparten los ingredientes (memoria).
  * El **lock** es como un temporizador que asegura que solo un cocinero use un ingrediente delicado a la vez.

---

## Buenas prácticas

✔ Usa `threading` para tareas I/O (red, archivos).
✔ No siempre mejora tareas CPU-intensivas por el **GIL** de Python.
✔ Protege recursos compartidos con **Lock** o mecanismos de sincronización.
✔ Combina con [[Logging]] para rastrear ejecución concurrente.

---

## Idea clave final

`threading` permite **concurrencia real en I/O y multitarea dentro de un proceso**, pero debido al **GIL**, no acelera tareas intensivas en CPU.
Es útil para:

* Programas con múltiples operaciones de red
* Automatización de tareas simultáneas
* Aprender conceptos de sincronización y condición de carrera
  Se conecta con [[Async y await]] y [[Multiprocessing]] para comprender la concurrencia completa en Python.
