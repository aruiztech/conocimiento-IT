---
title: "typing"
description: "Módulo de Python que proporciona clases y herramientas para usar anotaciones de tipo avanzadas (type hints) en variables, funciones y estructuras de datos."
tags: ["Python", "Avanzado", "Type hints", "Buenas prácticas"]
date: 2026-03-02
---

# Módulo typing

El **módulo `typing`** de Python permite **mejorar y ampliar las anotaciones de tipo** (type hints), especialmente en colecciones y tipos complejos.  
Se conecta con:
- [[Type hints]]
- [[Funciones]]
- [[Listas]], [[Diccionarios]], [[Tuplas]]
- [[Funciones lambda]]

---

## Importando `typing`

```python
from typing import List, Dict, Tuple, Optional, Union
````

* Permite declarar tipos más precisos y complejos.

---

## Ejemplos básicos

### Listas y diccionarios

```python
from typing import List, Dict

numeros: List[int] = [1, 2, 3]
usuarios: Dict[str, int] = {"Ángel": 34, "María": 28}

print(numeros)
print(usuarios)
```

**Salida:**

```text id="tt1"
[1, 2, 3]
{'Ángel': 34, 'María': 28}
```

---

### Tuplas

```python
from typing import Tuple

coordenadas: Tuple[float, float] = (40.7128, -74.0060)
print(coordenadas)
```

**Salida:**

```text id="tt2"
(40.7128, -74.006)
```

---

### Tipos opcionales

```python
from typing import Optional

def saludar(nombre: Optional[str] = None) -> str:
    if nombre:
        return f"Hola {nombre}"
    return "Hola desconocido"

print(saludar("Ángel"))
print(saludar())
```

**Salida:**

```text id="tt3"
Hola Ángel
Hola desconocido
```

* `Optional[str]` equivale a `Union[str, None]`.

---

### Unión de tipos con `Union`

```python
from typing import Union

def procesar(valor: Union[int, str]) -> str:
    return f"Procesando {valor}"

print(procesar(10))
print(procesar("texto"))
```

**Salida:**

```text id="tt4"
Procesando 10
Procesando texto
```

---

### Funciones complejas con `Callable`

```python
from typing import Callable

def aplicar_funcion(f: Callable[[int], int], valor: int) -> int:
    return f(valor)

resultado = aplicar_funcion(lambda x: x * 2, 5)
print(resultado)
```

**Salida:**

```text id="tt5"
10
```

* `Callable[[int], int]` indica que la función recibe un `int` y devuelve un `int`.

---

## Analogía mental

* Piensa en `typing` como un **manual de instrucciones para tu código**:

  * Le dice al programador “este bloque espera esto, devuelve esto otro”.
  * Evita errores por confusión de tipos y facilita el chequeo antes de ejecutar.

---

## Buenas prácticas

✔ Usa `typing` para funciones complejas o librerías públicas.
✔ Combina con `mypy` o `Pyright` para **verificación estática de tipos**.
✔ Usa `Optional`, `Union` y `Callable` para mayor claridad en los parámetros y retornos.
✔ Documenta tus colecciones y estructuras de datos complejas para mejorar la mantenibilidad del código.

---

## Idea clave final

El módulo `typing` **potencia los type hints**, permitiendo definir tipos más precisos y complejos, facilitando el mantenimiento y la detección temprana de errores, y conectando directamente con [[Type hints]] y buenas prácticas de desarrollo profesional en Python.
