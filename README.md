# Pizza Sales Analysis Report/Dasboard
Page 1 "Home"


![2024-04-09](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/d669020c-650a-421f-9c29-fc902d4ffbc9)

Page 1 "Best and Worst Sellers"


![2024-04-08 (1)](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/3a0d6a30-c9dc-4830-adf9-9d3818b3a19e)


### Table of content
### ENGLISH
- [About the project](#About-the-project)
- [Objectives](#Objectives)
- [Scope](#Scope)
- [Project Steps](#Project-Steps)
- [Source of Data](#Source-of-Data)
- [Used tools, softwares and platforms](#Used-tools-softwares-and-platforms)
- [Findings](#Findings)
- [Conclusions, Limitations and Recommendations](#Conclusions-Limitations-and-Recommendations)

### ESPAÑOL
- [Sobre el proyecto](#Sobre-el-proyecto)
- [Objetivos](#Objetivos)
- [Alcance](#Alcance)
- [Pasos del Proyecto](#Pasos-del-Proyecto)
- [Fuente de Datos](#Fuente-de-Datos)
- [Herramientas, Softwares y Plataformas Utilizadas](#Herramientas-Softwares-y-Plataformas-Utilizadas)
- [Descubrimientos](#Descubrimientos)
- [Conclusiones, limitaciones y recomendaciones](#Conclusiones-limitaciones-y-recomendaciones)


### About the project
This analysis is a Data Analysis Project involving transaction data occurring between 01/1/2010 and 12/12/2015 for a physical Pizza store registered in the United States. The company mainly sells different flavors of Pizza, opening in a range of 11 hours a day, everyday. The dataset contain detailed information about pizza orders, including specifics about the pizza variants, quantities, pricing, dates, times, and categorization details.

### Objectives
This analysis will determine the overall performance of sales of the products, grouped by category, number of orders, revenue, quantity, size, week, and hour of the day in order to identify patterns and insights that allow the analyst to pinpoint areas for improvement for later use by the company's management.

### Scope
This project aims to provide an effective report and ETL process related to the sales movements of the Pizza Store over the course of a year for subsequent utilization and analysis. The report and table will allow the company to investigate and find relationships between sales volume, categories, quantity per order, and more. The goal is to identify patterns, obtain clear, up-to-date, and accessible information for subsequent decision-making.

### Project Steps

1. Obtain Data Set Online and download it to local machine.
2. Set goals to detect KPIs and plan charts that meet the needs:

#### KPIs:

- Total Revenue: The sum of the total price of all pizza orders.
- Average Order Value: The average amount spent per order, calculated by dividing the total revenue by the total number of orders.
- Total Pizzas Sold: The sum of the quantities of all pizzas sold.
- Total Orders: The total number of orders placed.
- Average Pizzas Per Order: The average number of pizzas sold per order, calculated by dividing the total number of pizzas sold by the total number of orders.

#### Visualization Charts:

- Hourly Trend for Total Pizzas Sold: Create a stacked bar chart that displays the hourly trend of total orders over a specific time period. This chart will help us identify any patterns or fluctuations in order volumes on an hourly basis.
- Weekly Trend for Total Orders: Create a line chart that illustrates the weekly trend of total orders throughout the year. This chart will allow us to identify peak weeks or periods of high order activity.
- Percentage of Sales by Pizza Category: Create a pie chart that shows the distribution of sales across different pizza categories. This chart will provide insights into the popularity of various pizza categories and their contribution to overall sales.
- Percentage of Sales by Pizza Size: Generate a pie chart that represents the percentage of sales attributed to different pizza sizes. This chart will help us understand customer preferences for pizza sizes and their impact on sales.
- Total Pizzas Sold by Pizza Category: Create a funnel chart that presents the total number of pizzas sold for each pizza category. This chart will allow us to compare the sales performance of different pizza categories.
- Top 5 Best Sellers by Revenue, Total Quantity, and Total Orders: Create a bar chart highlighting the top 5 best-selling pizzas based on Revenue, Total Quantity, Total Orders. This chart will help us identify the most popular pizza options.
- Bottom 5 Best Sellers by Revenue, Total Quantity, and Total Orders: Create a bar chart showcasing the bottom 5 worst-selling pizzas based on Revenue, Total Quantity, Total Orders. This chart will enable us to identify underperforming or less popular pizza options.

3. Create Database in SQL Server and import file.
4. Create queries for each KPI and visualization chart in SQL Server to subsequently create a report with the aim of conducting future checks.

#### KPI's Queries:

a) Total revenue

SELECT SUM(total_price) AS Total_revenue
FROM pizza_sales
Output:
 
![Total revenue](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/1fb9b829-da08-4293-95cc-486d2713a554)

b) Average Order Value

SELECT SUM(total_price)/COUNT(DISTINCT order_id) AS Average_order_value
FROM pizza_sales
Output:

![SQL Avg Order Value](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/5aec33ca-b688-42dc-bccd-ab3a3eb2de26)

c) Total Pizzas Sold
	
SELECT SUM(quantity) AS Total_Pizzas_Sold
FROM pizza_sales
Output:
 
![Total Pizzas Sold](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/de1c421c-046b-4b40-869b-59e3753f9dc6)


d) Total Orders

SELECT COUNT(DISTINCT order_id) AS Total_orders
FROM pizza_sales

Output:

![Total Orders](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/fdf01cee-aef3-4c93-bc70-bb12d133e9c9)


e) Average Pizzas per Order

SELECT SUM(quantity)/COUNT(DISTINCT order_id) AS Average_Pizzas_per_Order
FROM pizza_sales

Output:

![Avg Pizzas per Order](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/bf4d7275-92f3-419c-8aa6-972ceea02494)


f) Average Pizzas per Order 2 DECIMALS
	
SELECT CAST(CAST(SUM(quantity) AS DECIMAL (10,2)) / 
CAST(COUNT(DISTINCT order_id) AS DECIMAL (10,2)) AS DECIMAL (10,2)) AS Average_Pizzas_per_Order
FROM pizza_sales
Output:

![Avg pizzas per order 2 decimals](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/039ed1ba-1281-4c66-95bf-6e726acf2017)


#### Chart Queries:

a)	Hourly Trend for Total Pizzas Sold:

SELECT DATEPART(HOUR, order_time) AS order_hour,
      SUM(quantity) AS Total_pizzas_Sold
FROM pizza_sales
GROUP BY DATEPART(HOUR, order_time)
ORDER BY DATEPART(HOUR, order_time)

Output:
 
![Hourly Trend for Total Pizzas Sold](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/18d58c64-95f7-441c-8fdf-dad9f19d3a59)


b)	Weekly Trend for Total Orders:


SELECT  DATEPART(ISO_WEEK, order_date) AS Week_number,
		YEAR(order_date) AS Order_year,
        COUNT(DISTINCT order_id) AS Total_orders
FROM pizza_sales
GROUP BY DATEPART(ISO_WEEK, order_date),
		YEAR(order_date)  
ORDER BY DATEPART(ISO_WEEK, order_date), 
		YEAR(order_date)  

Output:

![ISO Weekly Trend for Total Orders](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/3057cfb5-4f66-4651-8306-978bd2ecdab8)
![ISO Weekly Trend for Total Orders 2](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/74f26ead-82fc-43bf-8790-28ecc77b9695)



c)	Percentage of Sales by Pizza Category:


SELECT pizza_category,
		SUM(total_price) AS Total_sales,
		SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales) AS Percentage_of_sales
FROM pizza_sales
--WHERE MONTH(order_date) = 1 --January / APLICABLE A TODOS LOS QUERIES PARA FILTRAR POR MES/FECHA *TAMBIEN DEBE IR EN SUBQUERY*
GROUP BY pizza_category


Output:
 
![Percentage of Sales by Pizza Category](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/d8dcf443-16a1-45c8-a889-8f2f6fe26c50)

d)	Percentage of Sales by Pizza Size:


SELECT pizza_size,
		CAST(SUM(total_price) AS DECIMAL (10,2)) as Total_sales,
		CAST(SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales) AS DECIMAL (10,2)) AS Percentage_of_sales 
FROM pizza_sales
--WHERE pizza_size = 'M' --January / APLICABLE A TODOS LOS QUERIES PARA FILTRAR POR MES/FECHA *TAMBIEN DEBE IR EN SUBQUERY*
GROUP BY pizza_size
ORDER BY pizza_size

Output:

 ![Percentage of Sales by Pizza Size](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/0b5474c1-a4f0-4919-b96d-a932fedac617)


e)	Total Pizzas Sold by Pizza Category:


SELECT pizza_category, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_category
ORDER BY pizza_category ASC

Output:

 ![Total Pizzas Sold by Pizza Category](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/c5b473a0-bc5f-4bcf-b463-d1ebff98b09b)


f)	Top 5 Best Sellers by Revenue, Total Quantity and Total Orders

By Revenue: 

SELECT TOP 5 pizza_name, SUM(total_price) AS Total_revenue
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_revenue DESC

Output:

![Top 5 Best Sellers by Revenue](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/8397ea2c-75d3-4c71-983e-9d1dacc439b9)


By Quantity: 

SELECT TOP 5 pizza_name, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_quantity DESC

Output:
 
![Top 5 Best Sellers by Total Quantity](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/51f3fd7b-8e0d-4582-be5a-df655ccd38ad)

By Orders: 

SELECT TOP 5 pizza_name, COUNT(distinct order_id) AS Total_orders
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_orders DESC

Output:
 
![Top 5 Best Sellers by Total Orders](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/435dac65-3010-46de-82f4-bb196da5f0ef)



g)	Bottom 5 Best Sellers by Revenue, Total Quantity and Total Orders


By Revenue: 

SELECT TOP 5 pizza_name, CAST(SUM(total_price) AS DECIMAL (10,2)) AS Total_revenue
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_revenue ASC
	
Output:

 ![Bottom 5 Best Sellers by Revenue](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/feb4a3e9-f291-4db2-8d15-902f453bc200)


By Quantity:
SELECT TOP 5 pizza_name, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_quantity ASC

Output:
 
![Bottom 5 Best Sellers by Total Quantity](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/d612b483-5e02-467d-9e73-b4e265a039c2)


By Orders:


SELECT TOP 5 pizza_name, COUNT(distinct order_id) AS Total_orders
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_orders ASC

Output:

![Bottom 5 Best Sellers by Total Orders](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/9e0ccb67-7037-4a21-b375-8ee61cc02227)
6. Import data into Tableau Public.
7. Process the data in Tableau Public.
8. Create Report/Dashboard 1 "Home".
9. Create Report/Dashboard 2 "Best and Worst Sellers".
   



### Source of Data
Source: [https://www.kaggle.com/datasets/carrie1/ecommerce-data?resource=download](https://www.kaggle.com/datasets/nextmillionaire/pizza-sales-dataset)
The dataset was downloaded to the local machine and subsequently uploaded to Google Drive under the name "data".

### Used tools, softwares and platforms
- SQL Server
- Tableau
- Microsoft Word
- www.Canva.com
- www.Flaticon.com

### Findings


### Conclusions, Limitations and Recommendations

The data analysis project provides valuable insights into sales performance across different product categories.
The interactive dashboard offers a user-friendly interface for exploring and interpreting data, facilitating informed decision-making.
Recommendations for future improvements may include incorporating predictive analytics models to forecast sales trends and integrating additional data sources for comprehensive and deeper analysis regarding factors affecting the sales performance of each product in each category.

## ES - Analisis de Ventas de Ecommerce
  
### Sobre el proyecto
Este análisis es un Proyecto de Análisis de Datos que involucra datos de transacciones ocurridas entre el 01/01/2010 y el 12/12/2015 para una tienda física de pizzas registrada en los Estados Unidos. La empresa vende principalmente diferentes sabores de pizza, abriendo en un rango de 11 horas al día, todos los días. El conjunto de datos contiene información detallada sobre pedidos de pizza, incluyendo especificaciones sobre las variantes de pizza, cantidades, precios, fechas, horas y detalles de categorización.

### Objetivos
Este análisis determinará el rendimiento general de las ventas de los productos, agrupados por categoría, número de pedidos, ingresos, cantidad, tamaño, semana y hora del día con el fin de identificar patrones y conocimientos que permitan al analista señalar áreas de mejora para su posterior uso por parte de la dirección de la empresa.

### Alcance
Este proyecto tiene como objetivo proporcionar un informe efectivo y un proceso de ETL relacionado con los movimientos de ventas de la Tienda de Pizzas durante el transcurso de un año para su posterior utilización y análisis. El informe y la tabla permitirán a la empresa investigar y encontrar relaciones entre el volumen de ventas, las categorías, la cantidad por pedido y más. El objetivo es identificar patrones, obtener información clara, actualizada y accesible para la toma de decisiones posterior.

### Pasos del Proyecto
1. Obtener Data Set Online y descargarlo en maquina local.
2. Establecer objetivos para detectar KPI’s y planificar gráficos que cumplan con las necesidades:

#### KPI’s:

- Ingresos Totales: La suma del precio total de todos los pedidos de pizza.
- Valor Promedio del Pedido: El monto promedio gastado por pedido, calculado dividiendo los ingresos totales por el número total de pedidos.
- Total de Pizzas Vendidas: La suma de las cantidades de todas las pizzas vendidas.
- Total de Pedidos: El número total de pedidos realizados.
- Promedio de Pizzas por Pedido: El número promedio de pizzas vendidas por pedido, calculado dividiendo el total de pizzas vendidas por el número total de pedidos.

#### Gráficos de Visualización:

- Tendencia Horaria para Total de Pizzas Vendidas: Crear un gráfico de barras apiladas que muestre la tendencia horaria de los pedidos totales durante un período de tiempo específico. Este gráfico nos ayudará a identificar cualquier patrón o fluctuación en los volúmenes de pedidos por hora.
- Tendencia Semanal para Total de Pedidos: Crear un gráfico de líneas que ilustre la tendencia semanal de los pedidos totales a lo largo del año. Este gráfico nos permitirá identificar las semanas pico o los períodos de alta actividad de pedidos.
- Porcentaje de Ventas por Categoría de Pizza: Crear un gráfico circular que muestre la distribución de ventas entre diferentes categorías de pizza. Este gráfico proporcionará información sobre la popularidad de las diversas categorías de pizza y su contribución a las ventas totales.
- Porcentaje de Ventas por Tamaño de Pizza: Generar un gráfico circular que represente el porcentaje de ventas atribuidas a diferentes tamaños de pizza. Este gráfico nos ayudará a comprender las preferencias de los clientes por los tamaños de pizza y su impacto en las ventas.
- Total de Pizzas Vendidas por Categoría de Pizza: Crear un gráfico de embudo que presente el número total de pizzas vendidas para cada categoría de pizza. Este gráfico nos permitirá comparar el rendimiento de ventas de diferentes categorías de pizza.
- Top 5 Mejores Ventas por Ingresos, Cantidad Total y Total de Pedidos: Crear un gráfico de barras que destaque las 5 mejores pizzas más vendidas basadas en los ingresos, la cantidad total y los pedidos totales. Este gráfico nos ayudará a identificar las opciones de pizza más populares.
- Top 5 Peores Ventas por Ingresos, Cantidad Total y Total de Pedidos: Crear un gráfico de barras que muestre las 5 pizzas menos vendidas basadas en los ingresos, la cantidad total y los pedidos totales. Este gráfico nos permitirá identificar las opciones de pizza menos populares o con bajo rendimiento.

3. Crear Database en SQL Server e importar file
4. Crear consultas para cada KPI y gráfico de visualización en SQL Server para posteriormente crear un reporte con el objetivo de realizar corroboraciones futuras.

#### Consultas para cada KPI:

a) Total revenue

SELECT SUM(total_price) AS Total_revenue
FROM pizza_sales
Output:
 
![Total revenue](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/1fb9b829-da08-4293-95cc-486d2713a554)

b) Average Order Value

