---
title: "Objetos"
description: "Concepto de objetos en Programación Orientada a Objetos (POO) y su relación con clases en Python."
tags: ["Python", "POO", "Objetos", "Clases"]
date: 2026-03-02
---

# Objetos

Un **objeto** es una instancia de una clase.

Si la clase es el plano,  
el objeto es la construcción real basada en ese plano.

Conecta con:
- [[Clases]]
- [[Encapsulación]]
- [[Herencia en Python]]
- [[Polimorfismo]]

---

## Definición técnica

Un objeto combina:

- **Estado** → datos (atributos)
- **Comportamiento** → acciones (métodos)
- **Identidad** → referencia única en memoria

---

## Ejemplo básico

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        print(f"Hola, soy {self.nombre}")
````

Crear objetos:

```python
persona1 = Persona("Ana", 25)
persona2 = Persona("Luis", 30)
```

Aquí:

* `persona1` y `persona2` son objetos.
* Ambos pertenecen a la clase `Persona`.
* Cada uno tiene su propio estado.

---

## Estado (atributos)

Cada objeto guarda información propia:

```python
print(persona1.nombre)  # Ana
print(persona2.nombre)  # Luis
```

Aunque provienen de la misma clase, sus datos son independientes.

---

## Comportamiento (métodos)

Los objetos pueden ejecutar acciones:

```python
persona1.saludar()
persona2.saludar()
```

Salida:

```text
Hola, soy Ana
Hola, soy Luis
```

El comportamiento es el mismo, pero el estado cambia.

---

## Identidad en memoria

Cada objeto ocupa un espacio distinto en memoria:

```python
print(persona1 is persona2)  # False
```

Aunque sean del mismo tipo, son entidades diferentes.

---

## Visualización conceptual

```text
Clase Persona
 ├── persona1 → nombre: Ana, edad: 25
 └── persona2 → nombre: Luis, edad: 30
```

La clase define la estructura.
Los objetos contienen los datos reales.

---

## Objetos en todo Python

En Python, **todo es un objeto**:

* Números
* Strings
* Listas
* Funciones
* Clases

Ejemplo:

```python
print(type(5))
print(type("hola"))
print(type([1, 2, 3]))
```

Todo responde como objeto.

---

## Objetos y encapsulación

Los objetos permiten:

* Proteger datos internos
* Controlar cómo se modifican
* Aplicar reglas dentro de métodos

Ejemplo:

```python
class Cuenta:
    def __init__(self, saldo):
        self.saldo = saldo

    def retirar(self, cantidad):
        if cantidad > self.saldo:
            raise ValueError("Fondos insuficientes.")
        self.saldo -= cantidad
```

Aquí el objeto controla su propio estado.

---

## Diferencia clave

* Clase → definición.
* Objeto → instancia concreta con datos reales.

Sin objetos, las clases no tienen vida.

---

## Múltiples objetos, mismo molde

```python
cuenta1 = Cuenta(100)
cuenta2 = Cuenta(500)
```

Ambas son cuentas,
pero cada una mantiene su propio saldo.

---

## Mentalidad orientada a objetos

Pensar en objetos significa preguntarse:

* ¿Qué entidades existen en mi sistema?
* ¿Qué datos poseen?
* ¿Qué pueden hacer?

Es modelar el problema como un conjunto de entidades que interactúan.

---

