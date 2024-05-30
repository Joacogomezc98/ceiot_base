# Entrega ejercicio 1

## Alumno

Joaquin Horacio Gomez Codino

## Sistema víctima

El sistema propuesto es una solución para la inspección automatizada de yacimientos petrolíferos y gasíferos. Utiliza drones equipados con sensores y análisis de datos basado en inteligencia artificial para capturar imágenes del terreno y los activos del yacimiento. Estas imágenes son procesadas para detectar anomalías y generar alertas. Los resultados de las inspecciones se presentan a través de una plataforma web intuitiva, que permite a los usuarios acceder a informes detallados y recibir notificaciones sobre posibles problemas.

El sistema consiste en:

- Frontend: Desarrollado en React.js (con TS)
- Backend: Desarrollado en Nest.js
- Base de datos: Postgres
- Cloud: AWS (S3 y lambdas principalmente)

## ATAQUE

**Objetivo:** Acceder a informacion sensible de yacimientos como fugas de petroleo para extorsionar a dichas empresas con hacer esta información publica.

1. **Reconnaissance:**

   i. Identifico personas con acceso a la plataforma de uali - [Tecnica T1589](https://attack.mitre.org/techniques/T1589/)

   ii. Identifico la topología del sistema. - [Tecnica T1590.004](https://attack.mitre.org/techniques/T1590/004)

   iii. Identifico IP de la API (Backend) - [Tecnica T1590.005](https://attack.mitre.org/techniques/T1590/005)

   iv. Identifico medidas de seguridad. - [Tecnica 1590.006](https://attack.mitre.org/techniques/T1590/006)

   v. Identifico informacion del hardware utilizado. - [Tecnica 1592.001](https://attack.mitre.org/techniques/T1592/001)

   vi. Identifico las tecnologias utilizadas por el software a traves de active scanning. - [Tecnica T1595](https://attack.mitre.org/techniques/T1595/)

2. **Weaponization:**

   i. Crear o adquirir exploits que aprovechen las vulnerabilidades descubiertas en el software, hardware o red de la plataforma de uali. - [Tecnica 1608.001](https://attack.mitre.org/techniques/T1608/001)

   ii. Crear payloads (malware) que se integren con los exploits desarrollados, listos para ser entregados al sistema objetivo. - [Tecnica 1608.002](https://attack.mitre.org/techniques/T1608/002)

   iii. Buscar y utilizar exploits ya conocidos y disponibles públicamente que coincidan con las vulnerabilidades identificadas. - [Tecnica T1587.001](https://attack.mitre.org/techniques/T1587/001)

   iv. Diseñar herramientas que faciliten el control de los sistemas comprometidos para extraer datos sensibles sin ser detectados. - [Tecnica 1608.003](https://attack.mitre.org/techniques/T1608/003)

   v. Preparar métodos efectivos para la entrega de los payloads, como correos de phishing dirigidos a empleados con acceso a información sensible o exploits que se activen mediante acciones del usuario. - [Tecnica 1204](https://attack.mitre.org/techniques/T1204).

   vi. Crear scripts o herramientas que permitan la extracción silenciosa de datos sensibles sobre yacimientos y fugas de petróleo una vez que el sistema ha sido comprometido. - [Tecnica 1071.001](https://attack.mitre.org/techniques/T1071/001)

3. **Delivery**

   i. Utilizar correos electrónicos de phishing personalizados para engañar a empleados específicos con acceso a información sensible. - [Tecnica 1566.001](https://attack.mitre.org/techniques/T1566/001)

   ii. Crear aplicaciones o actualizaciones falsas que parezcan legítimas pero que contengan el payload malicioso, engañando a los usuarios para que las descarguen e instalen. - [Tecnica 1072](https://attack.mitre.org/techniques/1072)

4. **Exploit**

   i. Cuando el objetivo hace clic en un enlace malicioso en un correo de phishing o sitio web comprometido, se ejecuta el código que explota una vulnerabilidad del navegador o plugin. - [Tecnica 1204.001](https://attack.mitre.org/techniques/T1204/001)

   ii. Cuando los usuarios instalan una aplicación o actualización falsa, se ejecuta el payload que explota vulnerabilidades en el sistema. - [Tecnica 1072](https://attack.mitre.org/techniques/T1072)

5. **Installation**

   i. **Puedo** instalar el payload en el sistema objetivo para asegurar un acceso continuo. - [Tecnica T1105](https://attack.mitre.org/techniques/T1105)

   ii. **Decido** Instalar backdoors para asegurar el acceso persistente y permitir el retorno al sistema comprometido sin necesidad de re-explotar las vulnerabilidades. - [Tecnica T1204.002](https://attack.mitre.org/techniques/T1204/002)

6. **Command & Control**

   i. **Puedo** utilizar protocolos de capa de aplicación como HTTP o HTTPS para establecer un canal de comunicación seguro y oculto entre el sistema comprometido y el servidor de comando y control. - [Tecnica T1071](https://attack.mitre.org/techniques/T1071)

   ii. **Decido** aprovechar servicios web legítimos, como plataformas de blogs, almacenamiento en la nube, o redes sociales, para enmascarar el tráfico C2 y evitar la detección. [Tecnica T1102](https://attack.mitre.org/techniques/T1102)

7. **Actions on Objectives**

   i. Recolecto y exfiltro datos críticos sobre yacimientos y fugas de petróleo para utilizar esta información con fines de extorsión. Utilizo el canal de C2 para transferir los datos exfiltrados de vuelta al servidor de comando y control. [Tecnica T1041](https://attack.mitre.org/techniques/T1041)

   ii. Intercepto y capturo datos en tránsito dentro de la red para obtener información crítica sobre la empresa objetivo. Utilizo herramientas de sniffing de red para capturar tráfico de red y extraer datos sensibles. - [Tecnica T1040](https://attack.mitre.org/techniques/T1040)
