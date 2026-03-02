---
title: "Polimorfismo"
description: "Principio de POO que permite que distintos objetos respondan de manera diferente al mismo método o interfaz, facilitando flexibilidad y abstracción."
tags: ["Python", "POO", "Clases", "Objetos", "Métodos", "Herencia", "Polimorfismo"]
date: 2026-03-02
---

# Polimorfismo

El **polimorfismo** es un principio de la Programación Orientada a Objetos que permite que **objetos de distintas clases puedan ser tratados de manera uniforme**, respondiendo de forma diferente al mismo método o interfaz.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Métodos]]
- [[Herencia]]
- [[Encapsulación]]
- [[init]]
- [[Métodos especiales (str, repr)]]

---

## Concepto clave

- Significa literalmente "muchas formas".
- Un mismo método puede comportarse diferente según el objeto que lo invoque.
- Permite **escribir código más flexible y genérico**, que funciona con cualquier objeto que cumpla la interfaz esperada.

---

## Ejemplo básico con herencia

```python id="pol1"
class Animal:
    def hablar(self):
        return "Sonido genérico"

class Perro(Animal):
    def hablar(self):
        return "Guau!"

class Gato(Animal):
    def hablar(self):
        return "Miau!"
````

```python id="pol2"
animales = [Perro(), Gato(), Animal()]

for a in animales:
    print(a.hablar())
```

Salida:

```text id="pol3"
Guau!
Miau!
Sonido genérico
```

**Explicación:**

* Aunque llamamos al mismo método `hablar()` para todos los objetos, cada clase lo implementa de manera diferente.
* Esto es polimorfismo en acción.

---

## Polimorfismo con funciones genéricas

```python id="pol4"
def hacer_hablar(animal):
    print(animal.hablar())

hacer_hablar(Perro())  # Guau!
hacer_hablar(Gato())   # Miau!
```

**Ventaja:**

* La función no necesita saber la clase exacta, solo que el objeto tenga el método `hablar()`.

---

## Polimorfismo y métodos especiales

Python también soporta polimorfismo mediante métodos especiales:

```python id="pol5"
class Persona:
    def __str__(self):
        return "Soy una persona"

class Estudiante(Persona):
    def __str__(self):
        return "Soy un estudiante"

print(Persona())    # Soy una persona
print(Estudiante()) # Soy un estudiante
```

* El mismo método `__str__()` tiene comportamientos distintos según el tipo de objeto.

---

## Analogía mental

* Piensa en polimorfismo como un **control remoto universal**:

  * Todos los dispositivos tienen un botón “encender”.
  * Presionas el botón, pero cada dispositivo responde a su manera (TV, radio, luces).
  * El botón es la **misma interfaz**, pero el resultado depende del objeto.

---

## Buenas prácticas

✔ Aplica polimorfismo usando herencia o interfaces comunes.
✔ Prefiere código genérico que funcione con cualquier objeto compatible.
✔ Evita dependencias estrictas de la clase concreta; confía en la interfaz del objeto.

---

## Idea clave final

El polimorfismo **permite tratar distintos objetos de manera uniforme**, aumentando la flexibilidad, reduciendo duplicación de código y promoviendo la programación orientada a interfaces.
