---
title: "Herencia"
description: "Principio de POO que permite que una clase (subclase) herede atributos y métodos de otra (superclase), facilitando la reutilización de código."
tags: ["Python", "POO", "Clases", "Herencia", "Objetos", "Métodos"]
date: 2026-03-02
---

# Herencia

La **herencia** es un principio de la Programación Orientada a Objetos que permite a una clase **heredar atributos y métodos de otra clase**. Esto promueve la **reutilización de código** y facilita la creación de jerarquías de clases.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Atributos]]
- [[Métodos]]
- [[Encapsulación]]
- [[init]]
- [[Métodos especiales (str, repr)]]

---

## Conceptos clave

- **Superclase (clase base)**: clase que provee atributos y métodos.
- **Subclase (clase derivada)**: clase que hereda de la superclase y puede:
  - Usar los métodos y atributos heredados.
  - Sobrescribir métodos (override) para modificar comportamiento.
  - Añadir nuevos atributos y métodos propios.

---

## Sintaxis básica

```python id="her1"
class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

    def hablar(self):
        return "Sonido genérico"

# Subclase
class Perro(Animal):
    def hablar(self):
        return "Guau!"

class Gato(Animal):
    def hablar(self):
        return "Miau!"
````

---

## Uso de la herencia

```python id="her2"
perro = Perro("Rex")
gato = Gato("Luna")

print(perro.nombre, "dice:", perro.hablar())  # Rex dice: Guau!
print(gato.nombre, "dice:", gato.hablar())    # Luna dice: Miau!
```

Salida:

```text id="her3"
Rex dice: Guau!
Luna dice: Miau!
```

---

## Llamada al constructor de la superclase

Se puede llamar explícitamente al constructor de la clase base usando `super()`:

```python id="her4"
class Perro(Animal):
    def __init__(self, nombre, raza):
        super().__init__(nombre)  # llama al constructor de Animal
        self.raza = raza

    def hablar(self):
        return "Guau!"
```

```python id="her5"
p = Perro("Max", "Labrador")
print(p.nombre)  # Max
print(p.raza)    # Labrador
print(p.hablar())# Guau!
```

---

## Analogía mental

* Imagina **herencia** como un árbol genealógico:

  * La **superclase** es el ancestro.
  * La **subclase** hereda características (atributos y métodos) del ancestro.
  * Puede añadir sus propios rasgos y comportamientos.

---

## Buenas prácticas

✔ Usa herencia solo cuando exista una relación "es un/una" (is-a) entre clases.
✔ Prefiere composición cuando sea más apropiado que heredar.
✔ Sobrescribe métodos (`override`) con cuidado para mantener consistencia.
✔ Siempre llama a `super().__init__()` en subclases que añadan atributos propios.

---

## Idea clave final

La herencia permite **extender y reutilizar clases existentes**, evitando duplicación de código y creando jerarquías claras y mantenibles.
