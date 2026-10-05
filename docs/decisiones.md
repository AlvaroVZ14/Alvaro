\# Decisiones del proyecto



\## 1. Propósito



Este documento registra las principales decisiones tomadas durante el desarrollo del prototipo y los criterios utilizados para definir la solución.



Las decisiones pueden modificarse a medida que se valide el funcionamiento real del proceso con Mente y Futuro.



\## 2. Uso de Streamlit



Se decidió utilizar \*\*Streamlit\*\* para desarrollar el prototipo de la aplicación.



\### Motivos



\* Permite desarrollar rápidamente una interfaz web utilizando Python.

\* Es adecuado para construir prototipos funcionales.

\* Facilita la visualización de datos.

\* Reduce la complejidad técnica necesaria para una primera versión.

\* Permite validar la propuesta antes de desarrollar una solución más compleja.



\## 3. Uso de Supabase



Se consideró \*\*Supabase\*\* como alternativa para almacenar los datos del sistema.



\### Motivos



\* Proporciona una base de datos PostgreSQL.

\* Permite acceder a los datos desde la aplicación.

\* Facilita una futura implementación de usuarios y permisos.

\* Es adecuado para un prototipo de pequeña escala.

\* Cuenta con un plan gratuito apropiado para la etapa inicial.



La integración completa con la aplicación todavía se encuentra pendiente de validación.



\## 4. Uso de datos de prueba



Durante el desarrollo del prototipo se decidió utilizar datos ficticios.



\### Motivos



\* Evitar utilizar información real de clientes durante las pruebas.

\* Permitir demostrar el funcionamiento del sistema sin depender de datos definitivos.

\* Facilitar las pruebas de las distintas pantallas.

\* Evitar exponer información sensible.



Por este motivo, casos como \*\*#2026-014\*\* corresponden exclusivamente a ejemplos ficticios.



\## 5. Prototipar antes de implementar



Se decidió construir primero un prototipo mínimo antes de completar toda la implementación.



El enfoque utilizado es:



```text

Necesidad

&#x20;  ↓

Prototipo mínimo

&#x20;  ↓

Validación

&#x20;  ↓

Ajustes

&#x20;  ↓

Implementación

```



Esto permite detectar errores en los requisitos antes de invertir tiempo en funcionalidades que podrían cambiar después de la validación.



\## 6. Centralización de información



Una de las principales decisiones funcionales fue centralizar la información relacionada con:



\* Solicitudes.

\* Casos.

\* Cotizaciones.

\* Ventas.

\* Seguimiento.



El objetivo es evitar que la información quede distribuida en distintos archivos o carpetas y facilitar su consulta.



\## 7. Estados del caso



El prototipo considera estados para representar el avance de cada caso.



Entre los estados utilizados como referencia se encuentran:



\* Solicitud.

\* Cotización.

\* Venta.

\* En seguimiento.



Estos estados son provisionales y deberán ser validados con la contraparte para determinar el flujo definitivo.



\## 8. Tarifas de referencia



Se decidió incorporar una tarifa de referencia para apoyar la elaboración de cotizaciones.



La tarifa no representa necesariamente el precio final del servicio.



El precio definitivo dependerá de las reglas que se validen con Mente y Futuro.



Entre las variables consideradas se encuentran:



\* Temática.

\* Horas.

\* Número de participantes.

\* Tipo de servicio.



\## 9. Reparto de ingresos



Durante el caso de uso de la presentación se utiliza un reparto de ejemplo entre la empresa y la persona encargada.



Este porcentaje \*\*no corresponde a una regla definitiva del negocio\*\*.



Los porcentajes reales deberán ser definidos y validados con la contraparte antes de incorporarlos como una regla del sistema.



\## 10. Seguridad de credenciales



Se decidió mantener las credenciales de servicios externos fuera del repositorio público.



Para esto se utiliza:



```text

.streamlit/secrets.toml

```



y se incluye el archivo en `.gitignore`.



De esta manera, las claves no forman parte del código publicado en GitHub.



\## 11. GitHub como repositorio central



Se decidió utilizar GitHub para centralizar el código y la documentación del proyecto.



El repositorio permite:



\* Mantener versiones del código.

\* Registrar cambios mediante commits.

\* Documentar decisiones.

\* Organizar tareas mediante issues.

\* Facilitar el trabajo colaborativo.



La rama principal utilizada es `main`.



\## 12. Alcance del prototipo



Se decidió mantener un alcance reducido para la primera versión.



\### Incluido



\* Registro de solicitudes.

\* Visualización de casos.

\* Tarifas de referencia.

\* Estados de casos.

\* Dashboard demostrativo.

\* Documentación técnica.



\### Fuera del alcance actual



\* Facturación real.

\* Integración con sistemas contables.

\* Automatización de pagos.

\* Gestión avanzada de usuarios.

\* Integraciones externas complejas.



Estas funcionalidades podrían considerarse en etapas posteriores si fueran necesarias.



\## 13. Decisiones pendientes



Existen aspectos que todavía deben validarse con la contraparte:



\* Flujo real de cierre de una venta.

\* Proceso de cobro.

\* Proceso de facturación.

\* Estados definitivos de los casos.

\* Cálculo de tarifas.

\* Reparto de ingresos.

\* Uso real del proceso descrito en la documentación entregada.

\* Indicadores prioritarios para el dashboard.



Estas decisiones se incorporarán al sistema una vez que sean confirmadas.



\## 14. Criterio general



La decisión general del proyecto es priorizar una solución:



\*\*Simple → útil → validable → escalable\*\*



La primera versión busca resolver la necesidad principal sin agregar complejidad innecesaria. A partir de la validación con Mente y Futuro, el sistema podrá evolucionar hacia una solución más completa.



