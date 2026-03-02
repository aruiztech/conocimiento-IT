---
title: "else en excepciones"
description: "Uso del bloque else junto a try y except para ejecutar código solo cuando no ocurre ninguna excepción."
tags: ["Python", "Excepciones", "Control de flujo"]
date: 2026-03-02
---

# else en excepciones

El bloque `else` en manejo de excepciones se ejecuta **solo si NO ocurre ninguna excepción dentro del bloque `try`**.

Forma parte del sistema completo de manejo de errores en Python:

- [[Errores comunes]]
- [[Traceback]]
- [[try y except]]
- [[finally]]
- [[raise]]

---

## Estructura general

```python
try:
    # Código que puede generar error
except TipoDeError:
    # Se ejecuta si ocurre ese error
else:
    # Se ejecuta si NO ocurrió ningún error
finally:
    # Se ejecuta siempre (opcional)
````

---

## ¿Por qué existe else?

Porque separa claramente:

* Código que puede fallar
* Código que depende de que todo haya salido bien

Esto mejora:

* Legibilidad
* Organización
* Mentalidad profesional

---

## Ejemplo básico

```python
try:
    numero = int(input("Introduce un número: "))
except ValueError:
    print("Entrada inválida.")
else:
    print("El doble es:", numero * 2)
```

### Caso 1 — Usuario escribe `hola`

```text
Entrada inválida.
```

### Caso 2 — Usuario escribe `5`

```text
El doble es: 10
```

Observa que el `else` solo se ejecuta si no hubo excepción.

---

## Analogía mental

Imagina un examen:

* `try` → Haces el examen.
* `except` → Si suspendes, repites.
* `else` → Si apruebas, pasas al siguiente nivel.

El `else` representa el flujo normal cuando todo sale bien.

---

## Ejemplo más realista

```python
try:
    archivo = open("datos.txt")
except FileNotFoundError:
    print("El archivo no existe.")
else:
    contenido = archivo.read()
    print("Contenido:", contenido)
    archivo.close()
```

Aquí:

* Si el archivo no existe → se maneja el error.
* Si el archivo sí existe → el `else` gestiona el flujo normal.

Conecta con:

* [[Manejo de archivos]]
* [[Errores comunes]]

---

## ¿Por qué no poner todo dentro de try?

Mala práctica:

```python
try:
    numero = int(input("Número: "))
    print(numero * 2)
except ValueError:
    print("Error.")
```

Esto funciona.

Pero si agregas más lógica después, puedes capturar errores que no quieres capturar.

Buena práctica:

```python
try:
    numero = int(input("Número: "))
except ValueError:
    print("Error.")
else:
    print(numero * 2)
```

Ahora:

* Solo protegemos lo que puede fallar.
* El resto del código queda limpio.

---

## Regla profesional

El bloque `try` debe ser lo más pequeño posible.

El `else` permite mantener:

* Claridad
* Separación de responsabilidades
* Código más mantenible

---

## Flujo visual completo

```text
try → ocurre error → except
try → no ocurre error → else
siempre → finally (si existe)
```

---

## Caso combinado con múltiples excepciones

```python
try:
    numero = int(input("Número: "))
    resultado = 10 / numero
except ValueError:
    print("No es un número.")
except ZeroDivisionError:
    print("No puedes dividir entre cero.")
else:
    print("Resultado:", resultado)
```

Aquí:

* Si todo sale bien → se ejecuta `else`.
* Si hay error → se ejecuta el `except` correspondiente.
* El `else` nunca se ejecuta si hubo excepción.

Conecta con:

* [[ValueError]]
* [[ZeroDivisionError]]
* [[try y except]]

---

## Error común conceptual

Muchos principiantes creen que `else` es obligatorio.

No lo es.

Se usa cuando quieres separar claramente:

* Manejo de error
* Flujo normal

---

## Cuándo usar else

Usa `else` cuando:

* Hay código que depende de que el `try` haya funcionado.
* Quieres que el bloque protegido sea mínimo.
* Buscas claridad estructural.

No lo uses si el código es trivial o muy pequeño.

---

## Mentalidad de ingeniero

`else` no es solo sintaxis.

Es estructura mental:

* Manejar lo inesperado.
* Separar lo normal de lo excepcional.
* Escribir código limpio.

---

## Próximas notas relacionadas

* [[finally]]
* [[raise]]
* [[Crear excepciones personalizadas]]

---
