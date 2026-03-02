---
title: Entornos virtuales venv — Aislar proyectos en Python
description: Uso de entornos virtuales con venv para gestionar dependencias de proyectos Python de manera independiente y segura.
tags: [python, entornos, venv, dependencias, virtualenv, proyectos, automatización, buenas prácticas]
date: 2026-03-02
---

# Entornos virtuales venv en Python

Un **entorno virtual** permite crear un espacio aislado para cada proyecto Python, de manera que:

- Las librerías instaladas no afecten al sistema global.
- Diferentes proyectos puedan usar versiones distintas de paquetes.
- Se mejore la reproducibilidad y mantenimiento del código.

> Relacionado con [[pip]], [[Importar módulos]], [[Entornos virtuales]].

---

## 1. Crear un entorno virtual

```bash id="venv1a"
python -m venv mi_entorno
````

* Crea una carpeta `mi_entorno` con una copia aislada de Python y pip.
* **Analogía mental:** Cada entorno virtual es como una **caja de herramientas separada** para cada proyecto, sin mezclar herramientas con otros proyectos.

---

## 2. Activar el entorno virtual

* **Windows:**

```bash id="venv2a"
mi_entorno\Scripts\activate
```

* **Linux / macOS:**

```bash id="venv2b"
source mi_entorno/bin/activate
```

**Indicador:** Aparece el nombre del entorno en la terminal `(mi_entorno)`.

> Relacionado con [[pip]] y [[Entornos virtuales venv]].

---

## 3. Instalar paquetes dentro del entorno

```bash id="venv3a"
pip install requests
```

* El paquete `requests` solo estará disponible dentro de `mi_entorno`.
* **Analogía mental:** Es como guardar herramientas exclusivas dentro de tu caja de proyecto.

---

## 4. Listar paquetes instalados

```bash id="venv4a"
pip list
```

Muestra todas las librerías y versiones dentro del entorno virtual activo.

---

## 5. Guardar dependencias — `requirements.txt`

```bash id="venv5a"
pip freeze > requirements.txt
```

* Crea un archivo con todas las librerías y versiones instaladas.
* Permite **reproducir el entorno exacto** en otra máquina.

> Conexión: [[Entornos virtuales]], [[pip]], [[Importar módulos]].

---

## 6. Instalar dependencias desde `requirements.txt`

```bash id="venv6a"
pip install -r requirements.txt
```

* Instala todas las librerías necesarias para el proyecto.
* **Analogía:** Replicar exactamente tu caja de herramientas en otro lugar.

---

## 7. Desactivar el entorno

```bash id="venv7a"
deactivate
```

* Vuelve al Python global.
* **Analogía:** Guardar la caja de herramientas y volver a la mesa principal.

---

## Buenas prácticas

* Crear un entorno virtual para **cada proyecto**.
* Mantener actualizado `requirements.txt`.
* No instalar paquetes globalmente si trabajas en proyectos compartidos.
* Activar el entorno antes de ejecutar scripts o pruebas.
* Conectar con [[pip]] y [[Módulo pathlib]] para scripts de automatización.

---

## Resumen

* `venv` permite **aislar proyectos Python**, evitando conflictos de versiones.
* Es esencial para **proyectos profesionales y reproducibles**.
* **Analogía final:** Cada entorno virtual es una **caja de herramientas independiente**, lista para tu proyecto sin ensuciar el resto del sistema.

Conexión: [[pip]], [[Importar módulos]], [[Entornos virtuales]].

---
