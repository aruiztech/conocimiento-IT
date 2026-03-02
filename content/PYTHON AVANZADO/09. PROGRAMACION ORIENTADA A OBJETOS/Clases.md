---
title: "Clases"
description: "Concepto y uso de clases en Programación Orientada a Objetos (POO) en Python."
tags: ["Python", "POO", "Clases", "Objetos"]
date: 2026-03-02
---

# Clases

Una **clase** es una plantilla para crear objetos.

En Programación Orientada a Objetos (POO), las clases permiten:

- Agrupar datos (atributos)
- Definir comportamientos (métodos)
- Modelar entidades del mundo real o lógico

---

## ¿Qué es un objeto?

Un objeto es una **instancia de una clase**.

Analogía:

- Clase → Plano de una casa.
- Objeto → Casa construida a partir del plano.

---

## Sintaxis básica

```python
class NombreDeClase:
    pass
````

Ejemplo:

```python
class Persona:
    pass
```

Aquí hemos creado una clase vacía.

---

## Crear un objeto (instancia)

```python
persona1 = Persona()
```

Ahora `persona1` es un objeto de tipo `Persona`.

---

## Constructor: **init**

El método especial `__init__` se ejecuta cuando creas una instancia.

Sirve para inicializar atributos.

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
```

Crear objeto:

```python
persona1 = Persona("Ana", 25)
```

---

## ¿Qué es self?

`self` representa la instancia actual.

Permite que cada objeto tenga sus propios datos.

```python
print(persona1.nombre)  # Ana
print(persona1.edad)    # 25
```

---

## Métodos

Los métodos son funciones definidas dentro de una clase.

```python
class Persona:
    def __init__(self, nombre):
        self.nombre = nombre

    def saludar(self):
        print(f"Hola, soy {self.nombre}")
```

Uso:

```python
persona1 = Persona("Carlos")
persona1.saludar()
```

Salida:

```text
Hola, soy Carlos
```

---

## Atributos vs Métodos

* Atributos → Datos del objeto.
* Métodos → Comportamientos del objeto.

Ejemplo conceptual:

```text
Clase: Coche

Atributos:
- marca
- color
- velocidad

Métodos:
- acelerar()
- frenar()
- girar()
```

---

## Múltiples objetos

Cada instancia tiene su propio estado:

```python
persona1 = Persona("Ana")
persona2 = Persona("Luis")

print(persona1.nombre)  # Ana
print(persona2.nombre)  # Luis
```

---

## Buenas prácticas

✔ Nombres de clases en PascalCase.
✔ Métodos y atributos en snake_case.
✔ Cada clase debe representar una entidad clara.
✔ Evita clases gigantes con demasiadas responsabilidades.

---

## Clases y encapsulación

Las clases permiten controlar cómo se accede a los datos.

Esto se relaciona con:

* [[Encapsulación]]
* [[Herencia en Python]]
* [[Polimorfismo]]
* [[Métodos especiales]]

---

## Ejemplo más completo

```python
class CuentaBancaria:
    def __init__(self, titular, saldo=0):
        self.titular = titular
        self.saldo = saldo

    def depositar(self, cantidad):
        self.saldo += cantidad

    def retirar(self, cantidad):
        if cantidad > self.saldo:
            raise ValueError("Fondos insuficientes.")
        self.saldo -= cantidad
```

Uso:

```python
cuenta = CuentaBancaria("Ana", 100)
cuenta.depositar(50)
cuenta.retirar(30)

print(cuenta.saldo)  # 120
```

Aquí la clase modela una entidad real con reglas.

---

## Mentalidad de diseño

Las clases no son solo sintaxis.

Son una forma de pensar:

* ¿Qué representa mi sistema?
* ¿Qué datos necesita?
* ¿Qué comportamientos debe tener?

Diseñar bien las clases es diseñar bien el sistema.

---

