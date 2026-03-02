---
title: "Decoradores"
description: "Funciones que reciben otra función como argumento y devuelven una nueva función modificada, permitiendo agregar comportamiento de manera flexible."
tags: ["Python", "POO", "Funciones", "Avanzado", "Decoradores"]
date: 2026-03-02
---

# Decoradores

Un **decorador** en Python es una función que **toma otra función como argumento**, le añade funcionalidad adicional y devuelve una **nueva función modificada**.  
Permite aplicar **comportamientos repetitivos** sin modificar el código original de las funciones.

Conecta con:
- [[Funciones]]
- [[Funciones como argumentos]]
- [[Docstrings]]
- [[Generadores]] (cuando se decoran)
- [[Logging]] (para seguimiento de funciones)

---

## Concepto clave

- Decoradores usan funciones de **primer orden** (pueden pasarse como argumentos).  
- Se aplican con el **símbolo `@nombre_decorador`** justo antes de la definición de la función.  
- Permiten **enriquecer funciones**, como medir tiempos, validar datos o registrar llamadas.

---

## Ejemplo básico de decorador

```python
def decorador_simple(func):
    def nueva_funcion():
        print("Antes de la función")
        func()
        print("Después de la función")
    return nueva_funcion

@decorador_simple
def saludar():
    print("Hola mundo")

saludar()
````

**Salida:**

```text id="dec1-output"
Antes de la función
Hola mundo
Después de la función
```

* `saludar` ahora está envuelta por `decorador_simple`, que añade comportamiento **antes y después**.

---

## Decorador con argumentos

```python id="dec2-args"
def decorador_args(func):
    def wrapper(*args, **kwargs):
        print("Argumentos recibidos:", args, kwargs)
        return func(*args, **kwargs)
    return wrapper

@decorador_args
def sumar(a, b):
    return a + b

resultado = sumar(3, 5)
print("Resultado:", resultado)
```

**Salida:**

```text id="dec2-output"
Argumentos recibidos: (3, 5) {}
Resultado: 8
```

* `*args` y `**kwargs` permiten que el decorador funcione con **cualquier función** sin importar sus parámetros.

---

## Decoradores anidados y múltiples

```python id="dec3-multi"
def mayusculas(func):
    def wrapper():
        return func().upper()
    return wrapper

def exclamacion(func):
    def wrapper():
        return func() + "!"
    return wrapper

@exclamacion
@mayusculas
def mensaje():
    return "hola mundo"

print(mensaje())
```

**Salida:**

```text id="dec3-output"
HOLA MUNDO!
```

* Los decoradores se aplican **de abajo hacia arriba**: `@mayusculas` primero, luego `@exclamacion`.

---

## Analogía mental

* Piensa en decoradores como **envolver un regalo**:

  * La función original es el regalo.
  * Cada decorador añade **una capa extra** (cinta, papel, tarjeta).
  * Al final, cuando abres el paquete, ves tanto el regalo como las mejoras añadidas.

---

## Buenas prácticas

✔ Usa decoradores para separar **lógica transversal** (logging, validación, métricas) del **núcleo funcional**.
✔ Mantén el `wrapper` limpio y utiliza `functools.wraps(func)` para **preservar nombre y docstring**.
✔ Evita decoradores excesivamente complejos; pueden complicar la lectura.
✔ Combina decoradores con generadores para pipelines de datos avanzados.

```python id="dec4-wraps"
from functools import wraps

def decorador(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        """Wrapper que preserva docstring y nombre original"""
        print("Antes")
        return func(*args, **kwargs)
    return wrapper
```

---

## Idea clave final

Los **decoradores** son una herramienta poderosa para **modificar o extender el comportamiento de funciones y métodos** de manera elegante y reutilizable, manteniendo el código limpio y modular.
