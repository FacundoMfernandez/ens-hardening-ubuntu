# ens-hardening-ubuntu
# Hardening Ubuntu 22.04 LTS — CIS Benchmarks + ENS Categoría Alta

> Proyecto del **Bootcamp 360° en Ciberseguridad** de The Bridge Digital Talent Accelerator (2025-2026).

## 🎯 Objetivo

Aplicar un proceso completo de hardening sobre un servidor Ubuntu 22.04 LTS siguiendo los CIS Benchmarks y las medidas del Esquema Nacional de Seguridad (ENS) en Categoría Alta. Documentar la comparativa de superficie de ataque antes y después del proceso.

## 🧪 Entorno

- **Sistema**: Ubuntu Server 22.04 LTS (instalación limpia)
- **Auditoría**: Lynis (pre y post hardening)
- **Virtualización**: Entorno aislado de laboratorio

## 🔁 Fases del proyecto

### 1. Auditoría inicial (Baseline)
Ejecución de Lynis sobre sistema sin hardening. Identificación de servicios expuestos, configuraciones por defecto inseguras, puertos abiertos y CVEs potenciales.

### 2. Aplicación de controles CIS
Implementación sistemática de los controles CIS Benchmark para Ubuntu 22.04:
- Configuración de particiones y permisos del filesystem
- Deshabilitación de servicios innecesarios
- Configuración segura de SSH (clave pública, deshabilitación root login)
- Políticas de contraseñas y gestión de cuentas
- Configuración de auditd y rsyslog
- Reglas de firewall (UFW/iptables)

### 3. Mapeo a controles ENS
Correspondencia entre cada control CIS aplicado y su equivalente en el marco ENS Categoría Alta, incluyendo:
- Control de acceso (op.acc)
- Protección de las comunicaciones (mp.com)
- Registro de actividad (op.exp.8)
- Gestión de cambios (op.exp.5)

### 4. Auditoría final (Post-hardening)
Segunda ejecución de Lynis para medir la mejora. Comparativa cuantitativa y cualitativa de la superficie de ataque.

## 🛠️ Herramientas utilizadas

| Herramienta | Uso en el proyecto |
|---|---|
| Lynis | Auditoría de seguridad pre y post |
| CIS Benchmarks | Marco de controles de hardening |
| ENS (CCN-STIC) | Mapeo normativo español |
| auditd | Sistema de auditoría del kernel |
| rsyslog | Gestión centralizada de logs |
| UFW / iptables | Firewall |
| AIDE | Verificación de integridad de archivos |
| Bash scripting | Automatización del proceso |

## 📊 Aprendizajes clave

- La importancia de medir antes y después — sin baseline no hay evidencia de mejora
- Hardening no es "una vez y listo" — requiere proceso de revisión periódica
- El balance entre seguridad y operatividad: desactivar servicios sin entender su función rompe cosas
- La diferencia entre aplicar un checklist mecánicamente vs entender el porqué de cada control

## 🔒 Nota de confidencialidad

> **⚠️ Los informes detallados, scripts de automatización, resultados de auditoría y capturas de pantalla no se publican en este repositorio por razones de confidencialidad con la entidad formativa (The Bridge Digital Talent Accelerator).**
>
> **Si eres reclutador o profesional del sector y deseas ver el material completo, no dudes en contactarme:**
>
> 📧 **seguridadinformaticamf@gmail.com**
> 🔗 **[LinkedIn](https://www.linkedin.com/in/facundo-martin-fernandez-oton-/)**
>
> Estaré encantado de compartirlo en una conversación directa o entrevista técnica.

## ⚠️ Disclaimer

Este proyecto se ejecutó en un entorno de laboratorio aislado con fines educativos.

## 📧 Contacto

[Facundo Martín Fernández Otón](https://www.linkedin.com/in/facundo-martin-fernandez-oton-/) · [GitHub](https://github.com/FacundoMfernandez)

---

🔍 *¿Estás reclutando para un equipo SOC, Blue Team o IR? Mirá mi [perfil](https://github.com/FacundoMfernandez) y hablemos.*
