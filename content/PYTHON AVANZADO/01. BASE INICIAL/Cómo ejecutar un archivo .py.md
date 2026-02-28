---
title: Cómo ejecutar un archivo .py
description: Explicación sobre cómo ejecutar scripts de Python desde terminal, IDE o doble clic.
tags: [Python, ejecución, scripts]
date: 2026-02-28
---

# Cómo ejecutar un archivo .py

Un archivo `.py` es un script de Python que contiene instrucciones que la computadora puede ejecutar.  

Para ver cómo funciona tu código, debes **ejecutarlo** usando Python.

---

## Conceptos clave

- Python es un **lenguaje interpretado**, por lo que ejecuta el código línea por línea.  
- Para ejecutar un archivo `.py` necesitas tener **Python instalado** en tu sistema.  
- Puedes ejecutar scripts desde **terminal/command prompt** o desde un **IDE/editor**.

---

## Formas de ejecutar un archivo `.py`

### Desde la terminal (Windows)

1. Abre el **Símbolo del sistema (CMD)** o **PowerShell**.  
2. Navega a la carpeta donde guardaste tu archivo `.py` usando:

```bash
cd ruta\de\tu\carpeta
````

3. Escribe:

```bash
python nombre_del_archivo.py
```

4. Pulsa **Enter** y verás la salida de tu script.

> Nota: En algunas instalaciones, puede que necesites `python3 nombre_del_archivo.py`.

---

### Desde un IDE o editor

* Abre tu archivo `.py` en un editor como **VS Code, PyCharm, Thonny o Pydroid 3**.
* Busca un botón que diga **Run** o **Ejecutar**.
* El IDE ejecutará el script y mostrará la salida en una consola integrada.

---

### Ejecutar desde doble clic (Windows)

* Cambia la extensión del archivo a `.pyw` si no quieres que aparezca la ventana de la terminal.
* Haz doble clic en el archivo, se ejecutará con Python instalado.
* Útil para scripts simples de automatización o ventanas gráficas.

---

## Conecta con

* [[¿Qué es Python?]] → Para entender qué hace el script.
* [[Variables]] → Almacenar datos que se muestran al ejecutar.
* [[print()]] → Mostrar información en pantalla.
* [[Errores comunes]] → Qué pasa si falla la ejecución.

---

## Analogía mental

Ejecutar un archivo `.py` es como darle órdenes a un robot:

* El archivo es la **lista de instrucciones**.
* Python es el **robot** que lee cada línea y la ejecuta.
* La salida que ves en pantalla es el resultado del robot haciendo su trabajo.

