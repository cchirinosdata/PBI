# Tracking de Visitas - Proyecto Piloto "Volar"

Este repositorio contiene la documentación del dashboard de seguimiento para el Proyecto Piloto "Volar", desarrollado en Power BI.

***

## 📝 Descripción del Proyecto

El objetivo principal de este proyecto es realizar un seguimiento exhaustivo de las visitas y reuniones del proyecto. El dashboard permite:

* Conocer la disponibilidad (vacancia) de fechas para nuevas reuniones.
* Visualizar el estado actual de las reuniones (realizadas, pendientes, canceladas).
* Ubicar geográficamente dónde se están llevando a cabo.
* Analizar las rutas de desplazamiento de los visitantes a las cunas.

***

## 👨‍💻 Autor

* Claudia Chirinos

***

## 🛠️ Herramientas y Pre-requisitos

* **Microsoft Power BI:** Para la visualización de datos y creación del dashboard.
* **Microsoft Excel:** Como fuente de datos principal.
* **SQL:** Para consultas y manipulación de datos.

***

## 📊 Fuente de Datos

La información proviene de una base de datos centralizada y confidencial en **Excel**, la cual contiene el registro de todos los usuarios y sus interacciones con las cunas del proyecto.

***

## 💡 Transformaciones Clave en DAX

Para el análisis, se utilizaron fórmulas DAX (Data Analysis Expressions) dentro de Power BI. Una de las métricas clave fue el cálculo del porcentaje de avance de visitas.

**Ejemplo de medida DAX:**

```dax
-- Ejemplo de cómo calcular el porcentaje de visitas completadas
Porcentaje Avance = 
DIVIDE(
    CALCULATE(COUNTROWS('Visitas'), 'Visitas'[Status] = "Realizada"),
    COUNTROWS('Visitas')
)
