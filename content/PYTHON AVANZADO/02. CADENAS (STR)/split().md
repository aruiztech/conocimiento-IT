---
title: split()
description: Método split() del tipo str para dividir cadenas en listas en Python.
tags: [Python, str, métodos, list, procesamiento de texto]
date: 2026-02-28
---

# split()

El método `split()` divide una cadena en varias partes y devuelve una [[list]].  
Es uno de los métodos más usados para procesar texto.  
Pertenece al tipo [[str]].

---

## Analogía mental

Imagina que tienes una frase escrita en papel.  
`split()` es como usar unas tijeras para cortarla en partes según un separador.

---

## Sintaxis básica

```python
cadena.split(separador)
````

* Si no se indica separador, divide por espacios.
* Devuelve una lista.

---

## Ejemplo sin separador

```python id="k4t9px"
texto = "Python es muy potente"

resultado = texto.split()
print(resultado)
```

Resultado:

```text id="z7m2qw"
['Python', 'es', 'muy', 'potente']
```

Divide automáticamente por espacios.

---

## Ejemplo con separador personalizado

```python id="n3v8ly"
datos = "uno,dos,tres"

resultado = datos.split(",")
print(resultado)
```

Resultado:

```text id="q6r1hb"
['uno', 'dos', 'tres']
```

---

## Separador diferente

```python id="p9x4ts"
fecha = "2026-02-23"

print(fecha.split("-"))
```

Resultado:

```text id="w2k7mz"
['2026', '02', '23']
```

Muy útil para procesar fechas.

---

## Limitar el número de divisiones

Puedes usar un segundo argumento:

```python id="t5m1vd"
texto = "uno dos tres cuatro"

print(texto.split(" ", 1))
```

Resultado:

```text id="c8q3lx"
['uno', 'dos tres cuatro']
```

El `1` indica el número máximo de cortes.

---

## Usar split() con input()

```python id="y7p2kr"
datos = input("Introduce nombre y edad: ")

partes = datos.split()
print(partes)
```

Si el usuario escribe:

```
Angel 34
```

Resultado:

```text id="m4z9tw"
['Angel', '34']
```

---

## Uso en ciberseguridad

`split()` es muy importante para:

* Analizar logs
* Procesar líneas de archivos
* Extraer datos separados por comas (CSV)
* Separar comandos
* Parsear respuestas de red

---

## Importante

`split()` no modifica la cadena original
(devuelve una nueva lista).

```python id="v1k6qs"
texto = "Hola mundo"
texto.split()

print(texto)
```

Resultado:

```text id="d3x8pn"
Hola mundo
```

---

## Relación con otros métodos

* [[join()]] → Une una lista en una cadena
* [[strip()]] → Limpia espacios antes de dividir
* [[Métodos de cadenas]]
* [[list]]

---