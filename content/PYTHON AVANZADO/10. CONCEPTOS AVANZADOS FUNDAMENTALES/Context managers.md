---
title: "Context managers"
description: "Estructuras en Python que manejan recursos de manera automática, asegurando apertura y cierre correcto mediante 'with'."
tags: ["Python", "Avanzado", "Manejo de recursos", "Decoradores"]
date: 2026-03-02
---

# Context managers

Un **context manager** en Python es un patrón que permite **administrar recursos** (archivos, conexiones, locks) asegurando que se **abran y cierren correctamente**, incluso si ocurre un error.

- Se utilizan principalmente con la sentencia `with`.
- Conecta con:
  - [[Manejo de archivos]]
  - [[Decoradores]] (para crear context managers personalizados)
  - [[try y except]]
  - [[finally]]

---

## Concepto clave

- Los context managers controlan la **entrada y salida de un bloque de código**.  
- Garantizan que los recursos se liberen adecuadamente, evitando **fugas de memoria o errores de bloqueo**.  
- Se implementan con los métodos especiales `__enter__()` y `__exit__()`.

---

## Uso básico con archivos

```python
with open("archivo.txt", "w") as f:
    f.write("Hola mundo")
````

* Python se encarga de **cerrar el archivo automáticamente** al salir del bloque `with`.
* Equivalente a:

```python
f = open("archivo.txt", "w")
try:
    f.write("Hola mundo")
finally:
    f.close()
```

---

## Creando un context manager personalizado

```python
class MiContexto:
    def __enter__(self):
        print("Entrando al contexto")
        return self

    def __exit__(self, exc_type, exc_val, exc_tb):
        print("Saliendo del contexto")
        if exc_type:
            print(f"Ocurrió un error: {exc_val}")
        return True  # evita que la excepción se propague

with MiContexto() as mc:
    print("Dentro del bloque")
    x = 1 / 0  # Error que será manejado
```

**Salida:**

```text id="ctx1-output"
Entrando al contexto
Dentro del bloque
Ocurrió un error: division by zero
Saliendo del contexto
```

* La excepción se **captura y maneja** dentro del context manager gracias a `__exit__`.

---

## Decorador `contextmanager`

Python también permite crear context managers usando **decoradores** del módulo `contextlib`:

```python
from contextlib import contextmanager

@contextmanager
def mi_contexto():
    print("Antes del bloque")
    yield
    print("Después del bloque")

with mi_contexto():
    print("Dentro del bloque")
```

**Salida:**

```text id="ctx2-output"
Antes del bloque
Dentro del bloque
Después del bloque
```

* `yield` separa la parte **pre-bloque** de la parte **post-bloque**.

---

## Analogía mental

* Imagina que un context manager es como **alquilar un coche**:

  * `__enter__` → recibir las llaves y subir al coche.
  * Bloque de código → conduces el coche.
  * `__exit__` → devuelves las llaves, sin importar si tuviste un percance.

---

## Buenas prácticas

✔ Siempre usa `with` al manejar recursos externos (archivos, sockets, locks).
✔ Para recursos críticos, implementa context managers personalizados.
✔ Captura excepciones dentro de `__exit__` solo si deseas manejarlas.
✔ Combina context managers con decoradores para crear patrones reutilizables y seguros.

---

## Idea clave final

Los **context managers** permiten escribir código **limpio, seguro y predecible** al manejar recursos, eliminando la necesidad de cerrar manualmente o limpiar en bloques `try/finally`.
