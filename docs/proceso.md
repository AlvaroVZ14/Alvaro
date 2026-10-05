\# Proceso de gestión propuesto



\## 1. Objetivo



El proceso propuesto busca ordenar y centralizar la gestión de las solicitudes, cotizaciones, ventas y seguimiento de los servicios de Mente y Futuro.



La finalidad es que la información de cada servicio pueda ser registrada una sola vez y posteriormente utilizada para consultar el estado del caso y obtener indicadores de gestión.



\## 2. Flujo general



El proceso propuesto es:



```text

Solicitud

&#x20;   ↓

Registro del caso

&#x20;   ↓

Consulta de tarifa de referencia

&#x20;   ↓

Cotización

&#x20;   ↓

¿Cliente acepta?

&#x20;  ↙        ↘

&#x20;No          Sí

&#x20;↓            ↓

Fin      Registro de venta

&#x20;             ↓

&#x20;        Seguimiento

&#x20;             ↓

&#x20;         Dashboard

```



\## 3. Descripción de las etapas



\### 3.1 Solicitud



El proceso comienza cuando un cliente solicita un servicio de Mente y Futuro.



La solicitud puede incluir información como:



\* Cliente.

\* Temática.

\* Número de participantes.

\* Cantidad de horas.

\* Tipo de servicio.



\### 3.2 Registro del caso



La solicitud se registra en la aplicación y se genera un caso.



El caso permite mantener agrupada la información relacionada con el servicio y realizar su seguimiento.



Como ejemplo para el prototipo se utiliza el caso:



\*\*#2026-014\*\*



Los datos utilizados en este ejemplo son ficticios.



\### 3.3 Consulta de tarifa



Una vez registrado el caso, se consulta una tabla de tarifas de referencia.



La tarifa puede considerar variables como:



\* Temática.

\* Cantidad de horas.

\* Número de participantes.

\* Tipo de servicio.



La tarifa mostrada por el sistema corresponde a una referencia y no reemplaza la decisión final de la persona encargada.



\### 3.4 Cotización



Con la información del caso y la tarifa de referencia se prepara la cotización para el cliente.



El cliente puede aceptar o rechazar la propuesta.



\### 3.5 Aceptación



Si el cliente no acepta la cotización, el caso termina o queda registrado según las reglas que posteriormente se definan con la contraparte.



Si el cliente acepta, se continúa con el registro de la venta.



\### 3.6 Registro de venta



Cuando la cotización es aceptada, se registra la venta asociada al caso.



En esta etapa se deberán definir y validar con la contraparte aspectos como:



\* Monto final.

\* Forma de pago.

\* Fecha de cobro.

\* Estado del pago.

\* Facturación.

\* Distribución de los ingresos.



\### 3.7 Seguimiento



Después de registrar la venta, el caso puede pasar a un estado de seguimiento.



Esto permite conocer qué servicios se encuentran pendientes, en desarrollo o finalizados.



Los estados definitivos deberán ser validados con la contraparte.



\### 3.8 Dashboard



La información registrada puede utilizarse para generar indicadores de gestión.



Entre los indicadores propuestos se encuentran:



\* Ventas por mes.

\* Cantidad de casos.

\* Temáticas más solicitadas.

\* Horas de servicio.

\* Distribución de ingresos.

\* Períodos con y sin ventas.



\## 4. Ejemplo de caso de uso



Para demostrar el funcionamiento del proceso se utiliza el siguiente ejemplo ficticio:



\*\*Cliente:\*\* Empresa industrial

\*\*Participantes:\*\* 20

\*\*Horas:\*\* 8

\*\*Temática:\*\* Trabajo en equipo

\*\*Caso:\*\* #2026-014



El cliente solicita el servicio y la información se registra en la aplicación.



El sistema crea el caso y permite consultar una tarifa de referencia.



Karen revisa la información y prepara la cotización.



Si el cliente acepta, se registra la venta y el caso pasa a seguimiento.



Finalmente, la información de la venta puede aparecer en el dashboard para facilitar el análisis mensual.



\## 5. Roles involucrados



\### Cliente



\* Solicita el servicio.

\* Entrega la información necesaria.

\* Revisa y acepta o rechaza la cotización.



\### Karen / Mente y Futuro



\* Registra y revisa los casos.

\* Consulta tarifas de referencia.

\* Prepara las cotizaciones.

\* Registra las ventas.

\* Realiza el seguimiento.



\### Sistema



\* Centraliza la información.

\* Mantiene los datos de los casos.

\* Permite consultar tarifas.

\* Calcula o presenta indicadores.

\* Alimenta el dashboard.



\## 6. Información pendiente de validar



El proceso presentado corresponde a una propuesta inicial y debe ser validado con la contraparte.



Las principales preguntas pendientes son:



\* ¿Cómo se cierra actualmente una venta?

\* ¿Cuándo se considera efectivamente realizada una venta?

\* ¿Cómo se realiza el cobro?

\* ¿Cómo se registra la facturación?

\* ¿Existe un porcentaje definido para el reparto de ingresos?

\* ¿Qué estados debería tener un caso?

\* ¿El proceso descrito en la documentación entregada corresponde al proceso utilizado actualmente?



Estas validaciones permitirán ajustar el prototipo antes de implementar el flujo definitivo.



\## 7. Relación con el BPMN



El flujo descrito puede representarse mediante un diagrama BPMN utilizando tres participantes principales:



```text

Cliente          Karen / Mente y Futuro          Sistema



&#x20;  │                       │                       │

&#x20;  │── Solicitud ─────────>│                       │

&#x20;  │                       │── Registrar caso ────>│

&#x20;  │                       │<── Caso creado ───────│

&#x20;  │                       │── Consultar tarifa ──>│

&#x20;  │                       │<── Tarifa referencia ─│

&#x20;  │                       │                       │

&#x20;  │<── Cotización ────────│                       │

&#x20;  │                       │                       │

&#x20;  │── Aceptación ────────>│                       │

&#x20;  │                       │── Registrar venta ───>│

&#x20;  │                       │                       │

&#x20;  │                       │<── Indicadores ───────│

&#x20;  │                       │                       │

&#x20;  │                       │       Dashboard       │

```



El BPMN representa el \*\*proceso propuesto\*\*, por lo que sus etapas y reglas podrán modificarse después de la validación con la contraparte.



