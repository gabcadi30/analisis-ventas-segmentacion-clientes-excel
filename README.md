# Análisis de Ventas, Rentabilidad y Segmentación de Clientes | EXCEL
### Herramientas:
![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power_Query-Data_ETL-blue?style=for-the-badge)
![Power Pivot](https://img.shields.io/badge/Power_Pivot-Modeling-yellow?style=for-the-badge)
![DAX](https://img.shields.io/badge/DAX-Analysis-orange?style=for-the-badge)

## 1. 📌 Resumen 
Este proyecto analiza las ventas de Adventure Works con el propósito de identificar cómo se distribuyen los clientes y los ingresos, evaluar el valor y la frecuencia de compra de cada segmento y detectar oportunidades para mejorar la rentabilidad y la relación con los clientes.

Los clientes fueron clasificados en cuatro segmentos según su nivel de compra acumulada:

* Bronce
* Plata
* Oro
* Diamante

El análisis fue desarrollado en Excel, utilizando Power Query para la preparación de los datos, Power Pivot para el modelado y la creación de medidas, y tablas y gráficos dinámicos para construir el dashboard.

El periodo analizado comprende desde 2015 hasta el segundo trimestre de 2017. Los importes se presentan en dólares estadounidenses como convención para el análisis.
___________

## 2. 📊 Dashboard 
![Dashboard de Adventure Works](pictures/Dashboard.png)
*Nota.El presente dashboard permite analizar los resultados generales y filtrar la información por país.*
_____________
## 3. Fuente de Datos:
Los datos originales los pueden encontrar [Aquí](https://www.kaggle.com/datasets/sprasad018/adventureworks-dataset?utm_source=chatgpt.com&select=AdventureWorks_Products.csv)

El conjunto de datos contiene cinco tablas dimensionales con archivos CSV relacionados con clientes, productos, categorías y territorios. Además de una tabla de hechos con la información de las ventas.
_____________
## 4. 🎯 Objetivos:
Analizar el comportamiento comercial de los clientes de Adventure Works para determinar:

* **Analizar el desempeño de ventas en el tiempo:** 
Cómo evolucionaron los ingresos y la rentabilidad durante el periodo analizado.
* **Conocer a sus principales clientes y su comportamiento:**
Qué segmentos presentan mayor utilidad y margen de utilidad. Con qué frecuencia compran los clientes de cada segmento.Cuánto genera, en promedio, cada cliente.
* **Identificar los productos más y menos vendidos:** 
Qué categoría de producto predomina en cada segmento.
* **Analizar el desempeño por territorio:**
Cómo varían estos resultado según el país seleccionado.
_____________
## 5. 🛠️ Metodología 
El proyecto se desarrolló en las siguientes etapas:

1. Importación de los archivos CSV mediante Power Query.
2. Preparación y validación de los datos.
3. Construcción del modelo de datos y sus relaciones.
4. Segmentación de los clientes según su valor de compra.
5. Creación de medidas en Power Pivot.
6. Construcción de tablas dinámicas y del dashboard.

[Ver el proceso técnico completo](proceso_metodologico.md)



Para este proyecto se aplicó un flujo de trabajo optimizado, priorizando el rendimiento del modelo y la integridad de los cálculos.

1. Importación y preparación de los datos

**Carga y Optimización (ETL):** Los archivos CSV fueron integrados a través de **Power Query**, aplicando una estrategia de **Carga de conexión**  para optimizar el rendimiento de Excel y mantener un archivo ligero y ágil.
Durante esta etapa se revisaron los tipos de datos, la estructura de las tablas y los campos necesarios para relacionar la información de ventas, clientes, productos y territorios.


2. Construcción del modelo de datos

Las tablas fueron cargadas al modelo de datos de Excel y relacionadas mediante identificadores comunes.

Este modelo permitió analizar la información sin cargar todas las tablas como hojas independientes dentro del libro.

3. Segmentación de clientes

Los clientes fueron clasificados en Bronce, Plata, Oro y Diamante según su nivel de compra acumulada.

Esta segmentación corresponde a una clasificación descriptiva basada en reglas de negocio. No representa una segmentación estadística ni un modelo RFM.

4. Creación de medidas

Se crearon medidas para calcular los principales indicadores del análisis:

Métrica	Cálculo
Ingresos totales	Suma de los ingresos generados
Clientes	Conteo distinto de clientes
Cantidad de órdenes	Conteo distinto de órdenes
Ingreso por cliente	Ingresos totales / clientes únicos
Frecuencia de compra	Cantidad de órdenes / clientes únicos
Utilidad total	Ingresos – costos
Margen de utilidad	Utilidad total / ingresos totales
Participación de clientes	Clientes del segmento / clientes totales
Participación de ingresos	Ingresos del segmento / ingresos totales
5. Análisis temporal

La evolución de los ingresos y del margen de utilidad fue analizada trimestralmente.

Se eligió una comparación trimestral porque la información de 2017 solo está disponible hasta el segundo trimestre. Por este motivo, no se realizó una comparación entre años completos.

6. Construcción del dashboard

Finalmente, se utilizaron tablas dinámicas, gráficos combinados, formato condicional y un segmentador por país para presentar los resultados de manera visual e interactiva.

* **ETL y Limpieza de datos (Power Query):** Importación de datos mediante "Carga de conexión" para optimizar el uso de memoria.
    * Transformación de tipos de datos, creación de columnas de tiempo (Mes y año) a partir de la fecha original y consolidación de identidades (concatenación de nombres).
    * Eliminación de columnas irrelevantes para reducir el peso del modelo y mejorar el performance.
      
* **Modelado de datos (Star Schema):** Implementación de un **Modelo Estrella** en Power Pivot, estableciendo relaciones sólidas entre la *Fact Table* (`Sales`) y las *Dimension Tables* (`Customers`, `Products`, `Territories`, `Categories`,`Subcategories`). 
    * Configuración de integridad referencial para garantizar que todas las visualizaciones respondan de forma sincronizada.
      
* **Medidas DAX:** Desarrollo de medidas para **KPIs** base: Ingresos Totales, Margen, % Utilidad y Ticket Promedio.
    * **Lógica de Negocio:** Implementación de segmentación dinámica para categorizar a los 17,416 clientes según su volumen de consumo (Bronce, Plata, Oro y Diamante).
      
* **Diseño visual:** Diseño de interfaz profesional con una paleta de colores armonizada para facilitar la lectura de métricas críticas.
    * Uso de segmentadores dinámicos para un análisis interactivo por tiempo y región.
 
![Data Model Architecture](imagen/Star_schema.png)
*Figura 1: Arquitectura de Modelo Estrella implementada en Power Pivot.*
____________

## 4. 💡Insights
* **Contraste de Valor por Segmento:** Mientras que el segmento Bronce representa el mayor volumen de clientes (34.86%), el segmento Diamante sostiene la rentabilidad con un ticket promedio de **$2,058**.
* **Paradoja Regional:** Se identificó que Australia es un mercado de alto volumen pero baja eficiencia, mientras que **Canadá** es un mercado de bajo volumen pero máxima rentabilidad operativa.Esto indica que el costo de vender en Canadá es proporcionalmente más alto que en el resto del mundo.
* **Impacto de Diversificación:** La expansión de categorías en 2016 aumentó los ingresos en **$2.9M** y cambió la dinámica de adquisición hacia productos de menor ticket pero mayor frecuencia.
______________
## 5. Recomendaciones
* **Estrategia de Upselling:** Implementar campañas dirigidas al segmento Bronce (compradores de accesorios) para incentivarlos a adquirir productos de mayor valor, buscando elevar su *Customer Lifetime Value* (LTV).
* **Optimización de Márgenes:** Realizar un **análisis profundo de costos operativos** en la región de Australia para identificar fugas de rentabilidad o costos ocultos,además buscar replicar las políticas de eficiencia aplicadas en Canadá.
* **Fidelización del Segmento Diamante:** Crear programas de beneficios exclusivos para el segmento Diamante, dado que representan el motor financiero real del negocio a pesar de no ser el grupo más numeroso.

 👤 Autor
 
**Gabriela Cadillo** - *Junior Data Analyst*



