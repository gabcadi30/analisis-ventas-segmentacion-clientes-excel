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


## 2. 📊 Dashboard 
![Dashboard de Adventure Works](pictures/Dashboard.png)
*Nota.El presente dashboard permite analizar los resultados generales y filtrar la información por país.*

## 3. Fuente de Datos:
Los datos originales los pueden encontrar [Aquí](https://www.kaggle.com/datasets/sprasad018/adventureworks-dataset?utm_source=chatgpt.com&select=AdventureWorks_Products.csv)

El conjunto de datos contiene cinco tablas dimensionales con archivos CSV relacionados con clientes, productos, categorías y territorios. Además de una tabla de hechos con la información de las ventas.

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

## 5. 🛠️ Metodología 
El proyecto se desarrolló en las siguientes etapas:

1. Importación de los archivos CSV mediante Power Query.
2. Preparación y validación de los datos.
3. Construcción del modelo de datos y sus relaciones.
4. Segmentación de los clientes según su valor de compra.
5. Creación de medidas en Power Pivot.
6. Construcción de tablas dinámicas y del dashboard.

[Ver el proceso técnico completo](proceso_metodologico.md)

## 6. 💡Hallazgos Principales 

* Los ingresos se concentran en el segmento **Diamante**:
      Diamante representa el 30.84% de los clientes, pero genera el 82.61% de los ingresos. También registra el mayor ingreso promedio por cliente, con $3,832.07, y la mayor frecuencia de compra, con 1.86 órdenes por cliente.
      Esto convierte a Diamante en el segmento con mayor valor económico para la empresa.

*  **Bronce** tiene la mayor cantidad de clientes, pero una contribución reducida:
Bronce concentra el 34.86% de los clientes,la mayor participación entre los segmentos, pero aporta solamente el 1.30% de los ingresos.
Cada cliente Bronce genera aproximadamente $53.27 y realiza, en promedio, 1.06 órdenes, la frecuencia más baja del análisis.

*  **Plata** muestra una alta frecuencia de compra para su nivel de ingresos:
Los clientes Plata realizan, en promedio, 1.64 órdenes, superando a Oro. Sin embargo, el segmento representa solamente el 1.59% de los ingresos, debido a que su ingreso promedio por cliente es de $157.13.
Este comportamiento muestra que la frecuencia de compra no garantiza un alto valor económico cuando los montos de las compras son reducidos.

*  El segmento con mayor margen no es el que genera más utilidad:
Bronce presenta el mayor margen de utilidad, con 59.37%, pero genera una utilidad total de $191,994.39 debido a su bajo nivel de ingresos.
Diamante tiene un margen menor, de 41.78%, pero genera la mayor utilidad total, con $8,598,913.45.
Por lo tanto, el margen mide la rentabilidad proporcional, mientras que la utilidad total muestra cuánto dinero aporta realmente cada segmento.

*  La **categoría de producto** explica parte de las diferencias entre segmentos
La composición de ingresos cambia considerablemente según el segmento:
   * En Bronce, el 77.0% de los ingresos proviene de accesorios y el 23.0% de ropa.
   * En Plata, el 68.8% corresponde a accesorios y el 31.2% a ropa.
   * En Oro, el 93.9% de los ingresos proviene de bicicletas.
   * En Diamante, las bicicletas representan el 98.4% de sus ingresos.
Los segmentos de mayor valor están relacionados principalmente con la compra de bicicletas, mientras que Bronce y Plata concentran sus compras en accesorios y ropa.

* 6. Los ingresos crecieron sin deteriorar la rentabilidad
Los ingresos trimestrales presentan una **tendencia creciente** durante el periodo analizado.
El margen de utilidad pasó de aproximadamente 40.2% al inicio de 2015 a valores superiores al 42% durante 2016 y el primer semestre de 2017.
El mayor margen trimestral fue de aproximadamente 42.8%, registrado durante el tercer trimestre de 2016.

## 7. Conclusiones 
## 8. Recomendaciones
 

____________


 👤 Autor
 
**Gabriela Cadillo** - *Junior Data Analyst*



