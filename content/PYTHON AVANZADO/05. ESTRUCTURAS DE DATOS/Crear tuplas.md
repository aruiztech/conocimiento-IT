---
title: Crear tuplas — Estructuras de datos en Python
description: Explicación de cómo crear tuplas en Python, con ejemplos, resultados, enlaces a notas relacionadas y analogías mentales.
tags: [python, tuplas, estructuras, analogía]
date: 2026-03-01
---

# Crear tuplas — Estructuras de datos en Python

Una **tupla** es una colección **ordenada e inmutable** de elementos.  
Se usan cuando no quieres que los datos se modifiquen después de ser definidos.  

---

## Sintaxis básica

```python
mi_tupla = (1, 2, 3, 4)
otra_tupla = "a", "b", "c"  # sin paréntesis también funciona
tupla_vacia = ()
tupla_un_elemento = (5,)    # notar la coma
print(mi_tupla)
print(otra_tupla)
print(tupla_un_elemento)
````

**Salida:**

```python
(1, 2, 3, 4)
('a', 'b', 'c')
(5,)
```

> **Analogía mental:** Piensa en una tupla como un **contrato firmado**: una vez que está firmado, los valores no se pueden modificar.
> En contraste, una [[Crear listas]] es como una **caja de herramientas** que puedes reorganizar o agregar cosas a tu gusto.

---

## Acceso a elementos

```python
colores = ("rojo", "verde", "azul")
print(colores[0])  # rojo
print(colores[-1]) # azul
```

**Salida:**

```python
rojo
azul
```

> **Analogía:** Puedes **mirar dentro del contrato** y consultar valores, pero no cambiarlo.
> Relacionado con [[index()]] y [[count()]] si quieres buscar elementos en estructuras inmutables.

---

## Tuplas anidadas

```python
matriz = ((1, 2), (3, 4))
print(matriz[1][0])  # 3
```

**Salida:**

```python
3
```

> **Analogía:** Contratos dentro de contratos; puedes acceder a cláusulas específicas sin alterar nada.
> Esto conecta con [[List Comprehension]] si quieres generar listas a partir de tuplas.

---

## Diferencia clave con listas

| Característica | Lista            | Tupla            |
| -------------- | ---------------- | ---------------- |
| Mutabilidad    | Sí               | No               |
| Sintaxis       | `[ ]`            | `( )`            |
| Uso típico     | Datos cambiantes | Datos constantes |
| Velocidad      | Más lenta        | Más rápida       |

> **Analogía:** Lista = caja de herramientas; Tupla = contrato firmado.

---

## Buenas prácticas

* Usar tuplas cuando los datos **no deben cambiar**, por ejemplo coordenadas `(x, y)` o registros de configuración.
* Se pueden usar como **claves de diccionario** porque son inmutables, a diferencia de listas.

```python
registro = {("usuario1", "fecha"): "activo"}
print(registro)
```

**Salida:**

```python
{('usuario1', 'fecha'): 'activo'}
```

* Puedes combinar con listas o sets según necesidades:

```python
tupla_lista = [(1, 2), (3, 4)]  # lista de tuplas
print(tupla_lista)
```

**Salida:**

```python
[(1, 2), (3, 4)]
```

> Conexión con [[Crear listas]] y [[Sets]]: las tuplas inmutables pueden ser elementos de sets o claves de diccionarios.

---

## Resumen

* Las tuplas son **colecciones ordenadas e inmutables**.
* Útiles para datos que **no deben cambiar** y para combinarlas con otras estructuras de datos.
* Complementan [[List Comprehension]], [[Crear listas]] y [[Diccionarios]] en proyectos Python.
* **Analogía final:** Una tupla es tu **contrato seguro**: consultable, confiable y protegido de cambios accidentales.

---

