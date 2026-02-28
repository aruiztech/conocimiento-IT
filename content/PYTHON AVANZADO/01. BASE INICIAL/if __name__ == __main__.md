---
title: if __name__ == "__main__"
description: Explicación sobre la estructura `if __name__ == "__main__"` en Python, con ejemplos y buenas prácticas.
tags: [Python, scripts, buenas prácticas, __main__]
date: 2026-02-28
---

# if __name__ == "__main__"

La línea:

```python
if __name__ == "__main__":
````

es una estructura especial en Python que permite ejecutar cierto código **solo cuando el archivo se ejecuta directamente**, y no cuando es importado como módulo.

Es una práctica profesional y muy importante.

---

## Conceptos clave

* `__name__` es una variable especial que Python crea automáticamente.
* Cuando ejecutas un archivo directamente, `__name__` vale `"__main__"`.
* Cuando el archivo es importado, `__name__` vale el nombre del archivo.
* Permite separar:

  * Código reutilizable (funciones, clases)
  * Código ejecutable (pruebas, ejecución principal)

---

## Ejemplo básico

Archivo: `ejemplo.py`

```python
print("Este archivo se está ejecutando")

print(__name__)
```

### Resultado al ejecutar directamente:

```text id="t3lf1h"
Este archivo se está ejecutando
__main__
```

Python asigna automáticamente `"__main__"` cuando el archivo es el principal.

---

## Ejemplo con importación

Archivo: `modulo.py`

```python
print("El módulo se ha cargado")
print(__name__)
```

Archivo: `principal.py`

```python
import modulo
```

### Resultado al ejecutar `principal.py`:

```text id="a9kl2p"
El módulo se ha cargado
modulo
```

Aquí `__name__` ya no vale `"__main__"`, sino el nombre del archivo.

---

## Uso profesional correcto

```python id="p8kj4v"
def saludar(nombre):
    return f"Hola {nombre}"

if __name__ == "__main__":
    mensaje = saludar("Angel")
    print(mensaje)
```

### Resultado al ejecutar el archivo directamente:

```text id="w7g3hs"
Hola Angel
```

Si este archivo se importa desde otro, el bloque dentro del `if` **no se ejecutará**.

---

## ¿Por qué es importante?

Sin esta estructura:

* Todo el código se ejecuta al importar el archivo.
* Puede generar errores inesperados.
* No permite reutilizar código correctamente.

Con esta estructura:

* Puedes reutilizar funciones.
* Puedes hacer pruebas dentro del mismo archivo.
* Separas lógica de ejecución.

---

## Analogía mental

Imagina que el archivo es una fábrica:

* Las funciones son las máquinas.
* El bloque `if __name__ == "__main__"` es el botón de encendido.

Si solo importas la fábrica, no se enciende.
Si la ejecutas directamente, se activa la producción.

---

## Errores comunes

* Escribir mal la línea:

```python
if name == "main":   # ❌ Incorrecto
```

Debe llevar doble guion bajo:

```python
if __name__ == "__main__":  # ✅ Correcto
```

* Olvidar la indentación del bloque.

---

## Conecta con

* [[Estructura básica de un script]]
* [[Importar módulos]]
* [[Funciones]]
* [[Módulos]]

