# Proyecto GESTOP: Diseño e Implementación de Infraestructura IT

> Trabajo de Final de Grado (Crédito de Síntesis) - SMX
> Autor: Yassine El Hachioui

Este proyecto documenta el diseño integral, presupuesto y despliegue técnico de la infraestructura informática para la empresa simulada "Gestop". El alcance abarca desde el diseño físico de la red (cableado y electrónica) hasta la administración de servicios en entornos híbridos Windows/Linux.

## Objetivos del Proyecto
1.  Diseñar la red física sobre plano: cálculo de cableado, rosetas y armarios de comunicaciones.
2.  Implementar una arquitectura cliente-servidor híbrida (Windows Server y Ubuntu Linux).
3.  Desplegar servicios de red críticos: Web, Correo, Archivos y Directorio Activo.
4.  Realizar el estudio de hardware y presupuesto económico.

---

## 1. Infraestructura de Red Física y Electrónica
Se realizó un diseño sobre plano de las oficinas para calcular la tirada de cable necesaria y la ubicación de los puestos de trabajo.

* **Cableado Estructurado:** Cálculo de metros lineales de cable UTP Cat 6, canaletas y rosetas RJ45.
* **Electrónica de Red:** Selección de Routers para la salida a Internet y Switches gestionables para la interconexión de la LAN.
* **Inventario:** Presupuesto detallado de Racks, Paneles de Parcheo (Patch Panels) y Latiguillos.

*(Aquí puedes insertar la imagen del plano o del presupuesto de red si la tienes)*

---
## 2. Administración de Servidores

### Entorno Windows Server 2019
Actúa como el controlador principal de la infraestructura.
* **Active Directory (AD DS):** Gestión centralizada de usuarios, grupos y unidades organizativas.
* **Servidor Web (IIS):** Alojamiento de la intranet corporativa (`www.gestop.local`).
* **Servidor FTP:** Repositorio de archivos departamental con permisos NTFS estrictos y aislamiento de usuarios.
* **Servicios de Red:** Configuración de servidor DNS y DHCP para la asignación dinámica de direcciones.

![Servidor Web IIS](image.png)
*Figura 1: Despliegue del servicio web en IIS.*

### Entorno Linux (Ubuntu Server) - Servidor de Correo
Se implementó un servidor dedicado para la gestión de comunicaciones, integrando múltiples protocolos para un servicio de correo completo.
* **MTA (Mail Transfer Agent):** Postfix para el enrutamiento y envío de correos (SMTP).
* **MDA (Mail Delivery Agent):** Dovecot para la recepción de correos mediante protocolos IMAP/POP3.
* **Webmail:** Implementación de Roundcube para acceso al correo vía navegador.
* **Seguridad:** Configuración de Firewall (UFW) permitiendo únicamente puertos de correo (25, 143, 993, etc.) y SSH.

![Configuración Linux Postfix](linux-mail.png)
*Figura 2: Gestión del servicio de correo en Linux.*

---

## 3. Arquitectura de Hardware (Workstations)
Estudio de mercado para dotar a la empresa de equipos adaptados a las necesidades de cada perfil profesional, comparando arquitecturas Intel y AMD.

* **Perfil Ofimática:** Equipos optimizados para tareas administrativas y gestión documental.
* **Perfil Técnico/Ciberseguridad:** Estaciones de trabajo de alto rendimiento para virtualización y auditoría.

![Tabla de Hardware](hardware-setup.png)
*Figura 3: Tabla comparativa y presupuesto de componentes.*

---

## Tecnologías y Herramientas Utilizadas
* **Virtualización:** Oracle VirtualBox (Configuración de Red Interna y NAT).
* **Sistemas Operativos:** Windows Server 2019, Windows 10, Ubuntu Server LTS.
* **Protocolos:** TCP/IP, DNS, DHCP, HTTP, FTP, SMTP, IMAP.
* **Software de Servidor:** Microsoft IIS, Bind9, Postfix, Dovecot, Roundcube.

> [Ver Documentación Completa del Proyecto GESTOP (PDF)](GESTOP%20-%20Yassine%20El.pdf)
> [Ver Detalle Configuración Servidor Correo Linux (PDF)](_Pt2.2%20Instal·lació%20i%20conf
