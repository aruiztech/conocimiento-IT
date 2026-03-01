---
title: Definir funciones — Python
description: Explicación de cómo definir funciones en Python, con ejemplos, resultados, analogías mentales y enlaces a otras notas.
tags: [python, funciones, modularidad, analogía]
date: 2026-03-01
---

# Definir funciones en Python

Una **función** es un bloque de código reutilizable que realiza una tarea específica.  
Permite **modularizar programas**, evitar repeticiones y mejorar la legibilidad.

> Relacionado con [[Parámetros y argumentos]], [[Return]], [[Funciones lambda]] y [[if __name__ == __main__]].

---

## 1. Sintaxis básica

```python
def saludar():
    print("¡Hola, mundo!")
````

* `def` → palabra clave para definir una función.
* `saludar` → nombre de la función.
* `()` → aquí se colocan los **parámetros** si los hay.
* `:` → indica el inicio del **cuerpo de la función**.
* La **indentación** es obligatoria.

---

## 2. Llamar a la función

```python
saludar()
```

**Salida:**

```python id="f1r0k"
¡Hola, mundo!
```

> **Analogía mental:** Una función es como **una receta de cocina**: la defines una vez y luego puedes “llamarla” cada vez que quieras preparar ese plato.
> Conecta con [[Parámetros y argumentos]] para funciones más flexibles.

---

## 3. Función con parámetros

```python
def saludar_persona(nombre):
    print(f"¡Hola, {nombre}!")
    
saludar_persona("Ángel")
```

**Salida:**

```python id="f1r1k"
¡Hola, Ángel!
```

> **Analogía:** La receta (función) tiene **ingredientes variables** (parámetros) que puedes cambiar cada vez que la uses.
> Relacionado con [[Argumentos por defecto]] y [[*args y **kwargs]].

---

## Buenas prácticas

* Nombrar funciones con **verbos claros**, como `calcular_area()`.
* Mantener funciones **cortas y con un solo propósito**.
* Usar **docstrings** para documentarlas (ver [[Docstrings]]).
* Evitar modificar variables externas; usar **retorno de valores** (ver [[Return]]).
* Organizar funciones relacionadas en módulos (ver [[Importar módulos]]).

---

## Resumen

* Una función es **un bloque de código reutilizable**.
* Se define con `def` y se llama por su nombre.
* Puede recibir **parámetros** y devolver **resultados**.
* **Analogía final:** Es como tener **recetas listas para ejecutar**, que puedes personalizar con ingredientes.
* Conexión: [[Parámetros y argumentos]], [[Return]], [[Funciones lambda]], [[Docstrings]], [[if **name** == **main**]].

---
