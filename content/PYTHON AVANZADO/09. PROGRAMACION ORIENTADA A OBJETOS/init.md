---
title: "__init__"
description: "El método __init__ en Python, usado para inicializar objetos en Programación Orientada a Objetos."
tags: ["Python", "POO", "Clases", "Objetos", "Atributos", "__init__"]
date: 2026-03-02
---

# __init__

El método `__init__` es el **constructor** de una clase en Python.

Se ejecuta automáticamente al **crear un objeto**.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Atributos]]
- [[Métodos]]
- [[Encapsulación]]

---

## Función del constructor

`__init__` inicializa los atributos del objeto para definir su **estado inicial**.

Ejemplo conceptual:

```text
Clase: Persona
Atributos: nombre, edad
Al crear un objeto, debemos definir estos valores iniciales
````

---

## Sintaxis básica

```python id="init1"
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
```

Crear un objeto:

```python id="init2"
persona1 = Persona("Ana", 25)
print(persona1.nombre)  # Ana
print(persona1.edad)    # 25
```

Aquí `__init__` se ejecuta automáticamente al crear `persona1`.

---

## Analogía mental

Piensa en `__init__` como el **preparador de un objeto**:
Cuando compras un coche nuevo, viene con **estado inicial**: gasolina llena, color rojo, cero km.
`__init__` hace lo mismo para tus objetos en Python.

---

## Parámetros de **init**

Puedes pasar cualquier cantidad de parámetros para inicializar atributos:

```python id="init3"
class Cuenta:
    def __init__(self, titular, saldo_inicial=0):
        self.titular = titular
        self.saldo = saldo_inicial
```

```python id="init4"
cuenta1 = Cuenta("Luis")
cuenta2 = Cuenta("Ana", 100)
print(cuenta1.saldo)  # 0
print(cuenta2.saldo)  # 100
```

---

## Valores por defecto

Los parámetros pueden tener valores por defecto, permitiendo crear objetos sin especificar todos los datos.

---

## Relación con atributos

Todos los atributos de instancia normalmente se definen dentro de `__init__`.

```python id="init5"
self.nombre = nombre
self.edad = edad
```

Esto asegura que cada objeto tenga su propio estado.

---

## Buenas prácticas

✔ Inicializa todos los atributos importantes en `__init__`.
✔ Evita inicializar atributos en otros métodos salvo necesidad.
✔ Usa nombres claros para los parámetros y atributos.
✔ Si usas atributos opcionales, define valores por defecto.

---

## Error común

No incluir `self` como primer parámetro:

```python id="error-init"
class Persona:
    def __init__(nombre, edad):  # ❌ self falta
        self.nombre = nombre
```

Python lanzará un error al crear objetos:

```text
TypeError: __init__() takes 2 positional arguments but 3 were given
```

---

## Idea clave final

`__init__` define **cómo empieza la vida** de un objeto.
Sin él, tus objetos existirían, pero sus atributos no tendrían valores iniciales.

Siempre que crees una clase, piensa:

> ¿Qué necesita saber este objeto al nacer?
