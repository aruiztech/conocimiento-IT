---
title: "Atributos"
description: "Qué son los atributos en Programación Orientada a Objetos y cómo funcionan en Python."
tags: ["Python", "POO", "Atributos", "Clases", "Objetos"]
date: 2026-03-02
---

# Atributos

Los **atributos** son las variables que pertenecen a un objeto o a una clase.

Representan el **estado** de un objeto.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Métodos]]
- [[Encapsulación]]

---

## ¿Qué es el estado?

El estado es la información que un objeto almacena.

Ejemplo conceptual:

```text
Objeto: Coche
Estado:
- marca
- color
- velocidad
````

Cada uno de esos datos es un atributo.

---

## Atributos de instancia

Son los más comunes.
Pertenecen a cada objeto individualmente.

Se definen normalmente dentro de `__init__`.

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
```

Crear objetos:

```python id="atr1"
persona1 = Persona("Ana", 25)
persona2 = Persona("Luis", 30)
```

Cada objeto tiene sus propios atributos:

```python id="atr2"
print(persona1.nombre)  # Ana
print(persona2.nombre)  # Luis
```

Aunque comparten clase, no comparten estado.

---

## Atributos de clase

Pertenecen a la clase y son compartidos por todas las instancias.

```python
class Persona:
    especie = "Humano"  # atributo de clase

    def __init__(self, nombre):
        self.nombre = nombre
```

Uso:

```python id="atr3"
print(Persona.especie)
print(persona1.especie)
```

Todos los objetos acceden al mismo valor.

---

## Diferencia clave

* Atributos de instancia → viven dentro del objeto.
* Atributos de clase → viven en la clase y se comparten.

Visualización:

```text
Clase Persona
 ├── especie = "Humano"
 ├── persona1 → nombre = "Ana"
 └── persona2 → nombre = "Luis"
```

---

## Modificar atributos

```python
persona1.edad = 26
```

Los atributos pueden cambiar (si no se protege su acceso).

---

## Acceso dinámico

También puedes usar:

```python
getattr(persona1, "nombre")
setattr(persona1, "edad", 40)
```

Esto es útil en programación avanzada o metaprogramación.

---

## Buenas prácticas

✔ Define atributos en `__init__`.
✔ No crees atributos inesperados fuera del constructor (salvo casos justificados).
✔ Mantén coherencia en los nombres.
✔ Usa atributos de clase solo cuando el valor sea compartido.

---

## Relación con encapsulación

Aunque puedes acceder directamente:

```python
persona1.nombre
```

En sistemas más grandes se recomienda controlar el acceso mediante:

* Métodos
* Propiedades (`@property`)
* Convenciones como `_atributo`

Conecta con [[Encapsulación]].

---

## Error común

Crear atributos fuera de `__init__` sin intención:

```python
persona1.altura = 170
```

Esto funciona, pero puede romper la coherencia del diseño.

Un diseño sólido define claramente qué atributos existen.

---

## Atributos y memoria

Cada objeto almacena sus atributos en su propio espacio en memoria.

Por eso múltiples objetos pueden coexistir sin interferirse.

---

## Idea clave final

Los atributos definen el estado.

Sin atributos, un objeto no tiene identidad real.

Un objeto sin estado es solo estructura vacía.

