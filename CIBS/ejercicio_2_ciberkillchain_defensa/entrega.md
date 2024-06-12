# Ejercicio 2 - Defensa

## Alumno

Joaquin Horacio Gomez Codino

## Enunciado

Desarrollar la defensa en función del ataque planteado en orden inverso. No es una respuesta a un incidente, hay que detectar el ataque independientemente de la etapa.

Para cada etapa elegir una sola defensa, la más importante, considerar recursos limitados.

## Resolución

1. **Actions on Objectives:**

   - **Defensa:** Implementar la prevención de comportamiento en el endpoint. Esta técnica busca identificar y bloquear actividades maliciosas en los sistemas finales, como la exfiltración de datos sensibles. Al monitorear el comportamiento de los procesos y usuarios en los dispositivos finales, se pueden detectar acciones sospechosas que podrían indicar actividades de compromiso. ([Mitigación M1040: Behaviour prevention on endpoint](https://attack.mitre.org/mitigations/M1040/)

2. **Command & Control:**

   - **Defensa:** Implementar técnicas de protección de integridad de datos para detectar y prevenir la manipulación de datos sensibles, como el uso de firmas digitales y hash de datos para detectar cualquier alteración en los datos. ([Mitigación M1041: Encrypt sensitive information](https://attack.mitre.org/mitigations/M1041/))

3. **Installation:**

   - **Defensa:** Aplicar el principio de menor privilegio limitando los permisos de los usuarios y procesos en el sistema. Esto reducirá la capacidad del atacante para elevar sus privilegios y realizar acciones maliciosas. ([Mitigación M1026: Privileged Account Mangement](https://attack.mitre.org/mitigations/M1026/)

4. **Exploit:**

   - **Defensa:** Capacitar a los empleados para que reconozcan y eviten sitios web de phishing. La formación regular puede ayudar a los usuarios a identificar tácticas de ingeniería social. ([Mitigación M1017: User Training](https://attack.mitre.org/mitigations/M1017/)

5. **Delivery:**

   - **Defensa:** Realizar entrenamiento regular de concientización sobre seguridad para educar a los usuarios sobre las amenazas de phishing y cómo identificar correos electrónicos fraudulentos. Esto ayudará a reducir la probabilidad de que los usuarios caigan en el engaño y proporcionen información confidencial. ([Mitigación M1017: User Training](https://attack.mitre.org/mitigations/M1017/)

6. **Weaponization:**

   - **Defensa:** Restringir el contenido basado en web. Esto incluye el uso de filtros de contenido web para bloquear el acceso a sitios web maliciosos conocidos y el uso de listas blancas para limitar el acceso a sitios web aprobados. Esta medida puede evitar que los usuarios accedan a sitios web de phishing o descarguen contenido malicioso. ([Mitigación M1021: Restrict Web-Based Content](https://attack.mitre.org/mitigations/M1021/)

7. **Reconnaissance:**

   - **Defensa:** Monitorizar los registros de acceso y actividad en la plataforma para identificar intentos de enumeración de usuarios o escaneo de red. Además, limitar la cantidad de información sobre usuarios y topología del sistema que esté disponible públicamente para dificultar la recolección de información por parte de los atacantes. ([Mitigación M1043: Credential Access Protection](https://attack.mitre.org/mitigations/M1043/)
