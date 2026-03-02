---
title: "Errores comunes"
description: "Repaso de los errores más frecuentes en Python y cómo identificarlos para mejorar la depuración."
tags: ["Python", "Errores", "Depuración"]
date: 2026-03-02
---

# Errores comunes en Python

En Python, incluso los programadores experimentados cometen errores. Conocer los errores más frecuentes te ayudará a depurar más rápido y a entender mejor el comportamiento de tus programas.

---

## Tipos de errores más frecuentes

### 1. SyntaxError (Error de sintaxis)

Ocurre cuando Python no entiende el código que escribiste porque no sigue la **gramática del lenguaje**.

**Ejemplo:**
```python
print("Hola mundo"
````

**Salida:**

```
SyntaxError: unexpected EOF while parsing
```

**Analogía mental:** Es como si escribieras una frase en español pero olvidaras un punto o una coma: el lector (Python) no puede entenderla.

**Tips de prevención:**

* Revisa paréntesis, comillas y sangrías.
* Usa un editor que marque errores de sintaxis en tiempo real.

---

### 2. NameError (Variable no definida)

Se produce cuando intentas usar una variable que **no existe o no está definida en el ámbito actual**.

**Ejemplo:**

```python
print(valor)
```

**Salida:**

```
NameError: name 'valor' is not defined
```

**Analogía mental:** Es como llamar a alguien por un nombre que nadie tiene: nadie responde.

**Conexión:** Ver [[Ámbito de variables]] para entender cómo Python gestiona nombres y alcance.

---

### 3. TypeError (Error de tipo)

Ocurre cuando realizas una operación con un tipo de dato que **no es compatible**.

**Ejemplo:**

```python
numero = 5
texto = "3"
resultado = numero + texto
```

**Salida:**

```
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

**Analogía mental:** Es como intentar sumar manzanas y naranjas en la misma operación sin convertirlas.

**Solución:** Convertir tipos con `int()`, `str()`, `float()`.

**Ejemplo corregido:**

```python
resultado = numero + int(texto)
print(resultado)
```

**Salida:**

```
8
```

---

### 4. IndexError (Índice fuera de rango)

Se da cuando intentas acceder a un **índice que no existe en una lista, tupla o string**.

**Ejemplo:**

```python
lista = [1, 2, 3]
print(lista[5])
```

**Salida:**

```
IndexError: list index out of range
```

**Analogía mental:** Es como pedir el libro número 6 en una estantería que solo tiene 3 libros.

**Prevención:** Usar `len()` o validaciones antes de acceder.

---

### 5. KeyError (Clave inexistente en diccionarios)

Sucede cuando intentas acceder a una **clave que no existe** en un diccionario.

**Ejemplo:**

```python
diccionario = {"a": 1, "b": 2}
print(diccionario["c"])
```

**Salida:**

```
KeyError: 'c'
```

**Solución:** Usar `get()` con valor por defecto o verificar existencia con `in`.

```python
print(diccionario.get("c", 0))  # Devuelve 0 si no existe
```

**Conexión:** Ver [[Diccionarios]] y [[Métodos de diccionarios]].

---

### 6. ValueError (Valor incorrecto)

Ocurre cuando un **valor tiene el tipo correcto** pero es **inapropiado para la operación**.

**Ejemplo:**

```python
int("Hola")
```

**Salida:**

```
ValueError: invalid literal for int() with base 10: 'Hola'
```

**Analogía mental:** Es como intentar insertar un cajón cuadrado en un hueco redondo: el tipo coincide (cajón) pero no encaja el valor.

---

### 7. AttributeError (Atributo inexistente)

Sucede cuando llamas a un **método o atributo que no existe** en un objeto.

**Ejemplo:**

```python
numero = 5
numero.append(3)
```

**Salida:**

```
AttributeError: 'int' object has no attribute 'append'
```

**Analogía mental:** Es como intentar abrir una puerta que no tiene manilla.

**Conexión:** Ver [[Métodos de listas]] y [[Métodos de cadenas]] para entender qué métodos existen según el tipo.

---

### 8. ImportError / ModuleNotFoundError

Se produce cuando Python **no puede encontrar un módulo** que intentas importar.

**Ejemplo:**

```python
import modulo_inexistente
```

**Salida:**

```
ModuleNotFoundError: No module named 'modulo_inexistente'
```

**Solución:**

* Instala el paquete con `pip install nombre_paquete`.
* Verifica tu entorno virtual con [[Entornos virtuales venv]].
* Asegúrate de que el nombre del módulo es correcto y que está en tu `PYTHONPATH`.

---

### 9. IndentationError (Error de sangría)

Python **depende de la sangría** para definir bloques de código. Una sangría incorrecta genera error.

**Ejemplo:**

```python
if True:
print("Hola")
```

**Salida:**

```
IndentationError: expected an indented block
```

**Analogía mental:** Es como escribir un párrafo sin márgenes: no se entiende dónde empieza ni dónde termina cada sección.

---

### 10. Recursión infinita / RecursionError

Ocurre cuando una función **se llama a sí misma sin condición de parada**.

**Ejemplo:**

```python
def infinito():
    return infinito()

infinito()
```

**Salida:**

```
RecursionError: maximum recursion depth exceeded
```

**Solución:** Asegurarse de definir una condición base que detenga la recursión.

---

## Consejos generales para manejar errores

1. **Lee el traceback** completo: te indica línea y tipo de error.
2. **Divide y conquista:** aislar bloques problemáticos ayuda a localizar errores.
3. **Usa `try` y `except`** para manejar errores esperados [[try y except]].
4. **Prueba en REPL** para verificar pequeños fragmentos antes de integrarlos en scripts grandes [[REPL de Python]].
5. **Comenta temporalmente** partes del código para depurar [[Comentarios en Python]].

---

## Próximas notas relacionadas

* [[Traceback]]
* [[try y except]]
* [[else en excepciones]]
* [[finally]]
* [[raise]]
* [[Crear excepciones personalizadas]]

---
