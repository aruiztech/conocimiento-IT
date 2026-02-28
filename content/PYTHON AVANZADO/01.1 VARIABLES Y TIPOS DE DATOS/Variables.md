---
title: Variables en Python
description: Explicación sobre variables en Python, cómo crearlas, manipularlas y reglas para nombrarlas.
tags: [Python, variables, programación]
date: 2026-02-28
---

# Variables

Una **variable** es un nombre que referencia un valor en memoria.  
Permite almacenar datos para usarlos más adelante en el programa.

---

## Conceptos clave

- Una variable tiene:  
  - Nombre  
  - Valor  
- Python es **dinámicamente tipado** (no necesitas declarar el tipo).  
- Las variables son sensibles a mayúsculas y minúsculas.  
- El valor puede cambiar durante la ejecución.

---

## Crear una variable

```python id="a3f7yv"
nombre = "Angel"
print(nombre)
````

### Resultado:

```text id="b2r5px"
Angel
```

---

## Variables numéricas

```python id="c1k8jw"
edad = 34
print(edad)
```

### Resultado:

```text id="d9m4lt"
34
```

---

## Cambiar el valor de una variable

```python id="e2p6qs"
edad = 34
edad = edad + 1
print(edad)
```

### Resultado:

```text id="f4v7kw"
35
```

Aquí estamos usando el valor anterior para calcular uno nuevo.

---

## Usar varias variables juntas

```python id="g3t5pn"
nombre = "Angel"
edad = 34

print("Me llamo", nombre, "y tengo", edad, "años")
```

### Resultado:

```text id="h8r2vq"
Me llamo Angel y tengo 34 años
```

---

## Reglas para nombrar variables

✅ Permitido:

* Letras
* Números (no al inicio)
* Guion bajo `_`

```python id="i6x3dj"
mi_variable = 10
edad2 = 25
```

❌ No permitido:

```python id="j4y8ws"
2edad = 25      # No puede empezar por número
mi variable = 3 # No puede tener espacios
```

---

## Asignación múltiple

```python id="k9p5lr"
a, b, c = 1, 2, 3
print(a, b, c)
```

### Resultado:

```text id="l3t6vh"
1 2 3
```

---

## Intercambiar valores

```python id="m2q4dk"
x = 10
y = 20

x, y = y, x

print(x, y)
```

### Resultado:

```text id="n7r8fj"
20 10
```

---

## Ver el tipo de una variable

```python id="o1v9wp"
edad = 34
print(type(edad))
```

### Resultado:

```text id="p6t3kr"
<class 'int'>
```

---

## Cómo funcionan internamente

Cuando escribes:

```python id="q3m5sj"
x = 10
```

Python:

1. Crea el objeto `10` en memoria
2. Hace que el nombre `x` apunte a ese objeto

Las variables no “contienen” el valor.
Apuntan a un objeto en memoria.

---

## Errores comunes

Usar una variable sin definirla:

```python id="r4n8vd"
print(nombre)
```

Resultado:

```text id="s2k7pw"
NameError: name 'nombre' is not defined
```

Confundir mayúsculas:

```python id="t3q9lx"
Edad = 30
print(edad)
```

Resultado:

```text id="u6r5kv"
NameError: name 'edad' is not defined
```

---

## Conecta con

* [[Tipos de datos]]
* [[Conversión de tipos]]
* [[Asignación en Python]]
* [[Mutabilidad vs inmutabilidad]]
* [[Ámbito de variables]]

---

## Analogía mental

Una variable es como una **etiqueta pegada a una caja**.

La etiqueta no es el contenido.
Solo indica dónde está el contenido.

Si cambias el contenido, la etiqueta sigue siendo la misma.