SELECT SUM(total_price)/COUNT(DISTINCT order_id) AS Average_order_value
FROM pizza_sales
Output:

![SQL Avg Order Value](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/5aec33ca-b688-42dc-bccd-ab3a3eb2de26)

c) Total Pizzas Sold
	
SELECT SUM(quantity) AS Total_Pizzas_Sold
FROM pizza_sales
Output:
 
![Total Pizzas Sold](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/de1c421c-046b-4b40-869b-59e3753f9dc6)


d) Total Orders

SELECT COUNT(DISTINCT order_id) AS Total_orders
FROM pizza_sales

Output:

![Total Orders](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/fdf01cee-aef3-4c93-bc70-bb12d133e9c9)


e) Average Pizzas per Order

SELECT SUM(quantity)/COUNT(DISTINCT order_id) AS Average_Pizzas_per_Order
FROM pizza_sales

Output:

![Avg Pizzas per Order](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/bf4d7275-92f3-419c-8aa6-972ceea02494)


f) Average Pizzas per Order 2 DECIMALS
	
SELECT CAST(CAST(SUM(quantity) AS DECIMAL (10,2)) / 
CAST(COUNT(DISTINCT order_id) AS DECIMAL (10,2)) AS DECIMAL (10,2)) AS Average_Pizzas_per_Order
FROM pizza_sales
Output:

