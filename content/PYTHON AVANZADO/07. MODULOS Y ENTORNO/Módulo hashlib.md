---
title: Módulo hashlib — Hashing seguro en Python
description: Uso del módulo hashlib para generar hashes seguros de cadenas y archivos en Python, fundamental en ciberseguridad y autenticación.
tags: [python, modulos, hashlib, seguridad, hashing, ciberseguridad, analogía]
date: 2026-03-02
---

# Módulo hashlib en Python

El módulo `hashlib` permite generar **hashes criptográficos**, usados en:

- Almacenamiento seguro de contraseñas
- Verificación de integridad de archivos
- Autenticación y firmas digitales
- Seguridad en comunicaciones

> Relacionado con [[Módulo os]], [[Módulo json]], [[Sistema de autenticación con hashing]].

---

## 1. Importar el módulo

```python
import hashlib
````

---

## 2. Crear un hash SHA-256 de una cadena

```python id="hash1a2b"
texto = "contraseña123"
hash_obj = hashlib.sha256(texto.encode())
hash_hex = hash_obj.hexdigest()
print(hash_hex)
```

**Salida:**

```text
ef92b778ba... (resultado completo)
```

> **Analogía mental:** Es como pasar la cadena por una **máquina trituradora de información** que genera un código único e irreversible.

Relacionado con [[Módulo re]] (validación de entradas) y [[Definir funciones]].

---

## 3. Otros algoritmos de hashing

```python id="hash2a3b"
texto = "contraseña123"

md5_hash = hashlib.md5(texto.encode()).hexdigest()
sha1_hash = hashlib.sha1(texto.encode()).hexdigest()
sha512_hash = hashlib.sha512(texto.encode()).hexdigest()

print("MD5:", md5_hash)
print("SHA1:", sha1_hash)
print("SHA512:", sha512_hash)
```

> **Analogía:** Diferentes máquinas trituradoras, todas producen un código único diferente para la misma entrada.

---

## 4. Hashing de archivos

```python id="hash3a4b"
import hashlib
from pathlib import Path

archivo = Path("ejemplo.txt")
archivo.write_text("Este es un archivo de prueba.")

hash_archivo = hashlib.sha256()
with archivo.open("rb") as f:
    for bloque in iter(lambda: f.read(4096), b""):
        hash_archivo.update(bloque)

print("SHA-256 archivo:", hash_archivo.hexdigest())
```

> **Analogía:** Revisar la integridad de un archivo como sellando cada bloque con un código único.

Conexión: [[Módulo pathlib]], [[Lectura y escritura]], [[Ciberseguridad]].

---

## 5. Usar hashes en autenticación simple

```python id="hash5a6b"
import hashlib

def hash_contraseña(password):
    return hashlib.sha256(password.encode()).hexdigest()

stored_hash = hash_contraseña("mi_clave_secreta")
login_input = "mi_clave_secreta"

if hash_contraseña(login_input) == stored_hash:
    print("Acceso permitido")
else:
    print("Acceso denegado")
```

**Salida:**

```text
Acceso permitido
```

> Relacionado con [[Sistema de autenticación con hashing]] y [[Funciones]].

---

## Buenas prácticas

* Usar SHA-256 o SHA-512 en lugar de MD5 o SHA-1 (ya no seguros).
* No almacenar contraseñas en texto plano.
* Combinar con **salting** (añadir datos aleatorios) para proteger hashes.
* Validar entradas con [[Módulo re]] antes de hashear.

---

## Resumen

* `hashlib` permite generar hashes seguros para datos y archivos.
* Fundamental en **ciberseguridad** y autenticación.
* **Analogía final:** `hashlib` es como un **molino de códigos irreversibles**: la misma entrada siempre da el mismo hash, pero no se puede reconstruir el original.

Conexión: [[Módulo os]], [[Módulo json]], [[Sistema de autenticación con hashing]], [[Módulo pathlib]].

---

