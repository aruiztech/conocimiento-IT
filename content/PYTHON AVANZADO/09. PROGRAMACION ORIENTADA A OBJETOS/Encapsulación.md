---
title: "Encapsulación"
description: "Principio de POO que protege los atributos y métodos de una clase, controlando el acceso externo mediante convenciones y métodos."
tags: ["Python", "POO", "Clases", "Objetos", "Atributos", "Encapsulación"]
date: 2026-03-02
---

# Encapsulación

La **encapsulación** es un principio de la Programación Orientada a Objetos que **protege los datos de un objeto**, controlando el acceso a sus atributos y métodos.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Atributos]]
- [[Métodos]]
- [[init]]
- [[Métodos especiales (str, repr)]]

---

## Concepto

- Permite **ocultar información interna** de la clase.
- Protege los atributos y métodos de modificaciones externas no deseadas.
- Se logra mediante **convenciones de nombre** y métodos de acceso.

En Python, la encapsulación es **por convención**, no estricta.  

- `atributo` → público, accesible desde fuera.
- `_atributo` → protegido, se recomienda no acceder directamente.
- `__atributo` → privado, con **name mangling** (Python renombra internamente).

---

## Ejemplo básico

```python id="enc1"
class Cuenta:
    def __init__(self, titular, saldo):
        self.titular = titular        # público
        self._saldo = saldo           # protegido
        self.__clave = "1234"         # privado

cuenta = Cuenta("Ana", 1000)
print(cuenta.titular)  # Ana
print(cuenta._saldo)    # 1000 (acceso posible pero no recomendado)
# print(cuenta.__clave) # ❌ AttributeError
````

---

## Acceso a atributos privados

Se usan **métodos getter y setter**:

```python id="enc2"
class Cuenta:
    def __init__(self, titular, saldo):
        self.titular = titular
        self.__saldo = saldo  # privado

    # Getter
    def get_saldo(self):
        return self.__saldo

    # Setter
    def set_saldo(self, cantidad):
        if cantidad >= 0:
            self.__saldo = cantidad
        else:
            print("Saldo no puede ser negativo")
```

```python id="enc3"
cuenta = Cuenta("Luis", 500)
print(cuenta.get_saldo())  # 500
cuenta.set_saldo(800)
print(cuenta.get_saldo())  # 800
cuenta.set_saldo(-100)     # Saldo no puede ser negativo
```

---

## Propiedades con @property

Python permite usar **decoradores** para acceso seguro:

```python id="enc4"
class Cuenta:
    def __init__(self, titular, saldo):
        self.titular = titular
        self.__saldo = saldo

    @property
    def saldo(self):
        return self.__saldo

    @saldo.setter
    def saldo(self, cantidad):
        if cantidad >= 0:
            self.__saldo = cantidad
        else:
            print("Saldo no puede ser negativo")
```

```python id="enc5"
cuenta = Cuenta("Luis", 500)
print(cuenta.saldo)  # 500
cuenta.saldo = 700
print(cuenta.saldo)  # 700
cuenta.saldo = -50   # Saldo no puede ser negativo
```

---

## Analogía mental

Piensa en un objeto como una **caja fuerte**:

* Los atributos privados son como el contenido de la caja.
* Solo puedes acceder a ellos mediante **la llave correcta** (getter/setter).
* Esto protege los datos y evita errores por manipulación directa.

---

## Buenas prácticas

✔ Encapsula atributos sensibles o críticos de la clase.
✔ Usa `_` para indicar protección y `__` para privacidad estricta.
✔ Prefiere `@property` y setters en lugar de acceso directo a privados.
✔ Mantén consistencia en nombres de métodos de acceso.

---

## Idea clave final

La encapsulación garantiza que los **objetos controlen su propio estado**, evitando cambios directos desde fuera y promoviendo código más seguro y mantenible.

