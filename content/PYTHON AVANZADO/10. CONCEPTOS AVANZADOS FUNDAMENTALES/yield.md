---
title: "yield"
description: "Palabra clave de Python usada en generadores para producir valores uno a uno, permitiendo reanudar la función desde donde se quedó."
tags: ["Python", "POO", "Generadores", "Iteradores", "Avanzado"]
date: 2026-03-02
---

# yield

En Python, `yield` es la palabra clave que convierte una función normal en un **generador**.  
Permite **producir un valor**, **pausar la función**, y **reanudarla más tarde**, recordando el estado de todas sus variables locales.

Conecta con:
- [[Generadores]]
- [[Iteradores]]
- [[Funciones]]
- [[List Comprehension]]

---

## Concepto clave

- `yield` devuelve un valor al llamador sin finalizar la función.  
- Cada vez que se llama `next()` sobre el generador, la función continúa **justo después del último `yield`**.  
- Cuando la función termina, automáticamente lanza `StopIteration`.

---

## Ejemplo básico

```python
def numeros():
    yield 1
    yield 2
    yield 3

gen = numeros()

print(next(gen))
print(next(gen))
print(next(gen))
````

**Salida:**

```text
1
2
3
```

---

## Reanudar la función

```python
def contar_hasta(n):
    contador = 0
    while contador < n:
        yield contador
        contador += 1

gen = contar_hasta(3)

print(next(gen))  # 0
print(next(gen))  # 1
print(next(gen))  # 2
```

* Notar que la variable `contador` **mantiene su estado** entre llamadas a `next()`.

---

## Uso en bucles for

```python
for num in contar_hasta(5):
    print(num)
```

**Salida:**

```text
0
1
2
3
4
```

* No se necesita llamar a `next()` manualmente; el `for` consume el generador automáticamente.

---

## Diferencia con return

* `return` **termina la función** y devuelve un valor único.
* `yield` **pausa la función** y devuelve un valor **temporalmente**, permitiendo seguir produciendo más valores.

```python
def demo():
    yield 10
    return 20  # Esto termina la función
```

* El `return` en un generador puede ser capturado solo con manejo avanzado de `StopIteration`:

```python
gen = demo()
print(next(gen))  # 10
# next(gen)  # StopIteration: 20
```

---

## Analogía mental

* `yield` es como **entregar un producto a un cliente y recordar dónde quedaste** para poder entregar el siguiente cuando se pida:

  * Cada llamada a `next()` es como un nuevo pedido.
  * La función no se olvida de su estado.
  * Cuando no hay más productos, termina (`StopIteration`).

---

## Buenas prácticas

✔ Usa `yield` para secuencias grandes o infinitas.
✔ Combina generadores con expresiones generadoras `(x*x for x in range(n))` para eficiencia de memoria.
✔ Documenta claramente el orden y tipo de valores que produce.
✔ Evita modificar variables globales dentro de generadores si no es necesario.

---

## Idea clave final

`yield` es la **herramienta principal de Python para crear iteradores bajo demanda**, permitiendo **procesar grandes volúmenes de datos de manera eficiente** sin consumir memoria innecesariamente.
