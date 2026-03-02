---
title: "Métodos especiales (str, repr)"
description: "Uso de los métodos especiales __str__ y __repr__ en Python para personalizar la representación de objetos."
tags: ["Python", "POO", "Clases", "Objetos", "Métodos especiales", "str", "repr"]
date: 2026-03-02
---

# Métodos especiales (str, repr)

Los **métodos especiales** en Python permiten personalizar el comportamiento de los objetos.  
Entre los más usados para representación de objetos están:

- `__str__`: representación **legible para humanos**.
- `__repr__`: representación **informativa para desarrolladores**.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Métodos]]
- [[Atributos]]

---

## Diferencia conceptual

| Método   | Uso principal                      | Ejemplo mental                          |
|----------|-----------------------------------|----------------------------------------|
| `__str__` | Mostrar al usuario final          | Etiqueta bonita en un paquete           |
| `__repr__`| Mostrar al programador/desarrollador | Código que puede recrear el objeto    |

---

## Sintaxis básica

```python id="mes1"
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def __str__(self):
        return f"{self.nombre}, {self.edad} años"

    def __repr__(self):
        return f"Persona(nombre='{self.nombre}', edad={self.edad})"
````

---

## Uso de **str**

`__str__` se usa al imprimir el objeto:

```python id="mes2"
p = Persona("Ana", 25)
print(p)  # Ana, 25 años
```

Salida:

```text id="mes3"
Ana, 25 años
```

Esta es la versión **amigable para humanos**.

---

## Uso de **repr**

`__repr__` se usa cuando inspeccionamos el objeto en consola o en depuración:

```python id="mes4"
p  # en REPL o debugger
```

Salida:

```text id="mes5"
Persona(nombre='Ana', edad=25)
```

Esta versión es más **informativa y precisa**, útil para programadores.

---

## Analogía mental

Piensa en `__str__` como la **etiqueta bonita del producto**
y `__repr__` como la **ficha técnica que permite reconstruirlo**.

---

## Buenas prácticas

✔ Siempre define `__repr__` para que los objetos sean fáciles de depurar.
✔ Define `__str__` si quieres una salida legible al usuario.
✔ Si solo defines `__repr__`, Python lo usará también para `str()` si no hay `__str__`.
✔ Mantén `__repr__` preciso y que idealmente permita recrear el objeto.

---

## Ejemplo completo

```python id="mes6"
class Cuenta:
    def __init__(self, titular, saldo=0):
        self.titular = titular
        self.saldo = saldo

    def __str__(self):
        return f"Cuenta de {self.titular} con saldo {self.saldo}€"

    def __repr__(self):
        return f"Cuenta(titular='{self.titular}', saldo={self.saldo})"

c = Cuenta("Luis", 100)
print(c)   # Cuenta de Luis con saldo 100€
c         # Cuenta(titular='Luis', saldo=100)
```

---

## Idea clave final

* `__str__` → pensado para **humanos**, más amigable y legible.
* `__repr__` → pensado para **programadores**, más técnico y preciso.

Estos métodos hacen que tus objetos sean **claros, útiles y fáciles de depurar**.
