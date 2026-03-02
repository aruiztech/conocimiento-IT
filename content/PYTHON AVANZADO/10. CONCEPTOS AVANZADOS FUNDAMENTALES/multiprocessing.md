---
title: "multiprocessing"
description: "Módulo de Python que permite crear procesos independientes para ejecutar tareas en paralelo y aprovechar múltiples núcleos de CPU."
tags: ["Python", "Avanzado", "Concurrencia", "Procesos", "Multiprocessing"]
date: 2026-03-02
---

# Módulo multiprocessing

El **módulo `multiprocessing`** permite crear **procesos separados** que se ejecutan en paralelo y **no comparten memoria**, a diferencia de [[threading]].  
Se conecta con:
- [[Threading]] (para comparación de hilos vs procesos)
- [[Async y await]] (para concurrencia en I/O)
- [[Funciones]] y [[Generadores]] (como base para tareas)
- [[Logging]] (para rastrear ejecución de procesos)

---

## Conceptos clave

- **Proceso**: programa en ejecución con su propio espacio de memoria.  
- **Pool**: conjunto de procesos que pueden ejecutar tareas de manera concurrente.  
- **Queue / Pipe**: mecanismos para comunicación entre procesos.  
- Los procesos pueden aprovechar **múltiples núcleos de CPU**, superando las limitaciones del **GIL**.

---

## Ejemplo básico de multiprocessing

```python id="multiprocessing01"
from multiprocessing import Process
import time

def saludar(nombre):
    print(f"Hola {nombre}")
    time.sleep(1)
    print(f"Adiós {nombre}")

# Crear procesos
p1 = Process(target=saludar, args=("Ángel",))
p2 = Process(target=saludar, args=("María",))

# Iniciar procesos
p1.start()
p2.start()

# Esperar a que terminen
p1.join()
p2.join()
````

**Salida aproximada:**

```text id="multiprocessing02"
Hola Ángel
Hola María
Adiós Ángel
Adiós María
```

* Cada proceso tiene **memoria independiente**, por lo que no hay riesgo de sobrescribir variables compartidas.

---

## Ejemplo con Pool para paralelizar tareas

```python id="multiprocessing03"
from multiprocessing import Pool

def cuadrado(n):
    return n * n

if __name__ == "__main__":
    numeros = [1, 2, 3, 4, 5]
    with Pool(3) as p:  # 3 procesos en paralelo
        resultados = p.map(cuadrado, numeros)
    print(resultados)
```

**Salida:**

```text id="multiprocessing04"
[1, 4, 9, 16, 25]
```

* `Pool.map()` distribuye la lista de tareas entre los procesos disponibles.

---

## Analogía mental

* Piensa en **multiprocessing** como **varias cocinas independientes**:

  * Cada cocina tiene sus propios utensilios y espacio (memoria independiente).
  * Cada chef puede trabajar sin interferir en la otra cocina.
  * Ideal cuando quieres preparar **muchos platos pesados** al mismo tiempo (CPU-intensivos).

---

## Buenas prácticas

✔ Usa `multiprocessing` para tareas intensivas en CPU.
✔ Evita compartir variables globales; usa **Queue**, **Pipe**, o archivos temporales.
✔ Protege la creación de procesos con `if __name__ == "__main__":` para evitar bucles infinitos en Windows.
✔ Combina con [[Logging]] para seguimiento de procesos.

---

## Idea clave final

`multiprocessing` permite ejecutar tareas **realmente en paralelo**, aprovechando todos los núcleos del CPU, superando las limitaciones de [[threading]] por el **GIL**.
Se utiliza principalmente para:

* Cálculos intensivos
* Procesamiento de datos masivos
* Automatización de tareas que requieren CPU
* Experimentos de concurrencia avanzada en Python

