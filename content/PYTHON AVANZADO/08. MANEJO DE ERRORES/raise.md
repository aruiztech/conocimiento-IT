---
title: "raise"
description: "Uso de raise en Python para lanzar excepciones manualmente."
tags: ["Python", "Excepciones", "Control de flujo", "Errores"]
date: 2026-03-02
---

# raise

`raise` se usa para **lanzar una excepción manualmente**.

Hasta ahora hemos visto cómo capturar errores con:

- [[try y except]]
- [[else en excepciones]]
- [[finally]]

Pero `raise` permite **crear o propagar errores de forma intencional**.

---

## ¿Por qué lanzar un error manualmente?

Porque a veces:

- Los datos son inválidos.
- El estado del programa es incorrecto.
- Se rompe una regla de negocio.
- Queremos detener la ejecución.

Un programador profesional no solo captura errores.

También los genera cuando es necesario.

---

## Sintaxis básica

```python
raise TipoDeError("mensaje opcional")
````

---

## Ejemplo simple

```python
edad = -5

if edad < 0:
    raise ValueError("La edad no puede ser negativa.")
```

Salida:

```text
ValueError: La edad no puede ser negativa.
```

Aquí no hubo un error natural del sistema.

El programador decidió que esa situación es inválida.

---

## raise dentro de funciones

Muy común en validaciones:

```python
def dividir(a, b):
    if b == 0:
        raise ZeroDivisionError("No se permite dividir entre cero.")
    return a / b

print(dividir(10, 0))
```

Esto obliga a quien use la función a manejar el error.

Conecta con:

* [[ZeroDivisionError]]
* [[ValueError]]
* [[Errores comunes]]

---

## Propagar una excepción capturada

A veces quieres hacer algo y luego relanzar el error:

```python
try:
    numero = int("hola")
except ValueError:
    print("Ocurrió un error.")
    raise
```

Salida:

```text
Ocurrió un error.
ValueError: invalid literal for int()
```

`raise` sin argumentos vuelve a lanzar la excepción actual.

Esto se llama **re-lanzar la excepción**.

---

## Patrón profesional: Validación estricta

```python
def crear_usuario(nombre):
    if not nombre:
        raise ValueError("El nombre es obligatorio.")
    
    if len(nombre) < 3:
        raise ValueError("El nombre es demasiado corto.")
    
    return {"nombre": nombre}
```

Aquí `raise` actúa como mecanismo de defensa.

---

## Crear excepciones personalizadas

Puedes definir tus propios errores:

```python
class EdadInvalidaError(Exception):
    pass

def registrar_edad(edad):
    if edad < 0:
        raise EdadInvalidaError("Edad inválida detectada.")
```

Esto es común en:

* APIs
* Librerías
* Frameworks
* Sistemas grandes

Conecta con:

* [[Crear excepciones personalizadas]]
* [[Herencia en Python]]

---

## raise vs print

Mala práctica:

```python
if edad < 0:
    print("Edad inválida")
```

Buena práctica:

```python
if edad < 0:
    raise ValueError("Edad inválida")
```

Diferencia clave:

* `print` informa.
* `raise` obliga a manejar el problema.

El segundo es más profesional.

---

## Flujo mental completo

```text
Error ocurre naturalmente → except lo captura
Error detectado manualmente → raise lo genera
```

`raise` convierte reglas de negocio en errores formales.

---

## Casos donde debes usar raise

Usa `raise` cuando:

* Los parámetros son inválidos.
* Una función recibe datos corruptos.
* Se viola una precondición.
* Un estado interno es inconsistente.
* Quieres que el llamador maneje el problema.

---

## raise y finally

Incluso si lanzas un error manualmente, el bloque [[finally]] se ejecutará antes de que el programa termine.

Esto mantiene coherencia con el modelo general de excepciones.

---

## Mentalidad de ingeniero

`raise` es una herramienta de disciplina.

Un sistema robusto:

* No ignora errores.
* No los oculta.
* Los formaliza.

---
