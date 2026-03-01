---
title: upper()
description: Método upper() del tipo str para convertir texto a mayúsculas en Python.
tags: [Python, str, métodos, cadenas]
date: 2026-02-28
---

# upper()

El método `upper()` convierte todos los caracteres de una cadena a **MAYÚSCULAS**.

Pertenece al tipo de dato [[str]].

---

## Analogía mental

Imagina que tienes un texto normal:

"python es potente"

`upper()` es como activar el botón de:  
"GRITAR TODO"

---

## Sintaxis

```python
cadena.upper()
````

Devuelve una **nueva cadena** en mayúsculas.

Recuerda: las cadenas son [[Mutabilidad vs inmutabilidad|inmutables]].

---

## Ejemplo básico

```python id="k2x9fa"
texto = "python"
print(texto.upper())
```

Resultado:

```text id="n8m3qd"
PYTHON
```

---

## No modifica la cadena original

```python id="q7r1mv"
texto = "python"

nuevo = texto.upper()

print(texto)
print(nuevo)
```

Resultado:

```text id="p5t8lx"
python
PYTHON
```

La variable original permanece igual.

---

## Uso práctico: destacar mensajes

```python id="z1c4we"
mensaje = "error crítico"
print(mensaje.upper())
```

Resultado:

```text id="b6y2hs"
ERROR CRÍTICO
```

Muy útil para:

* Alertas
* Logs
* Mensajes importantes

---

## Combinado con input()

```python id="u9v3nk"
respuesta = input("Escribe OK para continuar: ")

if respuesta.upper() == "OK":
    print("Continuando...")
```

Permite aceptar:

* ok
* Ok
* oK
* OK

---

## upper() con números y símbolos

```python id="m3x8rt"
texto = "python123!"
print(texto.upper())
```

Resultado:

```text id="d4k7pw"
PYTHON123!
```

Solo afecta letras, no números ni símbolos.

---

## ¿Por qué es importante?

En programación y ciberseguridad se usa para:

* Normalizar datos
* Comparar credenciales
* Estandarizar entradas
* Mostrar mensajes críticos

---

## Comparación rápida

* [[lower()]] → todo en minúsculas
* [[upper()]] → todo en mayúsculas
* [[capitalize()]] → primera letra mayúscula
* [[title()]] → cada palabra con mayúscula

---

## Conecta con

* [[str]]
* [[Métodos de cadenas]]
* [[lower()]]
* [[Entrada de usuario input()]]

---
