---
title: Uso de la terminal
description: Guía sobre cómo usar la terminal en Windows, macOS y Linux para ejecutar Python y trabajar como desarrollador.
tags: [Python, terminal, comandos, desarrollo]
date: 2026-02-28
---

# Uso de la terminal

La **terminal** (también llamada consola o línea de comandos) es una herramienta que permite interactuar con el sistema operativo mediante comandos de texto.  

Es fundamental para ejecutar Python, instalar paquetes y trabajar como desarrollador profesional.

---

## Conceptos clave

- Permite ejecutar programas sin interfaz gráfica.  
- Es más rápida y potente que usar solo el explorador de archivos.  
- Es esencial en programación, automatización y ciberseguridad.  
- Se usa para ejecutar scripts `.py`, instalar librerías y gestionar proyectos.

---

## Cómo abrir la terminal

### Windows

- Presiona `Win + R`, escribe `cmd` y presiona Enter.  
- O busca **PowerShell** en el menú inicio.  
- También puedes usar **Windows Terminal** (recomendado).

### macOS

- Abre **Terminal** desde Aplicaciones → Utilidades.  
- O usa Spotlight (`Cmd + Espacio`) y escribe "Terminal".

### Linux

- Atajo común: `Ctrl + Alt + T`.  
- O busca “Terminal” en el menú del sistema.

---

## Comandos básicos

### Ver dónde estás (directorio actual)

```bash
pwd
````

En Windows también puede usarse:

```bash
cd
```

---

### Ver archivos y carpetas

```bash
ls
```

En Windows:

```bash
dir
```

---

### Cambiar de carpeta

```bash
cd nombre_carpeta
```

Ejemplo:

```bash
cd Documentos
```

---

### Volver atrás una carpeta

```bash
cd ..
```

---

### Crear una carpeta

```bash
mkdir mi_proyecto
```

---

### Crear un archivo Python vacío

```bash
touch archivo.py
```

(En Windows puedes crear el archivo manualmente o usar:)

```bash
echo. > archivo.py
```

---

## Ejecutar un archivo Python desde la terminal

```bash
python archivo.py
```

O en algunos sistemas:

```bash
python3 archivo.py
```

---

## Flujo típico de trabajo

1. Abrir la terminal.
2. Navegar hasta tu carpeta de proyecto.
3. Ejecutar el archivo Python.
4. Ver el resultado.
5. Editar el código.
6. Volver a ejecutar.

Este ciclo se repite constantemente.

---

## Errores comunes

* Ejecutar un archivo desde la carpeta incorrecta.
* No saber en qué directorio estás trabajando.
* Confundir `python` con `python3`.
* Escribir mal el nombre del archivo.

---

## Conecta con

* [[Instalación de Python]]
* [[Cómo ejecutar un archivo .py]]
* [[REPL de Python]]
* [[pip]]
* [[Entornos virtuales venv]]
* [[Uso profesional de la terminal]]


