---
title: join()
description: Método join() del tipo str para unir elementos de una lista en una sola cadena en Python.
tags: [Python, str, métodos, list, procesamiento de texto]
date: 2026-02-28
---

# join()

El método `join()` une los elementos de una [[list]] (u otro iterable) en una sola cadena.  
Pertenece al tipo [[str]].  

Es el “opuesto” de [[split()]].

---

## Analogía mental

Si [[split()]] es unas tijeras que cortan una frase,  
`join()` es el pegamento que vuelve a unir las piezas.

---

## Sintaxis

```python
"separador".join(iterable)
````

* El separador es la cadena que se colocará entre los elementos.
* El iterable suele ser una lista de strings.
* Devuelve una nueva cadena.

---

## Ejemplo básico

```python id="p4x9mz"
palabras = ["Python", "es", "potente"]

resultado = " ".join(palabras)
print(resultado)
```

Resultado:

```text id="q7t2lw"
Python es potente
```

---

## Usando otro separador

```python id="v3k8rn"
datos = ["2026", "02", "23"]

print("-".join(datos))
```

Resultado:

```text id="m1z6px"
2026-02-23
```

---

## Sin separador

```python id="t8q4vs"
letras = ["P", "Y", "T", "H", "O", "N"]

print("".join(letras))
```

Resultado:

```text id="c5n9wy"
PYTHON
```

---

## Error común

`join()` solo funciona con cadenas.

```python id="r2m7kd"
numeros = [1, 2, 3]

print(",".join(numeros))
```

Resultado:

```text id="x4p8jt"
TypeError: sequence item 0: expected str instance, int found
```

---

## Solución: convertir a string

```python id="z6v1qh"
numeros = [1, 2, 3]

numeros_str = [str(n) for n in numeros]

print(",".join(numeros_str))
```

Resultado:

```text id="w9k3mx"
1,2,3
```

---

## Uso práctico

Muy importante para:

* Crear CSV
* Formatear datos
* Generar logs
* Construir comandos
* Reconstruir texto después de usar [[split()]]

Ejemplo combinado:

```python id="y5t2nr"
texto = "Python es potente"

palabras = texto.split()
resultado = "-".join(palabras)

print(resultado)
```

Resultado:

```text id="k8m4pz"
Python-es-potente
```

---

## Importante

`join()` no modifica la lista original.

```python id="n3q7vx"
palabras = ["Hola", "mundo"]

" ".join(palabras)

print(palabras)
```

Resultado:

```text id="d6t1kw"
['Hola', 'mundo']
```

---

## Resumen mental

* `" ".join(lista)` → une con espacios
* `",".join(lista)` → une con comas
* `"".join(lista)` → une sin separador
* Solo funciona con strings

---

## Conecta con

* [[split()]]
* [[str]]
* [[list]]
* [[Métodos de cadenas]]
* [[Conversión de tipos]]

---