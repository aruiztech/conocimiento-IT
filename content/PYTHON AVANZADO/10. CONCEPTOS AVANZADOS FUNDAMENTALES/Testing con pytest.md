---
title: "Testing con pytest"
description: "Uso del framework pytest para crear pruebas automatizadas en Python de manera más simple y potente que unittest, con soporte para fixtures, parametrización y plugins."
tags: ["Python", "Avanzado", "Testing", "pytest", "Calidad de código"]
date: 2026-03-02
---

# Testing con pytest

**pytest** es un framework de Python para **testing automatizado**, más flexible y conciso que [[unittest]]:

- Detecta automáticamente funciones que comienzan con `test_`.  
- Permite **fixtures** para preparar y limpiar el entorno de pruebas.  
- Soporta **parametrización** de tests.  
- Se integra con [[Logging]] y pipelines de CI/CD.  
- Compatible con [[Funciones]], [[Clases]] y manejo de excepciones ([[try y except]], [[Raise]]).

---

## Conceptos clave

- **Test function**: función que comienza con `test_`.  
- **Assertions**: se usan directamente con `assert`.  
- **Fixtures**: funciones que preparan y limpian recursos antes/después de tests.  
- **Parametrización**: ejecutar un test con múltiples valores automáticamente.  
- **Plugins**: extensiones que agregan funcionalidades (ej. `pytest-cov` para cobertura).

---

## Ejemplo básico

```python id="pytest01"
# archivo: test_matematicas.py

def suma(a, b):
    return a + b

def test_suma_positiva():
    assert suma(2, 3) == 5

def test_suma_negativa():
    assert suma(-1, -1) == -2
````

**Ejecutar:**

```bash
pytest test_matematicas.py -v
```

**Salida:**

```text
test_matematicas.py::test_suma_positiva PASSED
test_matematicas.py::test_suma_negativa PASSED
```

---

## Ejemplo con manejo de excepciones

```python id="pytest02"
import pytest

def dividir(a, b):
    return a / b

def test_division_por_cero():
    with pytest.raises(ZeroDivisionError):
        dividir(5, 0)
```

**Salida:**

```text
test_matematicas.py::test_division_por_cero PASSED
```

* `pytest.raises` reemplaza a `unittest.assertRaises`.

---

## Ejemplo de fixture

```python id="pytest03"
import pytest

@pytest.fixture
def datos():
    return [1, 2, 3, 4, 5]

def test_suma_lista(datos):
    assert sum(datos) == 15
```

* `@pytest.fixture` prepara datos reutilizables para múltiples tests.

---

## Ejemplo de parametrización

```python id="pytest04"
import pytest

@pytest.mark.parametrize("a,b,resultado", [
    (2, 3, 5),
    (-1, -1, -2),
    (0, 5, 5)
])
def test_suma_param(a, b, resultado):
    assert a + b == resultado
```

**Salida al ejecutar:**

```text
test_matematicas.py::test_suma_param[2-3-5] PASSED
test_matematicas.py::test_suma_param[-1--1--2] PASSED
test_matematicas.py::test_suma_param[0-5-5] PASSED
```

---

## Analogía mental

* Piensa en **pytest** como un **robot inspector avanzado**:

  * Detecta automáticamente qué funciones probar.
  * Prepara recursos con fixtures antes de la inspección.
  * Prueba múltiples escenarios sin escribir código repetitivo (parametrización).
  * Reporta resultados claros y concisos.

---

## Buenas prácticas

✔ Usa nombres de funciones `test_` claros y descriptivos.
✔ Aplica fixtures para preparar y limpiar datos o recursos.
✔ Parametriza tests cuando quieras probar varios escenarios.
✔ Integra con [[Logging]] para registrar resultados de tests en producción.
✔ Combina con `pytest-cov` para medir cobertura de código.
✔ Mantén tests independientes y reproducibles.

---

## Idea clave final

`pytest` es **más moderno y potente que [[unittest]]**, ideal para proyectos Python profesionales, facilitando:

* Creación rápida de tests
* Pruebas de funciones, clases y manejo de excepciones
* Automatización de tests con CI/CD
* Integración con [[Logging]] y [[Subprocess]] para pruebas complejas
