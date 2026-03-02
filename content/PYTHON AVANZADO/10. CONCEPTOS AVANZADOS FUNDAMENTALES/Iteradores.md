---
title: "Iteradores"
description: "Objetos en Python que permiten recorrer elementos de una colección de forma secuencial sin exponer su estructura interna."
tags: ["Python", "POO", "Iteradores", "Colecciones", "Avanzado"]
date: 2026-03-02
---

# Iteradores

En Python, un **iterador** es un objeto que nos permite recorrer elementos de una colección (**listas, tuplas, diccionarios, sets**) de manera **secuencial**, sin necesidad de conocer la estructura interna del contenedor.

Conecta con:
- [[Generadores]]
- [[Funciones]]
- [[List Comprehension]]
- [[Bucles for]]

---

## Concepto clave

- Un iterador mantiene un **estado interno**, indicando **el siguiente elemento** que debe devolver.  
- Todo objeto iterable (`list`, `tuple`, `dict`, `set`, `str`) puede ser convertido en iterador con `iter()`.  
- Se recorre usando `next()` hasta que se alcanza el final, donde lanza `StopIteration`.

---

## Sintaxis básica

```python
numeros = [1, 2, 3]
iterador = iter(numeros)

print(next(iterador))
print(next(iterador))
print(next(iterador))
````

**Salida:**

```text
1
2
3
```

* Si llamamos a `next(iterador)` otra vez, se lanza:

```python
# next(iterador)  # StopIteration
```

**Salida:**

```text
StopIteration
```

---

## Iterando en un bucle for

El `for` en Python usa **internamente iteradores**, por lo que no necesitamos llamar a `next()` manualmente:

```python
frutas = ["manzana", "banana", "cereza"]

for fruta in frutas:
    print(fruta)
```

**Salida:**

```text
manzana
banana
cereza
```

---

## Creando un iterador personalizado

Podemos crear nuestra propia clase que implemente el **protocolo de iterador** (`__iter__` y `__next__`):

```python
class Contador:
    def __init__(self, limite):
        self.limite = limite
        self.actual = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.actual < self.limite:
            valor = self.actual
            self.actual += 1
            return valor
        else:
            raise StopIteration

contador = Contador(3)

for numero in contador:
    print(numero)
```

**Salida:**

```text
0
1
2
```

---

## Analogía mental

* Un iterador es como un **marcador de página** en un libro:

  * No necesitas leer todo el libro para saber dónde estás.
  * Cada vez que pides el siguiente elemento, el marcador avanza.
  * Cuando llegas al final del libro, no hay más páginas (StopIteration).

---

## Buenas prácticas

✔ Usa iteradores para recorrer grandes colecciones sin cargar todo en memoria.
✔ Combina iteradores con **generadores** para crear pipelines de datos eficientes.
✔ Evita modificar la colección mientras iteras, puede causar resultados inesperados.

---

## Idea clave final

Los **iteradores** permiten recorrer datos de manera controlada y eficiente, formando la base para técnicas avanzadas de Python como **generadores**, **decoradores**, y **manipulación de streams**.
