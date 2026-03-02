---
title: "try y except"
description: "Cómo manejar excepciones en Python usando try y except para evitar que el programa se detenga."
tags: ["Python", "Errores", "Excepciones", "Depuración"]
date: 2026-03-02
---

# try y except

`try` y `except` permiten **capturar y manejar errores** sin que el programa se detenga abruptamente.

En lugar de dejar que Python muestre un traceback y termine el programa, podemos **controlar el flujo cuando ocurre un error**.

Conecta directamente con:

- [[Errores comunes]]
- [[Traceback]]
- [[else en excepciones]]
- [[finally]]
- [[raise]]

---

## ¿Por qué necesitamos try y except?

Por defecto, cuando ocurre una excepción:

- Python muestra el [[Traceback]]
- El programa se detiene

Ejemplo sin manejo:

```python
numero = int(input("Introduce un número: "))
print(10 / numero)
````

Si el usuario introduce `0`:

```text
ZeroDivisionError: division by zero
```

El programa termina.

---

## Estructura básica

```python
try:
    # Código que puede fallar
except TipoDeError:
    # Código que se ejecuta si ocurre ese error
```

---

## Ejemplo básico

```python
try:
    numero = int(input("Introduce un número: "))
    resultado = 10 / numero
    print("Resultado:", resultado)
except ZeroDivisionError:
    print("No puedes dividir entre cero.")
```

Si el usuario introduce `0`, salida:

```text
No puedes dividir entre cero.
```

El programa no se rompe.

---

## Analogía mental

Imagina que conduces un coche.

* `try` → Conduces normalmente.
* `except` → Airbag si hay accidente.

No evita el accidente, pero evita que el sistema colapse.

---

## Capturar múltiples excepciones

Puedes manejar diferentes errores por separado:

```python
try:
    numero = int(input("Introduce un número: "))
    resultado = 10 / numero
except ZeroDivisionError:
    print("División por cero.")
except ValueError:
    print("Debes introducir un número válido.")
```

Si el usuario escribe `"hola"`:

```text
Debes introducir un número válido.
```

Conexión con [[ValueError]] y [[Errores comunes]].

---

## Capturar múltiples errores en un solo bloque

```python
except (ValueError, ZeroDivisionError):
    print("Entrada inválida.")
```

Útil cuando el tratamiento es el mismo.

---

## Capturar cualquier excepción (uso con cuidado)

```python
try:
    x = int("hola")
except Exception as e:
    print("Ha ocurrido un error:", e)
```

Salida:

```text
Ha ocurrido un error: invalid literal for int() with base 10: 'hola'
```

Aquí:

* `Exception` captura casi cualquier error.
* `as e` guarda el error en una variable.

⚠️ No es buena práctica usar siempre `except Exception` sin necesidad. Es mejor capturar errores específicos.

---

## Acceder al mensaje del error

```python
try:
    10 / 0
except ZeroDivisionError as error:
    print("Error detectado:", error)
```

Salida:

```text
Error detectado: division by zero
```

Esto es útil para:

* Logging
* Debugging
* Sistemas profesionales

Conecta con [[logging]].

---

## Qué no hacer

❌ No usar `try` para ocultar errores lógicos.

Ejemplo incorrecto:

```python
try:
    lista = [1, 2, 3]
    print(lista[10])
except:
    pass
```

Esto silencia el error.

Problema:

* No sabes que tu programa está fallando.
* Genera bugs ocultos.

Regla profesional:
Solo captura errores que realmente esperas que puedan ocurrir.

---

## Buen patrón profesional

Validar + capturar:

```python
try:
    numero = int(input("Introduce un número: "))
    if numero == 0:
        print("No se permite cero.")
    else:
        print(10 / numero)
except ValueError:
    print("Entrada inválida.")
```

Aquí mezclamos:

* Validación lógica
* Manejo de excepción

---

## try y control de flujo

Las excepciones cambian el flujo normal del programa.

Sin error:

* Se ejecuta el bloque `try`
* Se ignora `except`

Con error:

* Se salta el resto del `try`
* Se ejecuta el `except`

---

## Visualización mental del flujo

```
try:
    paso 1
    paso 2
    error aquí
    paso 3  ← no se ejecuta
except:
    manejo del error
```

---

## Casos reales donde usar try y except

* Entrada de usuario ([[input()]])
* Lectura de archivos ([[Manejo de archivos]])
* Conexiones de red ([[Sockets]])
* APIs externas ([[JSON y APIs REST]])
* Conversión de tipos

---

## Conexión con programación profesional

En proyectos reales:

* No puedes permitir que un error de usuario tumbe todo el sistema.
* Debes manejar fallos de red.
* Debes capturar errores de base de datos.
* Debes registrar errores en logs.

Por eso `try` y `except` son fundamentales para:

* Automatización
* APIs
* Ciberseguridad
* Scripts de sistema

---

## Próximas notas relacionadas

* [[else en excepciones]]
* [[finally]]
* [[raise]]
* [[Crear excepciones personalizadas]]

---

