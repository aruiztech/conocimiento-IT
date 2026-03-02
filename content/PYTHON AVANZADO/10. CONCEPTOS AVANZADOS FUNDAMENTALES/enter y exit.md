---
title: "__enter__ y __exit__"
description: "Métodos especiales para implementar context managers en Python, controlando la entrada y salida de bloques de código."
tags: ["Python", "Avanzado", "Context managers", "POO", "Manejo de recursos"]
date: 2026-03-02
---

# __enter__ y __exit__

En Python, los **métodos especiales `__enter__` y `__exit__`** permiten definir el comportamiento de un **context manager personalizado**, usado con la sentencia `with`.  
Se conectan con:
- [[Context managers]]
- [[Decoradores]]
- [[try y except]]
- [[finally]]
- [[Manejo de archivos]]

---

## Concepto clave

- `__enter__`: se ejecuta **al iniciar el bloque `with`**, puede devolver un objeto que será usado dentro del bloque.  
- `__exit__`: se ejecuta **al finalizar el bloque `with`**, incluso si ocurre una excepción.  
  - Parámetros de `__exit__`:
    - `exc_type`: tipo de excepción (o `None` si no hubo)
    - `exc_val`: valor/instancia de la excepción
    - `exc_tb`: traceback de la excepción

---

## Ejemplo simple

```python
class ContextoEjemplo:
    def __enter__(self):
        print("Entrando al contexto")
        return "Recurso"

    def __exit__(self, exc_type, exc_val, exc_tb):
        print("Saliendo del contexto")
        if exc_type:
            print(f"Ocurrió un error: {exc_val}")
        return True  # previene que la excepción se propague

with ContextoEjemplo() as recurso:
    print(f"Dentro del bloque usando: {recurso}")
    x = 1 / 0  # Genera excepción
````

**Salida:**

```text
Entrando al contexto
Dentro del bloque usando: Recurso
Ocurrió un error: division by zero
Saliendo del contexto
```

* Observa que la excepción se **captura dentro de `__exit__`** y no se propaga.

---

## Analogía mental

* Piensa en `__enter__` y `__exit__` como **abrir y cerrar un portal mágico**:

  * `__enter__` → abrir el portal y preparar el entorno.
  * Bloque `with` → usar lo que hay dentro del portal.
  * `__exit__` → cerrar el portal y limpiar todo lo que se usó, sin importar si ocurrió un accidente dentro.

---

## Ejemplo práctico: manejo de archivos

```python
class AbrirArchivo:
    def __init__(self, nombre, modo):
        self.nombre = nombre
        self.modo = modo
        self.archivo = None

    def __enter__(self):
        self.archivo = open(self.nombre, self.modo)
        return self.archivo

    def __exit__(self, exc_type, exc_val, exc_tb):
        if self.archivo:
            self.archivo.close()
        if exc_type:
            print(f"Error al trabajar con el archivo: {exc_val}")
        return False  # permite que la excepción se propague si la hay

with AbrirArchivo("archivo.txt", "w") as f:
    f.write("Hola desde __enter__ y __exit__")
    # f.write(5)  # Esto generaría un TypeError
```

**Salida si no hay error:**

```text
# archivo.txt creado con contenido: "Hola desde __enter__ y __exit__"
```

**Salida si se descomenta la línea con error:**

```text
Error al trabajar con el archivo: write() argument must be str, not int
Traceback (most recent call last):
  ...
TypeError: write() argument must be str, not int
```

* `__exit__` permite **cerrar recursos siempre**, similar a `finally`.

---

## Buenas prácticas

✔ Devuelve en `__enter__` el recurso que será usado dentro del bloque.
✔ Devuelve `True` en `__exit__` solo si quieres **suprimir excepciones**; de lo contrario devuelve `False` para que se propaguen.
✔ Úsalo siempre que manejes recursos que necesiten **limpieza garantizada** (archivos, sockets, locks, conexiones).
✔ Combínalo con decoradores para crear patrones reutilizables de gestión de recursos.

---

## Idea clave final

`__enter__` y `__exit__` son **la base de los context managers**: permiten **abrir, usar y cerrar recursos de forma automática**, asegurando seguridad y limpieza en cualquier situación, incluso frente a errores inesperados.
