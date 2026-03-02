---
title: "Testing con unittest"
description: "Uso del módulo unittest de Python para crear pruebas automatizadas, verificar el comportamiento de funciones y garantizar calidad de código."
tags: ["Python", "Avanzado", "Testing", "unittest", "Calidad de código"]
date: 2026-03-02
---

# Testing con unittest

El **módulo `unittest`** permite crear **tests automatizados** en Python para asegurar que tus funciones y clases se comporten correctamente.  
Se conecta con:
- [[Funciones]] y [[Clases]] para pruebas unitarias de lógica y métodos
- [[Logging]] para registrar resultados de tests
- [[Módulos y entorno]] para pruebas de componentes individuales
- [[try y except]] para pruebas de manejo de excepciones

---

## Conceptos clave

- **TestCase**: clase base para crear pruebas.  
- **assertions**: métodos que verifican condiciones (`assertEqual`, `assertTrue`, `assertRaises`, etc.).  
- **setUp / tearDown**: métodos que se ejecutan antes y después de cada test.  
- **suite**: conjunto de tests agrupados.  
- **runner**: ejecuta los tests y muestra resultados.

---

## Ejemplo básico

```python id="unittest01"
import unittest

def suma(a, b):
    return a + b

class TestSuma(unittest.TestCase):
    def test_suma_positivos(self):
        self.assertEqual(suma(2, 3), 5)

    def test_suma_negativos(self):
        self.assertEqual(suma(-1, -1), -2)

if __name__ == "__main__":
    unittest.main()
````

**Salida al ejecutar:**

```text id="unittest02"
..
----------------------------------------------------------------------
Ran 2 tests in 0.001s

OK
```

* Cada punto (`.`) indica que un test pasó correctamente.
* Si falla algún test, aparece un `F` y un traceback del error.

---

## Ejemplo con assertRaises (excepciones)

```python id="unittest03"
import unittest

def dividir(a, b):
    return a / b

class TestDivision(unittest.TestCase):
    def test_division_cero(self):
        with self.assertRaises(ZeroDivisionError):
            dividir(5, 0)

if __name__ == "__main__":
    unittest.main()
```

**Salida:**

```text id="unittest04"
.
----------------------------------------------------------------------
Ran 1 test in 0.001s

OK
```

* Verifica que una función **lanza la excepción esperada**, útil para pruebas de robustez.

---

## Analogía mental

* Piensa en **unittest** como un **control de calidad en fábrica**:

  * Cada función es un producto que se prueba antes de enviarlo.
  * Cada assertion es una inspección que debe pasar para aprobar.
  * `setUp` prepara la maquinaria antes de cada prueba, y `tearDown` limpia después.

---

## Buenas prácticas

✔ Crea una clase `TestCase` por módulo de funcionalidad.
✔ Usa nombres descriptivos para métodos de test (`test_login_valido`).
✔ Prueba tanto casos normales como límites y errores esperados.
✔ Automatiza la ejecución con CI/CD o scripts.
✔ Combina con [[Logging]] para registrar resultados en proyectos grandes.

---

## Idea clave final

`unittest` es la **herramienta oficial de Python** para pruebas unitarias, imprescindible para **proyectos profesionales**, asegurando:

* Corrección de funciones y clases
* Manejo adecuado de excepciones
* Facilidad de mantenimiento y refactorización
* Integración con [[Logging]] y automatización de tests en pipelines CI/CD
