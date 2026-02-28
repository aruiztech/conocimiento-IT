---
title: "ISO/IEC 27000 — MOC Integrado (Enfoque Técnico)"
objective: "Comprender la base de la gestión de seguridad de la información (SGSI) y conectarla con redes, sistemas y Python"
level: "Fundamentos sólidos con visión profesional"
---
# ISO/IEC 27000 — MOC Integrado (Enfoque Técnico)

> Objetivo: Comprender la base de la gestión de seguridad de la información (SGSI) y conectarla con redes, sistemas y Python  
> Nivel: Fundamentos sólidos con visión profesional

# 1. Fundamentos de Seguridad de la Información

## Conceptos Base
- [[Qué es la Seguridad de la Información]]
- [[Triada CIA]] ✅ (ya existente en Pre-ASIR)
- [[Activo de información]]
- [[Amenaza]]
- [[Vulnerabilidad]] ✅
- [[Riesgo]]
- [[Impacto]]
- [[Probabilidad]]
- [[Superficie de ataque]] ✅
- [[Vector de ataque]] ✅

🎯 Conexiones:
- [[Tipos de amenazas informáticas]]
- [[Ataques comunes en redes]]
- [[Ingeniería social (concepto)]]

# 2. Familia ISO 27000

## Normas principales
- [[ISO 27000 (visión general)]]
- [[ISO 27001]]
- [[ISO 27002]]
- [[ISO 27005]]
- [[ISO 27701]]

🎯 Objetivo:  
Entender qué es un SGSI y cómo se estructura.

# 3. SGSI (Sistema de Gestión de Seguridad de la Información)
- [[Qué es un SGSI]]
- [[Ciclo PDCA (Plan-Do-Check-Act)]]
- [[Política de Seguridad]]
- [[Alcance del SGSI]]
- [[Análisis de riesgos]]
- [[Tratamiento del riesgo]]
- [[Declaración de aplicabilidad (SoA)]]
- [[Auditoría interna]]
- [[Mejora continua]]

🎯 Conexiones técnicas:
- [[Principio de mínimo privilegio]] (Pre-ASIR)
- [[Permisos en Linux]] (Pre-ASIR)
- [[Gestión de usuarios y grupos]]
- [[Logging]] (Python MOC)
- [[Análisis básico de logs]] (Laboratorio)

# 4. Gestión de Riesgos (ISO 27005)
- [[Identificación de activos]]
- [[Valoración de activos]]
- [[Identificación de amenazas]]
- [[Evaluación de vulnerabilidades]]
- [[Matriz de riesgo]]
- [[Aceptación del riesgo]]
- [[Mitigación del riesgo]]
- [[Transferencia del riesgo]]

🎯 Conexión práctica:
- [[Escaneo de puertos]] (Python)
- [[Captura de tráfico con Wireshark (concepto)]]
- [[Configuración de firewall en laboratorio]]

# 5. Controles de Seguridad (ISO 27002)

## Organización
- [[Roles y responsabilidades en seguridad]]
- [[Segregación de funciones]]

## Control de acceso
- [[Control de acceso]]
- [[Autenticación]]
- [[Autorización]]
- [[Gestión de identidades]]
- [[MFA (Autenticación multifactor)]]
- [[Sistema de autenticación con hashing]] ✅

## Seguridad técnica
- [[Hardening]]
- [[Gestión de parches]]
- [[Cifrado simétrico]] (Redes MOC)
- [[Cifrado asimétrico]]
- [[RSA]]
- [[TLS]]
- [[VPN]]
- [[Hashing]]
- [[Generación segura con secrets]]

# 6. Seguridad en Redes dentro de ISO 27000
- [[Segmentación de red]]
- [[Firewalls]]
- [[IDS vs IPS]]
- [[NAT]]
- [[DNS y DHCP]]
- [[WiFi (802.11)]]
- [[Seguridad WiFi]]

🎯 Conexión con:
- [[Modelo OSI]]
- [[Modelo TCP/IP]]
- [[Puertos y protocolos]]
- [[Escáner simple de red]]

# 7. Seguridad en Sistemas
- [[Gestión de procesos]] (Pre-ASIR)
- [[Gestión de memoria]]
- [[Sistema de archivos]]
- [[Permisos en Linux]]
- [[Usuario y Grupo]]
- [[Hardening en Linux]]
- [[Backups]]
- [[Plan de recuperación ante desastres (DRP)]]
- [[Continuidad del negocio (BCP)]]

# 8. Seguridad en Entornos Modernos
- [[Cloud Computing]]
- [[Responsabilidad compartida en Cloud]]
- [[Virtualización de redes]]
- [[IoT]]
- [[Data Centers]]
- [[SDN]]

# 9. Auditoría y Cumplimiento
- [[Qué es una auditoría de seguridad]]
- [[Evidencias de seguridad]]
- [[Registros (Logs)]]
- [[Trazabilidad]]
- [[No conformidad]]
- [[Acción correctiva]]
- [[Acción preventiva]]

🎯 Conexión técnica:
- [[Logging]]
- [[Análisis básico de logs]]
- [[Proyecto 4 - Analizador de logs]]

# 10. Mentalidad ISO para Perfil Técnico
- [[Seguridad por diseño]]
- [[Defensa en profundidad]]
- [[Zero Trust]]
- [[Evaluación continua]]
- [[Gestión de cambios]]

# 11. Laboratorio Personal ISO 27000

## Simulación práctica
- [[Inventario de activos del laboratorio]]
- [[Evaluación de riesgos del laboratorio virtual]]
- [[Política de seguridad del laboratorio]]
- [[Segmentación de red en VirtualBox]]
- [[Configuración segura de Ubuntu Server]]
- [[Configuración segura de Kali Linux]]

🎯 Proyecto:
- Crear tu propio mini SGSI personal.

# Cómo conecta este MOC con los otros

### Con Python MOC
- Hashing
- secrets
- logging
- Analizador de logs
- Sockets
- Automatización de seguridad

### Con Pre-ASIR
- Permisos Linux
- Principio de mínimo privilegio
- Procesos
- Gestión de memoria
- Laboratorio virtual

### Con Redes
- OSI
- TCP/IP
- Firewalls
- TLS
- VPN
- Segmentación

# Lo importante que debes entender
ISO 27000 NO es hacking.  
Es marco mental profesional.  
Te enseña a pensar como:
- Administrador responsable
- Auditor
- Responsable de seguridad
- Ingeniero con visión empresarial