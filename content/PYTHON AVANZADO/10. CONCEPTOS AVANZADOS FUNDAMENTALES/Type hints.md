---
title: "Type hints"
description: "Sistema de anotaciones en Python que permite indicar tipos de variables, parámetros y valores de retorno para mejorar la claridad y el chequeo estático."
tags: ["Python", "Avanzado", "Tipado", "Buenas prácticas"]
date: 2026-03-02
---

# Type hints

Los **type hints** en Python son anotaciones que permiten **indicar el tipo esperado** de variables, parámetros y valores de retorno de funciones.  
No son obligatorios y Python no los aplica en tiempo de ejecución, pero ayudan a:
- Mejorar la **legibilidad del código**.
- Facilitar el **chequeo estático** con herramientas como `mypy`.
- Servir como documentación **automática y clara** para otros desarrolladores.

Se conectan con:
- [[Funciones]]
- [[Funciones lambda]]
- [[Parámetros y argumentos]]
- [[Módulos y entorno]] (para importar `typing`)

---

## Sintaxis básica

```python
def sumar(a: int, b: int) -> int:
    return a + b

resultado: int = sumar(2, 3)
print(resultado)
````

**Salida:**

```text
5
```

* `a: int` y `b: int` indican que ambos parámetros deben ser enteros.
* `-> int` indica que la función devuelve un entero.

---

## Type hints para listas, diccionarios y tuplas

```python
from typing import List, Dict, Tuple

numeros: List[int] = [1, 2, 3]
usuario: Dict[str, str] = {"nombre": "Ángel", "rol": "admin"}
coordenadas: Tuple[float, float] = (40.7128, -74.0060)
```

* Ayuda a herramientas de análisis estático a detectar errores antes de ejecutar el código.

---

## Type hints opcionales con `Optional`

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

```text
Hola Ángel
Hola desconocido
```

* `Optional[str]` significa que el parámetro puede ser `str` o `None`.

---

## Type hints para funciones complejas

```python
from typing import List

def promedio(valores: List[float]) -> float:
    return sum(valores) / len(valores)

print(promedio([3.5, 4.0, 5.0]))
```

**Salida:**

```text
4.166666666666667
```

* Aquí indicamos que la función recibe una lista de flotantes y devuelve un flotante.

---

## Analogía mental

* Imagina los type hints como **carteles de tráfico para programadores**:

  * `a: int` → “Este carril solo es para autos (enteros)”.
  * `-> str` → “Cuando salgas, debes salir por la carretera de strings”.
* No impiden que alguien meta un vehículo equivocado, pero ayudan a detectar problemas antes de un accidente.

---

## Buenas prácticas

✔ Usa type hints para funciones públicas o complejas.
✔ Combínalos con herramientas como `mypy` para validación estática.
✔ Documenta tu código de manera más clara y profesional.
✔ Para tipos genéricos complejos, usa `typing.List`, `typing.Dict`, `typing.Tuple`, `typing.Optional`, etc.

---

## Idea clave final

Los **type hints** no cambian la ejecución de Python, pero mejoran la **claridad, mantenimiento y seguridad** de tu código, funcionando como una guía visual y un sistema de chequeo anticipado de errores.

