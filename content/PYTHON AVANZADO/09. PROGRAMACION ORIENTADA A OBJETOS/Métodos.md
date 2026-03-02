---
title: "Métodos"
description: "Qué son los métodos en Programación Orientada a Objetos y cómo funcionan en Python."
tags: ["Python", "POO", "Métodos", "Clases", "Objetos"]
date: 2026-03-02
---

# Métodos

Los **métodos** son funciones definidas dentro de una clase.

Representan el **comportamiento** de los objetos.

Conecta con:
- [[Clases]]
- [[Objetos]]
- [[Atributos]]
- [[Encapsulación]]
- [[Métodos especiales]]

---

## ¿Qué hacen los métodos?

Si los atributos representan el **estado**,  
los métodos representan lo que el objeto **puede hacer**.

Ejemplo conceptual:

```text
Objeto: Coche

Atributos:
- velocidad
- color

Métodos:
- acelerar()
- frenar()
- girar()
````

---

## Sintaxis básica

```python
class Persona:
    def saludar(self):
        print("Hola")
```

El primer parámetro siempre es `self`.

---

## ¿Qué es self?

`self` representa la instancia actual del objeto.

Permite que el método acceda a los atributos del objeto.

Ejemplo:

```python id="met1"
class Persona:
    def __init__(self, nombre):
        self.nombre = nombre

    def saludar(self):
        print(f"Hola, soy {self.nombre}")
```

Uso:

```python id="met2"
persona1 = Persona("Ana")
persona1.saludar()
```

Salida:

```text id="met3"
Hola, soy Ana
```

---

## Métodos que modifican el estado

Los métodos pueden cambiar atributos:

```python id="met4"
class Cuenta:
    def __init__(self, saldo):
        self.saldo = saldo

    def depositar(self, cantidad):
        self.saldo += cantidad
```

Uso:

```python id="met5"
cuenta = Cuenta(100)
cuenta.depositar(50)
print(cuenta.saldo)  # 150
```

Aquí el método altera el estado interno.

---

## Métodos que retornan valores

```python id="met6"
class Calculadora:
    def sumar(self, a, b):
        return a + b
```

Uso:

```python id="met7"
calc = Calculadora()
resultado = calc.sumar(3, 5)
print(resultado)  # 8
```

---

## Tipos de métodos

En Python existen tres tipos principales:

### 1️⃣ Métodos de instancia

Son los más comunes.
Reciben `self`.

```python
def metodo(self):
    ...
```

---

### 2️⃣ Métodos de clase

Usan el decorador `@classmethod`
Reciben `cls` en lugar de `self`.

```python id="met8"
class Ejemplo:
    contador = 0

    @classmethod
    def incrementar(cls):
        cls.contador += 1
```

Se relacionan con atributos de clase.

---

### 3️⃣ Métodos estáticos

Usan `@staticmethod`
No reciben ni `self` ni `cls`.

```python id="met9"
class Utilidades:
    @staticmethod
    def sumar(a, b):
        return a + b
```

Son funciones agrupadas dentro de una clase por organización.

---

## Diferencia conceptual

```text
Método de instancia → trabaja con el objeto
Método de clase → trabaja con la clase
Método estático → no depende ni de clase ni de objeto
```

---

## Buenas prácticas

✔ Usa métodos para encapsular comportamiento.
✔ Evita métodos demasiado largos.
✔ Cada método debe tener una responsabilidad clara.
✔ No conviertas la clase en un conjunto caótico de funciones.

---

## Métodos y encapsulación

Los métodos controlan cómo se modifican los atributos.

Ejemplo profesional:

```python id="met10"
class Cuenta:
    def __init__(self, saldo):
        self._saldo = saldo

    def retirar(self, cantidad):
        if cantidad > self._saldo:
            raise ValueError("Fondos insuficientes.")
        self._saldo -= cantidad
```

Aquí el método protege la integridad del objeto.

---

## Mentalidad orientada a objetos

En POO no preguntas:

> ¿Qué función debo usar?

Preguntas:

> ¿Qué objeto debería encargarse de esta acción?

Eso es diseño.

---

## Idea clave final

Los atributos definen lo que el objeto es.

Los métodos definen lo que el objeto hace.

Sin métodos, una clase es solo un contenedor de datos.