![Avg pizzas per order 2 decimals](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/039ed1ba-1281-4c66-95bf-6e726acf2017)


#### Consultas en SQL para Gráficos:

a)	Hourly Trend for Total Pizzas Sold:

SELECT DATEPART(HOUR, order_time) AS order_hour,
      SUM(quantity) AS Total_pizzas_Sold
FROM pizza_sales
GROUP BY DATEPART(HOUR, order_time)
ORDER BY DATEPART(HOUR, order_time)

Output:
 
![Hourly Trend for Total Pizzas Sold](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/18d58c64-95f7-441c-8fdf-dad9f19d3a59)


b)	Weekly Trend for Total Orders:


SELECT  DATEPART(ISO_WEEK, order_date) AS Week_number,
		YEAR(order_date) AS Order_year,
        COUNT(DISTINCT order_id) AS Total_orders
FROM pizza_sales
GROUP BY DATEPART(ISO_WEEK, order_date),
		YEAR(order_date)  
ORDER BY DATEPART(ISO_WEEK, order_date), 
		YEAR(order_date)  

Output:

![ISO Weekly Trend for Total Orders](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/3057cfb5-4f66-4651-8306-978bd2ecdab8)
![ISO Weekly Trend for Total Orders 2](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/74f26ead-82fc-43bf-8790-28ecc77b9695)



