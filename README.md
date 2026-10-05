\# Integrador Transversal — Mente y Futuro



\## Descripción



Este proyecto corresponde al desarrollo de un prototipo de sistema de información para \*\*Mente y Futuro\*\*, con el objetivo de centralizar y ordenar la información relacionada con solicitudes, casos, cotizaciones, ventas y seguimiento de servicios.



Actualmente, parte de esta información se encuentra distribuida en distintos archivos y carpetas, lo que dificulta su consulta y seguimiento.



La propuesta consiste en desarrollar una aplicación web sencilla que permita registrar los casos y visualizar información relevante para apoyar la gestión del negocio.



\## Objetivo



Desarrollar un prototipo funcional que permita:



\* Registrar nuevas solicitudes de clientes.

\* Centralizar los casos en un solo lugar.

\* Consultar información de los casos y cotizaciones.

\* Mostrar tarifas de referencia.

\* Registrar el estado de cada caso.

\* Visualizar información de ventas mediante un dashboard.

\* Facilitar el seguimiento de los servicios realizados.



\## Tecnologías utilizadas



\* \*\*Python\*\*: lenguaje principal del proyecto.

\* \*\*Streamlit\*\*: desarrollo de la interfaz web.

\* \*\*Pandas\*\*: manejo y visualización de datos.

\* \*\*Supabase\*\*: base de datos propuesta para almacenar la información.

\* \*\*Looker Studio\*\*: herramienta considerada para la visualización del dashboard.

\* \*\*GitHub\*\*: control de versiones, documentación y gestión del proyecto.



\## Funcionalidades del prototipo



\### Nueva solicitud



Permite ingresar información básica de una solicitud:



\* Cliente.

\* Temática.

\* Número de participantes.

\* Cantidad de horas.

\* Estado del caso.



\### Casos y cotizaciones



Permite visualizar los casos registrados y consultar información como:



\* Cliente.

\* Temática.

\* Participantes.

\* Horas.

\* Estado.

\* Tarifa de referencia.



\### Dashboard



El prototipo contempla una vista de indicadores para apoyar la gestión, como:



\* Ventas mensuales.

\* Cantidad de casos.

\* Temáticas más solicitadas.

\* Distribución de ingresos.



\## Flujo propuesto



El proceso general considerado para la solución es:



\*\*Solicitud → Caso → Tarifa de referencia → Cotización → Venta → Seguimiento → Dashboard\*\*



Este flujo corresponde a la propuesta desarrollada a partir del levantamiento de información y queda sujeto a validación con la contraparte.



\## Arquitectura propuesta



```text

Usuario

&#x20;  │

&#x20;  ▼

Streamlit

&#x20;  │

&#x20;  ▼

Supabase

&#x20;  │

&#x20;  ▼

Datos de casos y ventas

&#x20;  │

&#x20;  ▼

Dashboard

```



La aplicación utiliza Streamlit como interfaz. Supabase se considera como la base de datos para almacenar la información y el dashboard permite visualizar los principales indicadores de gestión.



\## Datos de prueba



El prototipo utiliza \*\*datos ficticios de prueba\*\* para demostrar el funcionamiento de las pantallas y del flujo propuesto.



Los datos mostrados no representan información real de clientes ni ventas de Mente y Futuro.



\## Estado actual



El proyecto cuenta actualmente con un prototipo funcional desarrollado en Streamlit que incluye:



\* Pantalla de nueva solicitud.

\* Vista de casos y cotizaciones.

\* Vista de dashboard.

\* Datos de prueba.

\* Repositorio GitHub.

\* Configuración para mantener las credenciales fuera del repositorio.



La integración completa con la base de datos y la validación definitiva del proceso quedan como trabajo pendiente.



\## Seguridad



Las credenciales de conexión a servicios externos se almacenan mediante:



```text

.streamlit/secrets.toml

```



Este archivo se encuentra excluido del repositorio mediante `.gitignore`.



\*\*No se deben subir claves, contraseñas ni credenciales al repositorio.\*\*



\## Estructura del proyecto



```text

IntegradorTransversal/

├── app.py

├── README.md

├── requirements.txt

├── .gitignore

└── docs/

&#x20;   ├── arquitectura.md

&#x20;   ├── proceso.md

&#x20;   └── decisiones.md

```



\## Ejecución local



\### 1. Instalar las dependencias



```bash

pip install -r requirements.txt

```



\### 2. Ejecutar la aplicación



```bash

python -m streamlit run app.py

```



La aplicación se abrirá en el navegador mediante la dirección local proporcionada por Streamlit.



\## Proyecto académico



Este proyecto forma parte del \*\*Integrador Transversal\*\* y del trabajo de \*\*Aprendizaje + Servicio (A+S)\*\*, aplicando conocimientos de desarrollo de sistemas, gestión de datos y visualización para abordar una necesidad identificada junto a una contraparte real.



\## Próximos pasos



\* Validar con Karen el proceso real de cierre, cobro y facturación.

\* Confirmar cómo se calculan las tarifas y el reparto de los ingresos.

\* Validar el flujo descrito en la documentación.

\* Completar la integración con Supabase.

\* Conectar los datos reales con el dashboard.

\* Ajustar el sistema según las validaciones realizadas.



