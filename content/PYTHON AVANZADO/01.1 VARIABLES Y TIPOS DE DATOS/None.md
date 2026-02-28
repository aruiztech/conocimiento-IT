---
title: Tipo de dato None en Python
description: Explicación completa del tipo None, creación de variables, comparación, uso en funciones, valores por defecto y conversión a bool.
tags: [Python, None, tipos de datos, valores especiales, booleanos]
date: 2026-02-28
---

# 🐍 Tipo de dato: None

En Python, **None** representa la **ausencia de valor** o **nada**.  
Se usa para indicar que una variable **no tiene contenido**, un **retorno vacío** o un valor por defecto.

---

## 🔹 Crear variables con None

```python id="none2"
x = None
y = None
print(x)
print(y)
````

### ▶ Resultado:

```text id="none3"
None
None
```

---

## 🔹 Comparar con None

Para comprobar si una variable es None, se usa **is**, no `==`:

```python id="none4"
x = None

if x is None:
    print("x no tiene valor")
else:
    print("x tiene valor")
```

### ▶ Resultado:

```text id="none5"
x no tiene valor
```

---

## 🔹 Uso en funciones

Las funciones que no tienen `return` explícito devuelven **None**:

```python id="none6"
def saludar():
    print("Hola")

resultado = saludar()
print(resultado)
```

### ▶ Resultado:

```text id="none7"
Hola
None
```

---

## 🔹 Valores por defecto

```python id="none8"
def registrar_usuario(nombre, email=None):
    if email is None:
        print(f"{nombre} no proporcionó email")
    else:
        print(f"{nombre} tiene email: {email}")

registrar_usuario("Angel")
registrar_usuario("Luna", "luna@mail.com")
```

### ▶ Resultado:

```text id="none9"
Angel no proporcionó email
Luna tiene email: luna@mail.com
```

---

## 🔹 Conversión a bool

`None` siempre se considera **False** en contexto booleano:

```python id="none10"
x = None
if not x:
    print("x es considerado False")
```

### ▶ Resultado:

```text id="none11"
x es considerado False
```

---

## 🔗 Conecta con

* [[Tipos de datos]]
* [[bool]]
* [[Funciones]]
* [[Variables]]

---