c)	Percentage of Sales by Pizza Category:


SELECT pizza_category,
		SUM(total_price) AS Total_sales,
		SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales) AS Percentage_of_sales
FROM pizza_sales
--WHERE MONTH(order_date) = 1 --January / APLICABLE A TODOS LOS QUERIES PARA FILTRAR POR MES/FECHA *TAMBIEN DEBE IR EN SUBQUERY*
GROUP BY pizza_category


Output:
 
![Percentage of Sales by Pizza Category](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/d8dcf443-16a1-45c8-a889-8f2f6fe26c50)

d)	Percentage of Sales by Pizza Size:


SELECT pizza_size,
		CAST(SUM(total_price) AS DECIMAL (10,2)) as Total_sales,
		CAST(SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales) AS DECIMAL (10,2)) AS Percentage_of_sales 
FROM pizza_sales
--WHERE pizza_size = 'M' --January / APLICABLE A TODOS LOS QUERIES PARA FILTRAR POR MES/FECHA *TAMBIEN DEBE IR EN SUBQUERY*
GROUP BY pizza_size
ORDER BY pizza_size

Output:

 ![Percentage of Sales by Pizza Size](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/0b5474c1-a4f0-4919-b96d-a932fedac617)


e)	Total Pizzas Sold by Pizza Category:


