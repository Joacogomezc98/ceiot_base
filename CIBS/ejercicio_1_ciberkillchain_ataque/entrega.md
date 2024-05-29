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

**Objetivo:** Acceder a informacion sensible de yacimientos para como fugas de petroleo para extorsionar a dichas empresas con hacer esta información publica.

1. **Reconnaissance:**

   i. Identifico personas con acceso a la plataforma de uali - [Technique T1589](https://attack.mitre.org/techniques/T1589/)

   ii. Identifico IP de la API - [Technique T1590](https://example.com)

   iii. Relevo topología del sistema. - [Technique T1590](https://example.com)

   iv. Relevo mecanismos de seguridad presentes. - [Technique 1590](https://example.com)

   v. Relevo tecnologías utilizadas para la confección de la API. - [Technique T1595](https://example.com)

   vi. Relevo formatos y estilos estándar de las comunicaciones de los distintos proveedores de servicios utilizados en el sistema objetivo.

Weaponization:

Decido realizar ataques de phishing a las personas vinculadas al proyecto.
Decido preparar mails copiando los estilos utilizados en las comunicaciones de los proveedores de servicios del sistema objetivo.
Decido preparar un listado priorizado de mails a los cuales enviar los mensajes falsos. Se priorizan personas con menor seniority.
Decido preparar una landing page idéntica a la de uno de los proveedores con el objetivo de que la persona atacada ingrese sus credenciales.
Puedo, dado que conozco las IPs y la topología de la API, realizar un ataque de denegación de servicio.
Puedo, dado que conozco las tecnologías utilizadas en la API, explotar vulnerabilidades de los sistemas utilizados.
Delivery:

Envío mails simulando ser un peoveedor de servicios del sistema siguiendo el listado priorizado de personas.
Installation:

Cuando uno de los empleados ingrese las credenciales de acceso al sistema en la landing, guardo esos datos con el objetivo de utilizarlos cuantas veces sea necesario.
Command & Control:

Decido acceder a información relevante sobre la empresa y sus cientes.
Decido ingresar al sistema e invesigarlo por dentro.
Decido implementar un canal que me permita transferir datos desde el sistema atacado hacia mí.
Puedo alterar las credenciales de acceso al sistema.
Puedo alterar la configuración del sistema para provocar la caída del mismo.
Actions and objectives:

Extraigo toda la información posible sobre los clientes de la compañía atacada.
Extraigo toda la información posible de la compañía y sus sistemas para continuar profundizando el ataque.
