# SurConnect IT Solutions — Infraestructura de Red Empresarial
### Diseño e Implementación de una Red Empresarial Segmentada

---

## Descripción del Proyecto

Este proyecto consiste en el diseño e implementación de una 
infraestructura de red empresarial para SurConnect IT Solutions, 
una empresa colombiana de outsourcing de TI con operaciones 
en toda Sudamérica y aproximadamente 9.000 empleados.

La solución implementa una arquitectura segmentada en tres zonas 
de seguridad (LAN, DMZ y Servidores Internos), gestionadas por 
pfSense como dispositivo central de control de acceso. Integra 
servicios de autenticación centralizada con FreeIPA y Active 
Directory, filtrado de contenido web con Squid, un portal 
corporativo con Nginx y distribución de software autorizado 
mediante SMB, todo implementado en un entorno virtualizado 
con VMware Workstation.

La documentación técnica completa del proyecto se encuentra 
en la sección Wiki de este repositorio.

---

## Objetivos Técnicos

- Diseñar una topología de red empresarial segmentada en zonas 
de seguridad diferenciadas (LAN, DMZ, Servidores Internos)
- Implementar un esquema de direccionamiento IPv4 aplicando 
diseño estructurado VLSM partiendo del bloque 10.0.0.0/8
- Configurar pfSense como firewall, router y dispositivo de 
control de acceso entre zonas con principio de mínimo privilegio
- Implementar autenticación centralizada con FreeIPA (LDAP + Kerberos) 
y Active Directory con políticas de acceso diferenciadas por rol (GPOs)
- Configurar filtrado de contenido web mediante Squid y SquidGuard
- Desplegar un portal web corporativo con Nginx en la DMZ 
con HTTPS y resolución DNS interna
- Implementar un servidor de distribución de software autorizado 
mediante SMB restringido al grupo de soporte técnico
- Bloquear herramientas de acceso remoto no autorizadas 
(TeamViewer, AnyDesk) mediante reglas de firewall
- Documentar el desarrollo completo del proyecto en GitHub Wiki

---

## Tecnologías Utilizadas

- **pfSense 2.7.2** — Firewall, Router y NAT (FreeBSD)
- **FreeIPA** — Autenticación centralizada, LDAP, Kerberos y DNS (Rocky Linux 9)
- **Windows Server 2022** — Active Directory, GPOs y SMB
- **Nginx** — Servidor web corporativo con HTTPS (Ubuntu Server)
- **Squid + SquidGuard** — Proxy y filtrado de contenido web (Ubuntu Server)
- **VMware Workstation** — Hipervisor para virtualización
- **IPv4 + VLSM** — Diseño estructurado de direccionamiento
- **Kerberos + LDAP** — Protocolos de autenticación centralizada
- **SMB (puerto 445)** — Distribución de software autorizado
- **GitHub** — Repositorio y Wiki de documentación

---

## Características de la Red

- Segmentación en tres zonas: LAN (/18), DMZ (/29) 
y Servidores Internos (/28)
- Control de acceso perimetral con reglas por zona en pfSense
- Bloqueo explícito de TeamViewer (5938) y AnyDesk (7070)
- Autenticación centralizada con roles diferenciados: 
empleados y soporte técnico
- Políticas de grupo (GPOs): bloqueo de CMD y Panel de Control 
para usuarios normales
- Portal corporativo accesible en https://des.net 
desde equipos de la LAN
- DNS interno gestionado por FreeIPA para todas las zonas
- Repositorio de software SMB restringido al grupo soporte-tecnico

---

## Información Académica

- **Asignatura:** Redes y Comunicación de Datos
- **Institución:** Universidad de La Sabana
- **Profesor:** Juan Manuel Aranda López
- **Periodo:** 2026-1

---

## Autores

- Santiago Escobar
- Esteban Sequeda
- Daniel Sanabria

---

## Estructura del Repositorio

- **Wiki** → Documentación técnica completa del proyecto
- **Comandos-Utilizados.txt** → Archivo con todos los comandos 
ejecutados durante la implementación en FreeIPA, Windows Server, 
pfSense, Nginx y Squid, organizados por servicio
- **Video** → [INSERTAR ENLACE VIDEO]