SELECT pizza_category, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_category
ORDER BY pizza_category ASC

Output:

 ![Total Pizzas Sold by Pizza Category](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/c5b473a0-bc5f-4bcf-b463-d1ebff98b09b)


f)	Top 5 Best Sellers by Revenue, Total Quantity and Total Orders

By Revenue: 

SELECT TOP 5 pizza_name, SUM(total_price) AS Total_revenue
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_revenue DESC

Output:

![Top 5 Best Sellers by Revenue](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/8397ea2c-75d3-4c71-983e-9d1dacc439b9)


By Quantity: 

SELECT TOP 5 pizza_name, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_quantity DESC

Output:
 
![Top 5 Best Sellers by Total Quantity](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/51f3fd7b-8e0d-4582-be5a-df655ccd38ad)

By Orders: 

SELECT TOP 5 pizza_name, COUNT(distinct order_id) AS Total_orders
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_orders DESC

Output:
 
![Top 5 Best Sellers by Total Orders](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/435dac65-3010-46de-82f4-bb196da5f0ef)



g)	Bottom 5 Best Sellers by Revenue, Total Quantity and Total Orders


By Revenue: 

SELECT TOP 5 pizza_name, CAST(SUM(total_price) AS DECIMAL (10,2)) AS Total_revenue
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_revenue ASC
	
Output:

 ![Bottom 5 Best Sellers by Revenue](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/feb4a3e9-f291-4db2-8d15-902f453bc200)


By Quantity:
SELECT TOP 5 pizza_name, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_quantity ASC

Output:
 
![Bottom 5 Best Sellers by Total Quantity](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/d612b483-5e02-467d-9e73-b4e265a039c2)


By Orders:


SELECT TOP 5 pizza_name, COUNT(distinct order_id) AS Total_orders
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_orders ASC

Output:

![Bottom 5 Best Sellers by Total Orders](https://github.com/RafaellaGuti/Pizza-Sales-Analysis/assets/138822208/9e0ccb67-7037-4a21-b375-8ee61cc02227)

5. Importar datos a Tableau Public.
6. Procesamos los datos en Tableau Public 
7. Creamos Reporte/Tablero 1 “Home”
8. Creamos Reporte/Tablero 2 “Best and Worst Sellers”


### Fuente de Datos
Source: [https://www.kaggle.com/datasets/carrie1/ecommerce-data?resource=download](https://www.kaggle.com/datasets/nextmillionaire/pizza-sales-dataset)
The dataset was downloaded to the local machine and subsequently uploaded to Google Drive under the name "data".
   
### Herramientas, Softwares y Plataformas Utilizadas
- SQL Server
- Tableau
- Microsoft Word
- www.Flaticon.com
- www.Canva.com

### Descubrimientos

### Conclusiones, Limitationes y Recommendationes
