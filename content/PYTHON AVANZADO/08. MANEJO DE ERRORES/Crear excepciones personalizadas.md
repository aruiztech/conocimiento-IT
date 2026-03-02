---
title: "Crear excepciones personalizadas"
description: "Cómo definir y usar excepciones propias en Python para manejar reglas de negocio y errores específicos."
tags: ["Python", "Excepciones", "POO", "Buenas prácticas"]
date: 2026-03-02
---

# Crear excepciones personalizadas

En Python puedes definir tus propios tipos de error creando clases que hereden de `Exception`.

Esto permite:

- Representar reglas de negocio.
- Crear errores más claros.
- Diseñar sistemas más profesionales.
- Diferenciar tipos de fallos con precisión.

Conecta con:
- [[raise]]
- [[try y except]]
- [[finally]]
- [[Herencia en Python]]

---

## ¿Por qué no usar solo ValueError?

Podrías hacer esto:

```python
raise ValueError("Edad inválida")
````

Funciona.

Pero en sistemas grandes necesitas errores más específicos:

* UsuarioNoEncontradoError
* PermisoDenegadoError
* ConexionFallidaError
* SaldoInsuficienteError

Eso hace que el código sea más claro y mantenible.

---

## Forma básica

```python
class MiError(Exception):
    pass
```

Con eso ya tienes una excepción personalizada.

---

## Ejemplo simple

```python
class EdadInvalidaError(Exception):
    pass


def registrar_edad(edad):
    if edad < 0:
        raise EdadInvalidaError("La edad no puede ser negativa.")
```

Uso:

```python
try:
    registrar_edad(-5)
except EdadInvalidaError as e:
    print("Error detectado:", e)
```

Salida:

```text
Error detectado: La edad no puede ser negativa.
```

---

## Estructura profesional

Lo habitual es heredar directamente de `Exception`:

```python
class MiErrorPersonalizado(Exception):
    """Descripción del error."""
    pass
```

También puedes heredar de errores más específicos:

```python
class MiErrorDeValor(ValueError):
    pass
```

Esto permite mantener compatibilidad con bloques `except ValueError`.

---

## Ejemplo más realista

Sistema bancario simplificado:

```python
class SaldoInsuficienteError(Exception):
    pass


class CuentaBancaria:
    def __init__(self, saldo):
        self.saldo = saldo

    def retirar(self, cantidad):
        if cantidad > self.saldo:
            raise SaldoInsuficienteError("Fondos insuficientes.")
        self.saldo -= cantidad
```

Uso:

```python
cuenta = CuentaBancaria(100)

try:
    cuenta.retirar(200)
except SaldoInsuficienteError:
    print("Operación cancelada.")
```

Aquí el error representa una regla de negocio, no un fallo técnico.

---

## Excepciones con atributos

Puedes añadir información adicional:

```python
class ErrorDeAutenticacion(Exception):
    def __init__(self, usuario):
        self.usuario = usuario
        super().__init__(f"Usuario inválido: {usuario}")
```

Uso:

```python
raise ErrorDeAutenticacion("admin")
```

Esto permite enriquecer los errores con contexto.

---

## Jerarquía de excepciones

Puedes crear familias de errores:

```python
class ErrorAplicacion(Exception):
    pass


class ErrorBaseDeDatos(ErrorAplicacion):
    pass


class ErrorValidacion(ErrorAplicacion):
    pass
```

Luego puedes capturar:

```python
except ErrorAplicacion:
    # Captura todos los errores del sistema
```

Esto es arquitectura limpia.

---

## Buenas prácticas

✔ Hereda de `Exception`, no de `BaseException`.
✔ Usa nombres que terminen en `Error`.
✔ Documenta qué significa el error.
✔ Lanza errores cuando se rompan reglas claras.
✔ No abuses creando cientos innecesarios.

---

## Cuándo usar excepciones personalizadas

Úsalas cuando:

* Estás construyendo una librería.
* Hay múltiples tipos de fallo en tu sistema.
* Necesitas distinguir errores fácilmente.
* Quieres que otros desarrolladores entiendan mejor tu API.

---

## Flujo mental completo

```text
Regla de negocio se rompe → raise MiErrorPersonalizado
Código cliente → except MiErrorPersonalizado
Sistema mantiene claridad y control
```

---

