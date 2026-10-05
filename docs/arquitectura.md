\# Arquitectura del sistema



\## 1. Descripción general



La solución propuesta corresponde a una aplicación web desarrollada en Python utilizando Streamlit como interfaz principal.



El sistema busca centralizar la información relacionada con solicitudes, casos, cotizaciones, ventas y seguimiento de los servicios de Mente y Futuro.



La arquitectura considera una separación entre la interfaz de usuario, el almacenamiento de datos y la visualización de indicadores.



\## 2. Arquitectura propuesta



```text

┌──────────────────────┐

│       Usuario        │

│ Cliente / Karen      │

└──────────┬───────────┘

&#x20;          │

&#x20;          ▼

┌──────────────────────┐

│      Streamlit       │

│   Aplicación web     │

└──────────┬───────────┘

&#x20;          │

&#x20;          ▼

┌──────────────────────┐

│      Supabase        │

│ Base de datos        │

│        casos         │

└──────────┬───────────┘

&#x20;          │

&#x20;          ▼

┌──────────────────────┐

│      Dashboard       │

│ Indicadores gestión  │

└──────────────────────┘

```



\## 3. Componentes



\### Streamlit



Streamlit se utiliza para construir la interfaz web del prototipo.



Actualmente contiene tres vistas principales:



\* Nueva solicitud.

\* Casos y cotizaciones.

\* Dashboard.



Su objetivo es proporcionar una interfaz sencilla para registrar y consultar información.



\### Supabase



Supabase se considera como la solución de almacenamiento de datos del sistema.



La base de datos propuesta permite almacenar información estructurada de los casos, como:



\* Cliente.

\* Temática.

\* Número de participantes.

\* Horas.

\* Estado.

\* Tarifa de referencia.



La integración completa entre Streamlit y Supabase queda pendiente de validación y desarrollo.



\### Dashboard



El dashboard permite transformar los datos registrados en información útil para la gestión.



Entre los indicadores considerados se encuentran:



\* Ventas por período.

\* Cantidad de casos.

\* Temáticas más solicitadas.

\* Distribución de ingresos.



La solución contempla el uso de Looker Studio para la visualización de estos indicadores.



\### GitHub



GitHub se utiliza para:



\* Control de versiones.

\* Almacenamiento del código.

\* Documentación.

\* Registro de cambios mediante commits.

\* Organización de tareas mediante issues.



\## 4. Flujo de información



El flujo general propuesto es:



```text

Solicitud del cliente

&#x20;       ↓

Registro del caso

&#x20;       ↓

Consulta de tarifa

&#x20;       ↓

Cotización

&#x20;       ↓

Aceptación del cliente

&#x20;       ↓

Registro de venta

&#x20;       ↓

Seguimiento

&#x20;       ↓

Dashboard

```



Cada etapa busca mantener la información centralizada y facilitar su consulta posterior.



\## 5. Seguridad



Las credenciales utilizadas para servicios externos no forman parte del código publicado.



La configuración sensible se mantiene en:



```text

.streamlit/secrets.toml

```



Este archivo está incluido en `.gitignore` para evitar que las credenciales sean subidas al repositorio.



\## 6. Estado de implementación



La arquitectura descrita corresponde a la solución propuesta y al prototipo desarrollado.



\### Implementado



\* Interfaz Streamlit.

\* Vista de nueva solicitud.

\* Vista de casos y cotizaciones.

\* Vista de dashboard.

\* Datos de prueba.

\* Repositorio GitHub.

\* Configuración para proteger credenciales.



\### Pendiente



\* Integración completa con Supabase.

\* Validación del flujo real con la contraparte.

\* Definición definitiva de tarifas y reparto.

\* Incorporación de datos reales.

\* Conexión definitiva del dashboard con la fuente de datos.



\## 7. Criterio de diseño



Se priorizó una solución simple y alcanzable, evitando una arquitectura innecesariamente compleja.



La idea principal es:



\*\*Registrar una vez → centralizar la información → obtener indicadores para gestionar.\*\*



La arquitectura podrá ajustarse después de validar el proceso real con Mente y Futuro.



