# Reporte de Análisis y Curación de Datos
**Proyecto:** Control de Calidad en Muestra de Ventas  
**Nivel:** Técnico-Competitivo

## 1. Resumen del Proceso
El objetivo de este análisis fue auditar y depurar un conjunto de datos inicial compuesto por **7 registros de ventas**. Durante la fase de diagnóstico estadístico, se observó de manera contundente la presencia de un dato fuera de rango (*outlier*) que distorsionaba el comportamiento financiero real del negocio.

Con el fin de garantizar la integridad del análisis para posteriores tomas de decisiones, se procedió a la fase de curación y limpieza. Mediante este proceso, se eliminó dicho registro anómalo del flujo principal, lo que dio origen a la creación de dos estructuras independientes: un DataFrame limpio y depurado compuesto por **6 registros óptimos**, y un DataFrame secundario que almacena la anomalía aislada para auditoría externa.

## 2. Evidencia y Validación Estadística
Para fundamentar técnicamente la remoción del registro, el análisis se acompañó de un **Diagrama de Caja (Boxplot)**. Esta herramienta visual permite validar el comportamiento del set de datos bajo los siguientes criterios objetivos:

* **Rango de Normalidad (El 50% de los datos):** La caja central del gráfico delimita visualmente el espacio donde se concentra la mitad de las transacciones más comunes del negocio (comprendidas estrictamente entre los cuartiles Q1 y Q3), reflejando una operación interna sana y compacta.
* **Identificación del Outlier:** El registro correspondiente al monto de **$9,500.00** se observa de manera clara, explícita y totalmente divorciada del cuerpo principal del gráfico, ubicándose mucho más allá de los límites máximos permitidos por los "bigotes" estadísticos.

## 3. Estructura de Entregables en este Repositorio
* `/ventas_operacion_limpias.csv`: Dataset prolijo con los 6 registros validados para operación.
* `/ventas_auditoria_anomalias.csv`: Dataset de auditoría con el outlier aislado.
* `/Reporte_Analisis_y_Curacion_Ventas.pdf`: Documentación formal ejecutiva en formato PDF.
