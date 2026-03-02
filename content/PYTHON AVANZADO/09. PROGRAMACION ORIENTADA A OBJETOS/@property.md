---
title: "@property"
description: "Decorador que permite definir métodos que se comportan como atributos, facilitando encapsulación y control sobre el acceso a datos."
tags: ["Python", "POO", "Clases", "Objetos", "Métodos", "Encapsulación", "Property"]
date: 2026-03-02
---

# @property

El decorador **@property** en Python permite **convertir un método en un atributo calculado**, controlando el acceso a los datos de manera segura y manteniendo la sintaxis limpia.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Atributos]]
- [[Métodos]]
- [[Encapsulación]]
- [[Herencia]]
- [[Polimorfismo]]
- [[init]]

---

## Concepto clave

- Permite **acceder a métodos como si fueran atributos**.
- Facilita la **encapsulación**, controlando lectura, escritura y eliminación de atributos.
- Evita el acceso directo a atributos privados, respetando buenas prácticas de OOP.

---

## Sintaxis básica

```python id="prop1"
class Persona:
    def __init__(self, nombre, edad):
        self._nombre = nombre  # atributo privado por convención
        self._edad = edad

    @property
    def nombre(self):
        return self._nombre

    @property
    def edad(self):
        return self._edad
````

```python id="prop2"
p = Persona("Ana", 25)
print(p.nombre)  # Ana
print(p.edad)    # 25
```

**Nota:**

* Aunque `nombre` y `edad` son métodos, se acceden como atributos.

---

## Modificación de atributos con setter

```python id="prop3"
class Persona:
    def __init__(self, nombre, edad):
        self._nombre = nombre
        self._edad = edad

    @property
    def edad(self):
        return self._edad

    @edad.setter
    def edad(self, nuevo_valor):
        if nuevo_valor < 0:
            raise ValueError("La edad no puede ser negativa")
        self._edad = nuevo_valor
```

```python id="prop4"
p = Persona("Luis", 30)
p.edad = 35
print(p.edad)  # 35

# p.edad = -5  # ValueError: La edad no puede ser negativa
```

* `@edad.setter` permite definir la lógica de asignación del atributo.
* Esto protege los datos y mantiene la consistencia.

---

## Eliminación de atributos con deleter

```python id="prop5"
class Persona:
    def __init__(self, nombre):
        self._nombre = nombre

    @property
    def nombre(self):
        return self._nombre

    @nombre.deleter
    def nombre(self):
        print("Borrando nombre...")
        del self._nombre

p = Persona("Ana")
del p.nombre  # Borrando nombre...
```

---

## Analogía mental

* Imagina que un **atributo privado** es como una caja fuerte.
* `@property` es la **ventana con control**, que te permite mirar o cambiar lo que hay dentro de manera segura, sin abrir la caja directamente.

---

## Buenas prácticas

✔ Usa `@property` para controlar acceso a atributos sensibles.
✔ Mantén atributos internos con `_` para indicar privacidad.
✔ Agrega validaciones en setters para proteger los datos.
✔ Evita sobrecargar la lógica dentro del getter; su función principal debe ser **proporcionar acceso seguro**.

---

## Idea clave final

**@property** permite que los métodos se comporten como atributos, combinando **encapsulación, seguridad y sintaxis limpia**, y es una herramienta central para una OOP profesional y mantenible.

