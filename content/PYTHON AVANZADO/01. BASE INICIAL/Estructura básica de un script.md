---
title: Estructura básica de un script
description: Explicación sobre la estructura de un script en Python, ejemplos mínimos y buenas prácticas.
tags: [Python, scripts, estructura, buenas prácticas]
date: 2026-02-28
---

# Estructura básica de un script

Un **script** en Python es un archivo con extensión `.py` que contiene instrucciones que el intérprete ejecuta de arriba hacia abajo.  

Comprender su estructura es fundamental para escribir código organizado y profesional.

---

## Conceptos clave

- Un script se ejecuta de forma secuencial (de arriba hacia abajo).  
- Puede contener:  
  - Comentarios  
  - Variables  
  - Funciones  
  - Condicionales  
  - Bucles  
- Puede ejecutarse desde la terminal.  
- Puede incluir un bloque especial: `if __name__ == "__main__"`.

---

## Ejemplo mínimo de un script

```python
# Este es mi primer script

nombre = "Angel"

print("Hola", nombre)
````

### Resultado al ejecutar:

```text
Hola Angel
```

---

## Estructura recomendada de un script profesional

```python id="l2p7yx"
"""
Descripción del script.
Autor: Tu nombre
Fecha: YYYY-MM-DD
"""

# Importaciones
import math

# Constantes
PI = 3.1416

# Funciones
def saludar(nombre):
    return f"Hola {nombre}"

# Código principal
if __name__ == "__main__":
    mensaje = saludar("Angel")
    print(mensaje)
```

### Resultado al ejecutar:

```text
Hola Angel
```

---

## Qué está pasando

1. Python lee el archivo de arriba hacia abajo.
2. Define variables y funciones.
3. Cuando llega al bloque principal, ejecuta el código dentro.
4. Llama a la función `saludar()` y muestra el resultado.

---

## Errores comunes

* Mezclar todo el código sin orden.
* No usar funciones en scripts largos.
* No usar el bloque `if __name__ == "__main__"` en proyectos más grandes.
* No documentar el propósito del archivo.

---

## Conecta con

* [[Cómo ejecutar un archivo .py]]
* [[Comentarios en Python]]
* [[Funciones]]
* [[Importar módulos]]
* [[if **name** == "**main**"]]

---

## Analogía mental

Un script es como una receta:

1. Ingredientes (importaciones y variables).
2. Preparación (funciones).
3. Ejecución final (bloque principal).

Si todo está desordenado, la receta falla.


