---
title: "Traceback"
description: "Cómo leer y entender un traceback en Python para depurar errores correctamente."
tags: ["Python", "Errores", "Depuración"]
date: 2026-03-02
---

# Traceback

Un **traceback** es el informe detallado que Python muestra cuando ocurre una excepción y el programa no puede continuar.

Es tu **mapa del crimen**: te dice qué ocurrió, dónde ocurrió y cómo llegó hasta allí.

Conecta directamente con:
- [[Errores comunes]]
- [[try y except]]
- [[Cómo leer errores]]
- [[Ámbito de variables]]

---

## ¿Qué es exactamente un traceback?

Cuando ocurre un error, Python imprime:

1. La secuencia de llamadas a funciones (desde el inicio hasta el punto del error).
2. El archivo y número de línea donde ocurrió.
3. El tipo de error.
4. El mensaje específico del error.

---

## Ejemplo básico de Traceback

```python
def dividir(a, b):
    return a / b

resultado = dividir(10, 0)
print(resultado)
````

Salida:

```text
Traceback (most recent call last):
  File "ejemplo.py", line 4, in <module>
    resultado = dividir(10, 0)
  File "ejemplo.py", line 2, in dividir
    return a / b
ZeroDivisionError: division by zero
```

---

## Cómo leer un Traceback correctamente

### Parte 1 — "Traceback (most recent call last):"

Indica que empieza el recorrido desde la última llamada hasta el error final.

---

### Parte 2 — La cadena de llamadas

```text
File "ejemplo.py", line 4, in <module>
resultado = dividir(10, 0)
```

Esto indica:

* Archivo: `ejemplo.py`
* Línea: 4
* Contexto: código principal

Luego:

```text
File "ejemplo.py", line 2, in dividir
return a / b
```

Aquí vemos:

* La función `dividir`
* Línea exacta donde ocurre el error

**El error real está en la última parte del traceback.**

---

### Parte 3 — Tipo y mensaje del error

```text
ZeroDivisionError: division by zero
```

Tipo: `ZeroDivisionError`
Mensaje: "division by zero"

---

## Analogía mental

Imagina que un coche se estrella.

El traceback es como:

1. La ruta que siguió el coche.
2. La calle exacta donde chocó.
3. El motivo del choque.

Sin traceback, estarías buscando el accidente a ciegas.

---

## Ejemplo con varias funciones

```python
def nivel1():
    nivel2()

def nivel2():
    nivel3()

def nivel3():
    print(variable_inexistente)

nivel1()
```

Salida:

```text
Traceback (most recent call last):
  File "ejemplo.py", line 10, in <module>
    nivel1()
  File "ejemplo.py", line 2, in nivel1
    nivel2()
  File "ejemplo.py", line 5, in nivel2
    nivel3()
  File "ejemplo.py", line 8, in nivel3
    print(variable_inexistente)
NameError: name 'variable_inexistente' is not defined
```

Aquí vemos claramente:

* Flujo de llamadas: nivel1 → nivel2 → nivel3
* Error final: NameError
* Línea exacta del fallo

Conexión directa con [[NameError]] dentro de [[Errores comunes]].

---

## Regla de oro al leer un Traceback

Siempre:

1. Baja hasta la última línea → identifica el tipo de error.
2. Sube una línea → localiza el archivo y número de línea.
3. Ignora el ruido intermedio hasta entender el punto exacto del fallo.

---

## Traceback en módulos y entornos virtuales

Cuando trabajas con:

* [[pip]]
* [[Entornos virtuales venv]]
* Librerías externas

El traceback puede mostrar rutas largas como:

```text
File ".../site-packages/..."
```

Eso significa que el error ocurre dentro de una librería instalada.

En ese caso:

* Revisa si estás usando correctamente la función.
* Verifica versión del paquete.
* Comprueba documentación oficial.

---

## Cómo usar el Traceback para mejorar como programador

Un buen programador no le teme al traceback.

Lo usa como herramienta.

Cada traceback te enseña:

* Cómo fluye tu programa.
* Cómo se conectan tus funciones.
* Dónde fallan tus suposiciones.

Esto desarrolla tu mentalidad de ingeniero.

Conecta con:

* [[Cómo dividir un problema]]
* [[Cómo depurar con breakpoint()]]
* [[pdb]]
* [[Buenas prácticas]]

---

## Buen hábito profesional

Cuando algo falla:

❌ No borres código al azar.
❌ No cambies cosas sin entender.

✔ Lee el traceback completo.
✔ Localiza la línea exacta.
✔ Comprende el tipo de excepción.
✔ Reproduce el error en pequeño.

---

## Próxima nota relacionada

* [[try y except]]
* [[else en excepciones]]
* [[finally]]
* [[raise]]
* [[Crear excepciones personalizadas]]

---

