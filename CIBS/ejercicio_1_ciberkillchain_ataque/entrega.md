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

   i. **Identifico personas con acceso a la plataforma de uali** - [Tecnica T1589: Gather Victim Identity Information](https://attack.mitre.org/techniques/T1589/)

   ii. **Identifico la topología del sistema.** - [Tecnica T1590.004: Network Topology](https://attack.mitre.org/techniques/T1590/004)

   iii. **Identifico IP de la API (Backend)** - [Tecnica T1590.005: IP Addresses](https://attack.mitre.org/techniques/T1590/005)

   iv. **Identifico medidas de seguridad.** - [Tecnica 1590.006: Defensive Systems](https://attack.mitre.org/techniques/T1590/006)

   vi. **Identifico las tecnologias utilizadas por el software a traves de active scanning.** - [Tecnica T1595: Active Scanning](https://attack.mitre.org/techniques/T1595/)

2. **Weaponization:**

i. **Desarrollo de un Correo Electrónico de Phishing Engañoso** - Puedo crear un correo electrónico falso persuasivo con alertas de seguridad, adaptado específicamente para engañar a los destinatarios y obtener información confidencial, como credenciales de usuario. - [Técnica T1598.001 - Phishing](https://attack.mitre.org/techniques/T1598/001)

ii. **Creación de una Página Web Falsa para Phishing** - Decido desarrollar una página web falsa que imite fielmente el aspecto y la funcionalidad de un sitio web legítimo de la empresa objetivo. Esta página se utilizará para capturar las credenciales de usuario proporcionadas por las víctimas que hayan sido dirigidas a ella a través del correo electrónico de phishing. - [Técnica T1598.001 - Phishing](https://attack.mitre.org/techniques/T1598/001).

3. **Delivery**

   i. **Envío del Correo Electrónico de Phishing** - Decido crear un correo electrónico falso persuasivo con alertas de seguridad, adaptado específicamente para engañar a los destinatarios y que entren a la pagina web falsa a traves del link de ese mail y se logueen con sus credenciales de la plataforma original. - [Técnica T1566.003 - Spearphishing Link](https://attack.mitre.org/techniques/T1566/001)

4. **Exploit**

   i. **Explotación de Credenciales de Usuario** - Decido aprovechar las credenciales de usuario obtenidas en la pagina de phishing para acceder a la plataforma con los accesos requeridos. - [Técnica T1078 - Valid Account](https://attack.mitre.org/techniques/T1078/)

5. **Installation**

   i. **Puedo** elevar mis privilegios y obtener un mayor control. - [Explotación para Escalada de Privilegios](https://attack.mitre.org/techniques/T1068/)

   ii. **Puedo** crear nuevos usuarios en el sistema comprometido con privilegios adecuados para mantener el acceso persistente.
   [Técnica T1136 - Create Account](https://attack.mitre.org/techniques/T1136/)

   iii. **Decido** guardar las credenciales obtenidas y aprovechar la manipulación de cuentas para obtener credenciales adicionales en la nube, lo que me permite mantener el acceso incluso si las credenciales originales son revocadas o cambiadas. [Técnica T1098 - Additional Cloud Credentials](https://attack.mitre.org/techniques/T1098/001/)

6. **Command & Control**

   i. **Puedo** configurar un servidor proxy para enrutar el tráfico de comando y control a través de él, ocultando la ubicación real del servidor de comando y control y dificultando la detección. - [Técnica T1090 - Proxy](https://attack.mitre.org/techniques/T1090/)

   ii. **Decido** desarrollar un proceso que combine los datos sensibles con los datos basura para dificultar la deteccion. - [Técnica T1565/001 Manipulación de Datos: Datos Basura](https://attack.mitre.org/techniques/T1565/001)

7. **Actions on Objectives**

   i. Recolecto y exfiltro datos críticos sobre yacimientos y fugas de petróleo para utilizar esta información con fines de extorsión. - [Técnica T1567 - Exfiltration Over Web Service](https://attack.mitre.org/techniques/T1567/)
