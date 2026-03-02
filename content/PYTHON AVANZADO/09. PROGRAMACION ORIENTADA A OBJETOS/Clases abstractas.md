---
title: "Clases abstractas"
description: "Clases que no pueden ser instanciadas directamente y que sirven como plantilla para otras clases, garantizando que ciertos métodos se implementen."
tags: ["Python", "POO", "Clases", "Objetos", "Herencia", "Polimorfismo", "ABC"]
date: 2026-03-02
---

# Clases abstractas

Las **clases abstractas** son clases que **no pueden ser instanciadas directamente**. Sirven como **plantillas** para otras clases, asegurando que ciertos métodos o atributos sean implementados en las subclases.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Herencia]]
- [[Polimorfismo]]
- [[Métodos]]
- [[@property]]

---

## Concepto clave

- Una clase abstracta **define la interfaz**, pero no necesariamente la implementación completa.  
- Obliga a las subclases a implementar ciertos métodos, garantizando consistencia en la jerarquía de clases.  
- En Python se implementa usando el módulo `abc` (`Abstract Base Classes`).

---

## Sintaxis básica

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def hablar(self):
        pass

    @abstractmethod
    def moverse(self):
        pass
````

**Explicación:**

* `Animal` es una clase abstracta (hereda de `ABC`).
* Los métodos `hablar` y `moverse` son abstractos y **deben implementarse en cualquier subclase**.

---

## Implementación en subclases

```python
class Perro(Animal):
    def hablar(self):
        return "Guau!"

    def moverse(self):
        return "Corre en cuatro patas"

class Pez(Animal):
    def hablar(self):
        return "Blub"

    def moverse(self):
        return "Nada en el agua"

perro = Perro()
pez = Pez()

print(perro.hablar())
print(perro.moverse())
print(pez.hablar())
print(pez.moverse())
```

**Salida:**

```
Guau!
Corre en cuatro patas
Blub
Nada en el agua
```

* Si intentamos instanciar `Animal()` directamente, Python lanzará un **TypeError**:

```python
# animal = Animal()
```

**Salida:**

```
TypeError: Can't instantiate abstract class Animal with abstract methods hablar, moverse
```

---

## Analogía mental

* Una clase abstracta es como un **contrato** o **manual de instrucciones**:

  * Define qué métodos **deben existir** en cualquier objeto que siga ese contrato.
  * No te da la herramienta, solo te dice qué necesitas construir.
  * Las subclases son los fabricantes que cumplen el contrato construyendo los métodos.

---

## Buenas prácticas

✔ Usa clases abstractas para definir interfaces claras y consistentes.
✔ Combínalas con polimorfismo para crear jerarquías flexibles.
✔ No agregues demasiada lógica en clases abstractas; su objetivo principal es **forzar la implementación de métodos**.
✔ Documenta bien qué métodos deben implementar las subclases.

---

## Idea clave final

Las **clases abstractas** son una herramienta poderosa en Python para garantizar que las subclases cumplan con una interfaz definida, aumentando la consistencia y seguridad de tus jerarquías de objetos.
