# Implementacion-DLP-USB
Proyecto de ciberseguridad para prevención de fuga de datos (DLP) mediante bloqueo de puertos USB en Windows
# Política Corporativa de Prevención de Pérdida de Datos (DLP)

## 1. Introducción al Data Loss Prevention (DLP)
En el entorno digital actual, los datos son el activo más valioso de nuestra organización. El **Data Loss Prevention (DLP)** se define como un conjunto de estrategias, procedimientos y herramientas tecnológicas diseñadas para garantizar que la información sensible no salga de la red corporativa de manera no autorizada.

La implementación de estas políticas es crucial para:
* Proteger la propiedad intelectual y los datos personales de clientes (PII).
* Cumplir con normativas legales (GDPR, ISO 27001).
* Preservar la reputación de la organización frente a filtraciones accidentales o malintencionadas.

## 2. Clasificación de Datos
Para aplicar medidas de protección efectivas, la información se clasifica en tres niveles de sensibilidad:

	**Nivel 1: Datos Públicos**
    **Definición:** Información que puede ser divulgada sin riesgo alguno para la organización.
     **Ejemplos:** Material de marketing, notas de prensa, información publicada en el sitio web oficial.
	**Nivel 2: Datos de Uso Interno**
    * **Definición:** Información destinada exclusivamente a empleados. Su divulgación causaría inconvenientes operativos o pérdida de ventaja competitiva leve.
    * **Ejemplos:** Directorios de empleados, manuales de procedimientos, memorandos internos, políticas de la empresa.
	**Nivel 3: Datos Sensibles / Confidenciales**
    * **Definición:** Información crítica cuya filtración causaría daños financieros, legales o reputacionales graves. Requiere los controles más estrictos.
    * **Ejemplos:** Datos bancarios, contraseñas, bases de datos de clientes, propiedad intelectual (código fuente), estrategias de negocio futuras.

## 3. Acceso y Control (Principio del Menor Privilegio)
El acceso a la información se rige estrictamente por el **Principio del Menor Privilegio (PoLP)**: un usuario solo debe tener acceso a los datos estrictamente necesarios para desempeñar sus funciones laborales actuales.

### Flujo de Revisión de Permisos:
1.  **Solicitud:** El empleado solicita acceso justificando la necesidad operativa.
2.  **Aprobación:** El "Data Owner" (Propietario del Dato) o el Gerente del área debe aprobar la solicitud.
3.  **Revisión Periódica:**
    * **Responsable:** CISO (Chief Information Security Officer) junto con Gerentes de Área.
    * **Frecuencia:** Trimestral.
    * **Acción:** Se auditan los accesos vigentes. Cualquier permiso que ya no sea justificable (por cambio de puesto o fin de proyecto) será revocado inmediatamente.

## 4. Monitoreo y Auditoría
Para garantizar el cumplimiento de estas políticas, se implementará un sistema de vigilancia continua:

* **Regla de Monitoreo:** Todo acceso, modificación, copiado o eliminación de datos clasificados como "Sensibles" generará un registro de evento (log).
* **Herramientas:**
    * **SIEM (Security Information and Event Management):** Para centralizar y correlacionar alertas de seguridad en tiempo real.
    * **Auditoría de Logs:** Revisión mensual de los intentos de acceso denegados y transferencias de archivos sospechosas.

## 5. Prevención de Filtraciones (Implementación Técnica)
Se desplegarán barreras tecnológicas para evitar la exfiltración de datos:

* **Cifrado:** Uso de cifrado (ej. BitLocker) en todos los dispositivos portátiles y cifrado TLS para datos en tránsito.
* **Restricción de Puertos (USB):** Se bloqueará la capacidad de escritura y lectura en puertos USB para dispositivos de almacenamiento masivo en todos los endpoints, excepto para personal de TI autorizado.
* **Filtrado Web:** Bloqueo de acceso a sitios de almacenamiento en la nube no corporativos (Dropbox personal, Mega, etc.).

## 6. Educación y Concientización
El usuario es la primera línea de defensa. La estrategia educativa incluye:
* **Capacitación Obligatoria:** Cursos semestrales sobre manejo seguro de datos y reconocimiento de Ingeniería Social.
* **Acuerdos de Confidencialidad (NDA):** Firma obligatoria al inicio del contrato laboral.
* **Simulacros:** Pruebas de Phishing periódicas para evaluar y reforzar la respuesta del personal ante amenazas.
