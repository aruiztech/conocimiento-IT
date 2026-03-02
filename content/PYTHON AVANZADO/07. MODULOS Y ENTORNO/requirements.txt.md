---
title: requirements.txt — Gestionar dependencias en Python
description: Uso de requirements.txt para guardar y replicar las dependencias de un proyecto Python, asegurando consistencia y reproducibilidad.
tags: [python, dependencias, pip, entornos, automatización, buenas prácticas]
date: 2026-03-02
---

# requirements.txt en Python

`requirements.txt` es un archivo de texto que contiene **la lista de librerías y versiones exactas** que un proyecto necesita para funcionar correctamente.

- Permite **reproducir entornos** en otras máquinas.
- Facilita el trabajo en equipo y en proyectos profesionales.
- Conecta con [[Entornos virtuales venv]] y [[pip]].

> Relacionado con [[Entornos virtuales venv]], [[pip]], [[Importar módulos]].

---

## 1. Crear un archivo requirements.txt

```bash id="req1a"
pip freeze > requirements.txt
````

* `pip freeze` lista todas las librerías instaladas en el entorno activo con su versión exacta.
* El archivo generado tendrá un formato como:

```text id="req1r1"
requests==2.31.0
numpy==1.26.2
pandas==2.1.1
```

> **Analogía mental:** Es como hacer un inventario exacto de tu **caja de herramientas** de Python para compartirla o replicarla.

---

## 2. Instalar dependencias desde requirements.txt

```bash id="req2a"
pip install -r requirements.txt
```

* Instala todas las librerías y versiones listadas en el archivo.
* Garantiza que el proyecto funcione igual en cualquier máquina.

> **Analogía:** Replicar tu caja de herramientas exacta en otra mesa de trabajo sin errores.

---

## 3. Añadir o actualizar dependencias manualmente

* Puedes editar `requirements.txt` y luego ejecutar:

```bash id="req3a"
pip install -r requirements.txt
```

* Esto instalará cualquier nueva librería añadida o actualizará versiones según corresponda.

---

## 4. Buenas prácticas

* Mantener `requirements.txt` actualizado cada vez que agregues o cambies paquetes en tu proyecto.
* Usar siempre **entornos virtuales venv** para evitar conflictos.
* No incluir paquetes globales del sistema.
* Conectar con [[Entornos virtuales venv]] para automatizar la preparación del entorno.
* Combinable con [[Módulo pathlib]] para automatizar scripts que crean o leen `requirements.txt`.

---

## 5. Resumen

* `requirements.txt` es el estándar para **gestionar dependencias en Python**.
* Es clave para reproducibilidad, trabajo colaborativo y despliegue profesional.
* **Analogía final:** Es tu **lista de materiales exacta** para construir tu proyecto Python sin sorpresas.

Conexión: [[Entornos virtuales venv]], [[pip]], [[Importar módulos]], [[Módulo pathlib]].

---
