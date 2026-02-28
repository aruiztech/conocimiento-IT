---
title: Reglas para nombrar variables en Python
description: Normas obligatorias y buenas prácticas para nombrar variables en Python de forma clara y profesional.
tags: [Python, variables, buenas prácticas, estilo, sintaxis]
date: 2026-02-28
---

# Reglas para nombrar variables

Nombrar bien las variables es fundamental para escribir código claro, profesional y fácil de mantener.

Python tiene reglas obligatorias (sintaxis) y buenas prácticas recomendadas (estilo).

---

# 🧠 1️⃣ Reglas obligatorias (Sintaxis)

Estas reglas deben cumplirse o el código dará error.

---

## ✅ 1. Solo letras, números y guion bajo (_)

```python
mi_variable = 10
edad2 = 25
_total = 100
````

---

## ❌ 2. No puede comenzar con número

```python
2edad = 25
```

### ▶ Resultado:

```text
SyntaxError: invalid decimal literal
```

---

## ❌ 3. No puede contener espacios

```python
mi variable = 10
```

### ▶ Resultado:

```text
SyntaxError: invalid syntax
```

---

## ❌ 4. No puede usar palabras reservadas

```python
class = 10
```

### ▶ Resultado:

```text
SyntaxError: invalid syntax
```

Algunas palabras reservadas:

* `if`
* `for`
* `while`
* `class`
* `def`
* `return`
* `import`

---

## ⚠️ 5. Diferencia entre mayúsculas y minúsculas

```python
edad = 30
Edad = 40

print(edad)
print(Edad)
```

### ▶ Resultado:

```text
30
40
```

Son variables distintas.

---

# 🧑‍💻 2️⃣ Buenas prácticas (Estilo profesional)

Estas no generan error, pero hacen tu código más limpio.

---

## ✅ Usar snake_case

```python
nombre_completo = "Angel Martinez"
total_usuarios = 150
precio_final = 19.99
```

❌ Evitar:

```python
NombreCompleto = "Angel"
precioFinal = 19.99
```

En Python, la convención oficial es **snake_case** para variables.

---

## ✅ Usar nombres descriptivos

❌ Malo:

```python
x = 10
y = 20
```

✅ Mejor:

```python
precio_producto = 10
cantidad = 20
```

---

## ✅ Constantes en MAYÚSCULAS

```python
PI = 3.1416
MAX_INTENTOS = 3
```

Convención usada en proyectos profesionales.

---

# 🧠 ¿Por qué es importante?

Un mal nombre:

* Hace el código difícil de entender.
* Genera errores al crecer el proyecto.
* Complica el mantenimiento.

Un buen nombre:

* Explica la intención.
* Reduce la necesidad de comentarios.
* Mejora la calidad profesional del código.

---

# 🔗 Conecta con

* [[Variables]]
* [[PEP8]]
* [[Buenas prácticas]]
* [[Estructura profesional de proyecto]]

---

# 🧩 Analogía mental

Nombrar variables es como **etiquetar carpetas**.

Si pones:

```
carpeta1
carpeta2
```

No sabes qué contienen.

Pero si pones:

```
facturas_2024
clientes_activos
```

Todo se entiende sin abrirlas.

---
