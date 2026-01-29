# 🏢 GESTOP: Proyecto de Infraestructura IT Híbrida

> **Crédito de Síntesis - Grado Medio SMX**
>
> Este proyecto documenta el diseño, presupuesto y despliegue técnico de la infraestructura informática completa para una empresa simulada ("Gestop"). Se integran servicios heterogéneos (Windows/Linux) y se define la arquitectura de hardware.

## 🎯 Objetivos Técnicos
- **Interoperabilidad:** Integración de servidores Windows y Linux en un mismo dominio.
- **Servicios de Red:** Despliegue de Web (IIS), Transferencia de ficheros (FTP) y Correo (Postfix).
- **Hardware:** Selección de componentes y montaje de equipos según perfil de usuario.

---

## ⚙️ Implementaciones Realizadas

### 1. Servidor Web y FTP (Windows Server 2019)
Se configuró **IIS (Internet Information Services)** para alojar la intranet corporativa y un servidor FTP con autenticación segura.
- **Acceso Web:** `http://www.gestop.local`
- **Seguridad FTP:** Permisos NTFS aplicados a carpetas de usuario.

![Servidor Web IIS](web-iis.png)
*Figura 1: Intranet corporativa desplegada sobre IIS.*

![Servidor FTP](ftp-server.png)
*Figura 2: Acceso al servidor de ficheros FTP.*

---

### 2. Servidor de Correo (Linux Ubuntu Server)
Implementación de un servidor de mensajería utilizando **Postfix**.
- **MTA:** Configuración de Postfix para gestión de correo saliente/entrante.
- **Integración:** El servidor Linux resuelve nombres mediante el DNS del Directorio Activo.

---

### 3. Arquitectura de Hardware
Estudio de mercado y selección de componentes para estaciones de trabajo de alto rendimiento (Ciberseguridad/Virtualización) y ofimática básica.

![Tabla de Hardware](hardware-setup.png)
*Figura 3: Planificación de componentes (AMD Ryzen / Intel Core).*

---

## 🏆 Tecnologías Utilizadas
- **Virtualización:** Oracle VirtualBox.
- **Sistemas Operativos:** Windows Server 2019, Windows 10, Ubuntu Server.
- **Protocolos:** HTTP, FTP, SMTP, DNS, DHCP.
