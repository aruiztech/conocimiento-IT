---
title: "Generadores"
description: "Funciones especiales que devuelven un iterador y generan valores bajo demanda usando 'yield', permitiendo manejo eficiente de memoria."
tags: ["Python", "POO", "Iteradores", "Generadores", "Memoria", "Avanzado"]
date: 2026-03-02
---

# Generadores

Los **generadores** son funciones que permiten **producir valores uno a uno bajo demanda** en lugar de generar toda la colección en memoria. Se usan cuando necesitamos **recorrer grandes cantidades de datos** o pipelines de datos de manera eficiente.

Conecta con:
- [[Iteradores]]
- [[Funciones]]
- [[List Comprehension]]
- [[Bucles for]]

---

## Concepto clave

- Se definen como funciones normales pero usan la palabra clave `yield` en lugar de `return`.  
- Cada vez que se llama `next()` sobre un generador, la ejecución se **reanuda desde donde se quedó**, hasta llegar a otro `yield` o finalizar.  
- Son **iteradores**, por lo que podemos usarlos en bucles `for` directamente.

---

## Sintaxis básica

```python
def generador_simple():
    yield 1
    yield 2
    yield 3

gen = generador_simple()

print(next(gen))
print(next(gen))
print(next(gen))
````

**Salida:**

```text id="gen1-output"
1
2
3
```

* Si llamamos otra vez a `next(gen)` se lanza `StopIteration`.

---

## Uso en un bucle for

```python
def cuadrados(n):
    for i in range(n):
        yield i ** 2

for valor in cuadrados(4):
    print(valor)
```

**Salida:**

```text id="gen2-output"
0
1
4
9
```

* Notar que **no se crea una lista completa**, solo se genera cada valor cuando se necesita.

---

## Generadores con expresión (similar a List Comprehension)

```python
gen_expr = (x ** 2 for x in range(5))

for n in gen_expr:
    print(n)
```

**Salida:**

```text id="gen3-output"
0
1
4
9
16
```

* Las expresiones generadoras son **más ligeras que las listas por comprensión** porque no almacenan todos los valores en memoria.

---

## Analogía mental

* Un generador es como una **fábrica que produce un producto a pedido**:

  * No fabricas todo el inventario de golpe.
  * Cada vez que el cliente pide un producto (`next()`), la fábrica lo produce y recuerda dónde se quedó.
  * Cuando no hay más productos, la fábrica cierra (`StopIteration`).

---

## Buenas prácticas

✔ Usa generadores para secuencias grandes o infinitas.
✔ Combínalos con funciones de Python como `sum()`, `max()` o `list()` para procesar datos de manera eficiente.
✔ Evita almacenar grandes listas si solo necesitas iterar una vez.
✔ Documenta claramente qué produce el generador y en qué orden.

---

## Idea clave final

Los **generadores** son una forma eficiente y elegante de crear iteradores en Python, fundamentales para **trabajar con streams de datos, pipelines y grandes volúmenes de información** sin saturar la memoria.
