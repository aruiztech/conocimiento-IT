---
title: "CEH - MOC Integrado (Certified Ethical Hacker)"
certification: "EC-Council CEH"
objective: "Comprender metodologías de hacking ético con base sólida técnica"
level: "Intermedio (requiere base en redes, sistemas y scripting)"
focus: "Técnico + mentalidad profesional"
---
# CEH - MOC Integrado (Certified Ethical Hacker)

> Objetivo: Comprender metodologías de hacking ético con base sólida técnica  
> Nivel: Intermedio (requiere base en redes, sistemas y scripting)  
> Enfoque: Técnico + mentalidad profesional

# 1. Fundamentos del Hacking Ético

## Conceptos base
- [[Qué es el hacking ético]]
- [[White Hat vs Black Hat vs Gray Hat]]
- [[Pentesting]]
- [[Red Team vs Blue Team]]
- [[Fases del hacking ético]]
- [[Metodología de pentesting]]
- [[Ética y marco legal del hacking]]

🎯 Conexiones:
- [[ISO 27001]]
- [[Gestión de riesgos]]
- [[Triada CIA]]
- [[Seguridad por diseño]]

# 2. Footprinting y Reconocimiento
- [[Reconocimiento pasivo]]
- [[Reconocimiento activo]]
- [[OSINT]]
- [[Enumeración]]
- [[DNS y reconocimiento]]
- [[Whois (concepto)]]
- [[Ingeniería social (concepto)]]

🎯 Conexiones:
- [[DNS]]
- [[Puertos y protocolos]]
- [[Modelo OSI]]
- [[Vector de ataque]]
- [[Superficie de ataque]]

# 3. Escaneo de Redes
- [[Escaneo de puertos]] ✅ (Python MOC)
- [[Tipos de escaneo]]
- [[TCP vs UDP en escaneo]]
- [[Banner Grabbing]]
- [[Detección de servicios]]
- [[Fingerprinting de sistemas]]

🎯 Conexiones:
- [[TCP]]
- [[UDP]]
- [[Handshake de tres vías]]
- [[Sockets]]
- [[Proyecto 7 - Escáner simple de red]]
- [[Wireshark (concepto)]]

# 4. Enumeración y Explotación Básica
- [[Enumeración SMB]]
- [[Enumeración SNMP]]
- [[Fuerza bruta (concepto)]]
- [[Diccionarios de ataque]]
- [[Vulnerabilidad]]
- [[Exploit (concepto)]]
- [[Payload (concepto)]]

🎯 Conexiones:
- [[Hashing]]
- [[Sistema de autenticación con hashing]]
- [[Gestión de usuarios y grupos]]
- [[Permisos en Linux]]

# 5. Ataques a Sistemas
- [[Escalada de privilegios]]
- [[Hardening]]
- [[Gestión de parches]]
- [[Persistencia (concepto)]]
- [[Backdoors (concepto)]]

🎯 Conexiones:
- [[Principio de mínimo privilegio]]
- [[Modo usuario vs modo kernel]]
- [[Gestión de procesos]]
- [[Sistema de archivos]]

# 6. Ataques a Redes
- [[ARP Spoofing]]
- [[Man in the Middle (MITM)]]
- [[Sniffing]]
- [[DoS vs DDoS]]
- [[Secuestro de sesión]]

🎯 Conexiones:
- [[ARP]]
- [[Switches]]
- [[NAT]]
- [[TLS]]
- [[VPN]]
- [[Captura de tráfico con Wireshark (concepto)]]

# 7. Seguridad Web
- [[HTTP]]
- [[HTTPS]]
- [[OWASP Top 10]]
- [[SQL Injection (concepto)]]
- [[XSS (concepto)]]
- [[CSRF (concepto)]]
- [[Autenticación web]]

🎯 Conexiones:
- [[Requests]]
- [[JSON y APIs REST]]
- [[Proyecto 8 - Mini API con Flask]]
- [[Sistema de autenticación con hashing]]

# 8. Criptografía en CEH
- [[Cifrado simétrico]]
- [[Cifrado asimétrico]]
- [[RSA]]
- [[TLS]]
- [[Hashing]]
- [[Criptografía básica]]

🎯 Conexión directa:
- [[Redes de computadoras - Andrew S. Tanenbaum]]
- [[ISO-IEC 27000 — MOC Integrado (Enfoque Técnico)]]

# 9. Hacking en Entornos Modernos
- [[Cloud Computing]]
- [[Responsabilidad compartida en Cloud]]
- [[Virtualización de redes]]
- [[IoT]]
- [[Contenedores (concepto)]]

# 10. Wireless Hacking (Conceptual)
- [[WiFi (802.11)]]
- [[Seguridad WiFi]]
- [[WPA2 vs WPA3]]
- [[Ataques comunes en redes inalámbricas]]

# 11. Herramientas (Nivel Conceptual)
- [[nmap (concepto)]]
- [[Wireshark (concepto)]]
- [[Metasploit (concepto)]]
- [[Burp Suite (concepto)]]
- [[Hydra (concepto)]]

⚠️ En mi laboratorio personal:
- [[Instalar Kali Linux en VirtualBox]]
- [[Montar laboratorio virtual]]
- [[Crear red interna virtual]]

# 12. Mentalidad de Pentester
- [[Modelo de amenazas]]
- [[Defensa en profundidad]]
- [[Zero Trust]]
- [[Reporte de vulnerabilidades]]
- [[Ética profesional en ciberseguridad]]
- [[Documentación técnica]]

🎯 Conexión:
- [[ISO 27001]]
- [[Auditoría interna]]
- [[Evidencias de seguridad]]
- [[Análisis básico de logs]]

# 13. Laboratorio Personal CEH

## Fase 1
- Crear red virtual aislada
- Simular red doméstica
- Aplicar escaneo básico

## Fase 2
- Analizar tráfico
- Detectar vulnerabilidades
- Proponer mitigaciones

## Fase 3
- Redactar informe técnico estilo auditoría

🎯 Proyecto final:
- Simulación completa de pentest interno documentado

# Cómo conecta este MOC con todo mi ecosistema

|Área|Conexión|
|---|---|
|Python|Sockets, hashing, automatización, escáner|
|Redes (Tanenbaum)|OSI, TCP/IP, ruteo, protocolos|
|CCNA|VLAN, switching, routing, ACL|
|ISO 27000|Gestión de riesgos, controles|
|Pre-ASIR|Linux, permisos, procesos|

# Algo importante
CEH **no sustituye**:
- Base de redes (CCNA)
- Base de sistemas (ASIR)
- Mentalidad de gestión (ISO 27000)

CEH es la capa ofensiva encima de todo eso.