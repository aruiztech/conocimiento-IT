---
title: "finally"
description: "Uso del bloque finally en el manejo de excepciones para ejecutar código que debe ejecutarse siempre."
tags: ["Python", "Excepciones", "Control de flujo", "Recursos"]
date: 2026-03-02
---

# finally

El bloque `finally` se ejecuta **siempre**, haya ocurrido o no una excepción.

Forma parte del sistema completo de manejo de errores en Python:

- [[Errores comunes]]
- [[Traceback]]
- [[try y except]]
- [[else en excepciones]]
- [[raise]]

---

## ¿Para qué sirve finally?

Sirve para ejecutar código que **debe ejecutarse pase lo que pase**, por ejemplo:

- Cerrar archivos
- Cerrar conexiones de red
- Liberar recursos
- Registrar eventos en logs
- Limpiar estados temporales

Es un bloque de **garantía de ejecución**.

---

## Estructura general

```python
try:
    # Código que puede fallar
except TipoDeError:
    # Manejo del error
else:
    # Se ejecuta si no hubo error
finally:
    # Se ejecuta siempre
````

El bloque `finally` es opcional, pero muy importante en código profesional.

---

## Ejemplo básico

```python id="h6k9zp"
try:
    numero = int(input("Número: "))
    resultado = 10 / numero
except ZeroDivisionError:
    print("No puedes dividir entre cero.")
finally:
    print("Operación finalizada.")
```

### Caso 1 — Usuario introduce 0

```text id="k2v8xm"
No puedes dividir entre cero.
Operación finalizada.
```

### Caso 2 — Usuario introduce 5

```text id="p9lqst"
Operación finalizada.
```

Observa que `finally` se ejecuta en ambos casos.

---

## Analogía mental

Imagina un laboratorio químico.

* `try` → Realizas el experimento.
* `except` → Manejas una explosión si ocurre.
* `finally` → Limpias el laboratorio siempre.

La limpieza no depende del resultado del experimento.

---

## Ejemplo real con archivos

```python id="u7md3b"
try:
    archivo = open("datos.txt")
    contenido = archivo.read()
    print(contenido)
except FileNotFoundError:
    print("El archivo no existe.")
finally:
    print("Cerrando proceso.")
```

Problema: si el archivo no se abrió correctamente, `archivo` no existe.

Mejor versión profesional:

```python id="q4hs7r"
archivo = None

try:
    archivo = open("datos.txt")
    contenido = archivo.read()
    print(contenido)
except FileNotFoundError:
    print("El archivo no existe.")
finally:
    if archivo:
        archivo.close()
    print("Proceso terminado.")
```

Conecta con:

* [[Manejo de archivos]]
* [[Context managers]]
* [[Errores comunes]]

---

## finally incluso con return

Un detalle importante:

`finally` se ejecuta incluso si hay un `return`.

```python id="c8ykf2"
def ejemplo():
    try:
        return "Dentro del try"
    finally:
        print("Se ejecuta el finally")

print(ejemplo())
```

Salida:

```text id="y5ntkd"
Se ejecuta el finally
Dentro del try
```

Esto demuestra que `finally` es incondicional.

---

## finally incluso con error no capturado

```python id="b3kz8p"
try:
    10 / 0
finally:
    print("Esto se ejecuta antes de que el programa termine.")
```

Salida:

```text id="r9hv2m"
Esto se ejecuta antes de que el programa termine.
ZeroDivisionError: division by zero
```

El error sigue ocurriendo, pero `finally` se ejecuta antes de que el programa colapse.

---

## Diferencia clara entre bloques

* `except` → Maneja errores.
* `else` → Se ejecuta si no hubo errores.
* `finally` → Se ejecuta siempre.

Visualización mental:

```text id="v2mbqs"
Error ocurre → except → finally
No error → else → finally
Error no capturado → finally → programa termina
```

---

## Caso profesional típico

En automatización o ciberseguridad:

```python
try:
    conexion = conectar_servidor()
    enviar_datos(conexion)
except ConnectionError:
    print("No se pudo conectar.")
finally:
    cerrar_conexion()
```

Aquí `finally` protege la estabilidad del sistema.

Conecta con:

* [[Sockets]]
* [[logging]]
* [[Automatización]]

---

## Buen hábito profesional

Usa `finally` cuando trabajes con:

* Archivos
* Conexiones
* Recursos del sistema
* Bases de datos
* Sesiones

Sin limpieza garantizada, los sistemas reales se vuelven inestables.

---

## Relación con Context Managers

Muchos casos donde usarías `finally` pueden resolverse mejor con:

```python
with open("datos.txt") as archivo:
    contenido = archivo.read()
```

Esto usa internamente un mecanismo equivalente a `try/finally`.

Ver [[Context managers]] para entender cómo funciona.

---

## Mentalidad de ingeniero

`finally` representa responsabilidad.

No solo ejecutas código.

También te aseguras de que el sistema quede en estado correcto.

Eso es mentalidad profesional.

---

## Próximas notas relacionadas

* [[raise]]
* [[Crear excepciones personalizadas]]
* [[Context managers]]

---

## Idea clave final

Si `except` maneja el problema,

`finally` protege la estabilidad del sistema.

