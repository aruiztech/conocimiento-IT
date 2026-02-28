---
title: Instalación de Python
description: Guía completa para instalar Python en Windows, macOS y Linux, y verificar la instalación.
tags: [Python, instalación, configuración]
date: 2026-02-28
---

# Instalación de Python

Instalar Python correctamente es el primer paso para poder ejecutar scripts, crear proyectos y usar herramientas como `pip` o entornos virtuales.

---

## Conceptos clave

- Python puede descargarse desde su página oficial.  
- Es importante agregar Python al **PATH** del sistema.  
- La instalación incluye normalmente:  
  - El intérprete (`python`)  
  - El gestor de paquetes (`pip`)  
- Puedes verificar la instalación desde la terminal.

---

## Descarga oficial

Descarga Python desde:

https://www.python.org/downloads/

⚠️ Evita descargarlo desde sitios no oficiales.

---

## Instalación en Windows

1. Descarga el instalador desde la web oficial.  
2. Ejecuta el archivo `.exe`.  
3. ✅ Marca la opción **"Add Python to PATH"**.  
4. Haz clic en **Install Now**.  
5. Espera a que finalice la instalación.

---

## Instalación en macOS

### Opción 1 (recomendada): usar el instalador oficial

1. Descarga el `.pkg` desde la web oficial.  
2. Ejecuta el instalador.  
3. Sigue los pasos hasta finalizar.

### Opción 2 (usuarios más técnicos): usar Homebrew

```bash
brew install python
````

---

## Instalación en Linux

En muchas distribuciones ya viene instalado.

Verifica primero:

```bash
python3 --version
```

Si no está instalado:

```bash
sudo apt update
sudo apt install python3 python3-pip
```

(Comando válido para distribuciones basadas en Debian/Ubuntu).

---

## Verificar que Python está instalado

Abre la terminal o CMD y escribe:

```bash
python --version
```

O en algunos sistemas:

```bash
python3 --version
```

Deberías ver algo como:

```
Python 3.12.0
```

---

## Verificar pip

```bash
pip --version
```

O:

```bash
pip3 --version
```

Si aparece una versión, significa que pip está correctamente instalado.

---

## Probar el intérprete (REPL)

En la terminal escribe:

```bash
python
```

O:

```bash
python3
```

Deberías ver algo así:

```
>>>
```

Eso significa que estás dentro del intérprete interactivo de Python.

Para salir:

```python
exit()
```

---

## Errores comunes

* No marcar "Add Python to PATH" en Windows.
* Tener múltiples versiones de Python sin saber cuál se está ejecutando.
* Confundir `python` con `python3` en sistemas Linux/macOS.

---

## Conecta con

* [[Uso de la terminal]]
* [[REPL de Python]]
* [[Cómo ejecutar un archivo .py]]
* [[pip]]
* [[Entornos virtuales venv]]

