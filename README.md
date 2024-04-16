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
This analysis is a Data Analysis Project involving transaction data occurring between 01/1/2010 and 12/12/2015 for a physical `Pizza store registered in the United States. The company mainly sells different flavors of Pizza, opening in a range of 11 hours a day, everyday.

### Objectives
This analysis will determine the overall performance of sales of the products, grouped by category, number of orders, revenue, quantity, size, week, and hour of the day in order to identify patterns and insights that allow the analyst to pinpoint areas for improvement for later use by the company's management.

### Scope
This project aims to provide an effective report and ETL process that builds tables related to the sales movements of the Pizza Store over the course of a year for subsequent utilization and analysis. report and table will allow the company to investigate and find relationships between sales volume, categories, quantity per order, and more. The goal is to identify patterns, obtain clear, up-to-date, and accessible information for subsequent decision-making.

### Project Steps

1. Obtain Data Set Online and download it to local machine.
2. Set goals to detect KPIs and plan charts that meet the needs:

KPIs:

- Total Revenue: The sum of the total price of all pizza orders.
- Average Order Value: The average amount spent per order, calculated by dividing the total revenue by the total number of orders.
- Total Pizzas Sold: The sum of the quantities of all pizzas sold.
- Total Orders: The total number of orders placed.
- Average Pizzas Per Order: The average number of pizzas sold per order, calculated by dividing the total number of pizzas sold by the total number of orders.

Visualization Charts:

- Hourly Trend for Total Pizzas Sold: Create a stacked bar chart that displays the hourly trend of total orders over a specific time period. This chart will help us identify any patterns or fluctuations in order volumes on an hourly basis.
- Weekly Trend for Total Orders: Create a line chart that illustrates the weekly trend of total orders throughout the year. This chart will allow us to identify peak weeks or periods of high order activity.
- Percentage of Sales by Pizza Category: Create a pie chart that shows the distribution of sales across different pizza categories. This chart will provide insights into the popularity of various pizza categories and their contribution to overall sales.
- Percentage of Sales by Pizza Size: Generate a pie chart that represents the percentage of sales attributed to different pizza sizes. This chart will help us understand customer preferences for pizza sizes and their impact on sales.
- Total Pizzas Sold by Pizza Category: Create a funnel chart that presents the total number of pizzas sold for each pizza category. This chart will allow us to compare the sales performance of different pizza categories.
- Top 5 Best Sellers by Revenue, Total Quantity, and Total Orders: Create a bar chart highlighting the top 5 best-selling pizzas based on Revenue, Total Quantity, Total Orders. This chart will help us identify the most popular pizza options.
- Bottom 5 Best Sellers by Revenue, Total Quantity, and Total Orders: Create a bar chart showcasing the bottom 5 worst-selling pizzas based on Revenue, Total Quantity, Total Orders. This chart will enable us to identify underperforming or less popular pizza options.

3. Create Database in SQL Server and import file.
4. Create queries for each KPI and visualization chart in SQL Server to subsequently create a report with the aim of conducting future checks.
5. Import data into Tableau Public.
6. Process the data in Tableau Public.
7. Create Report/Dashboard 1 "Home".
8. Create Report/Dashboard 2 "Best and Worst Sellers".
   



### Source of Data
Source: https://www.kaggle.com/datasets/carrie1/ecommerce-data?resource=download
The dataset was downloaded to the local machine and subsequently uploaded to Google Drive under the name "data".

### Used tools, softwares and platforms
- SQL Server
- Tableau
- www.Canva.com
- www.Flaticon.com

### Findings


### Conclusions, Limitations and Recommendations

The data analysis project provides valuable insights into sales performance across different product categories.
The interactive dashboard offers a user-friendly interface for exploring and interpreting data, facilitating informed decision-making.
Recommendations for future improvements may include incorporating predictive analytics models to forecast sales trends and integrating additional data sources for comprehensive and deeper analysis regarding factors affecting the sales performance of each product in each category.

## ES - Analisis de Ventas de Ecommerce
  
### Sobre el proyecto


### Objetivos


### Alcance

### Pasos del Proyecto
1. Obtener Data Set Online y descargarlo en maquina local.
2. Establecer objetivos para detectar KPI’s y planificar gráficos que cumplan con las necesidades:

KPI’s:

- Ingresos Totales: La suma del precio total de todos los pedidos de pizza.
- Valor Promedio del Pedido: El monto promedio gastado por pedido, calculado dividiendo los ingresos totales por el número total de pedidos.
- Total de Pizzas Vendidas: La suma de las cantidades de todas las pizzas vendidas.
- Total de Pedidos: El número total de pedidos realizados.
- Promedio de Pizzas por Pedido: El número promedio de pizzas vendidas por pedido, calculado dividiendo el total de pizzas vendidas por el número total de pedidos.

Gráficos de Visualización:

- Tendencia Horaria para Total de Pizzas Vendidas: Crear un gráfico de barras apiladas que muestre la tendencia horaria de los pedidos totales durante un período de tiempo específico. Este gráfico nos ayudará a identificar cualquier patrón o fluctuación en los volúmenes de pedidos por hora.
- Tendencia Semanal para Total de Pedidos: Crear un gráfico de líneas que ilustre la tendencia semanal de los pedidos totales a lo largo del año. Este gráfico nos permitirá identificar las semanas pico o los períodos de alta actividad de pedidos.
- Porcentaje de Ventas por Categoría de Pizza: Crear un gráfico circular que muestre la distribución de ventas entre diferentes categorías de pizza. Este gráfico proporcionará información sobre la popularidad de las diversas categorías de pizza y su contribución a las ventas totales.
- Porcentaje de Ventas por Tamaño de Pizza: Generar un gráfico circular que represente el porcentaje de ventas atribuidas a diferentes tamaños de pizza. Este gráfico nos ayudará a comprender las preferencias de los clientes por los tamaños de pizza y su impacto en las ventas.
- Total de Pizzas Vendidas por Categoría de Pizza: Crear un gráfico de embudo que presente el número total de pizzas vendidas para cada categoría de pizza. Este gráfico nos permitirá comparar el rendimiento de ventas de diferentes categorías de pizza.
- Top 5 Mejores Ventas por Ingresos, Cantidad Total y Total de Pedidos: Crear un gráfico de barras que destaque las 5 mejores pizzas más vendidas basadas en los ingresos, la cantidad total y los pedidos totales. Este gráfico nos ayudará a identificar las opciones de pizza más populares.
- Top 5 Peores Ventas por Ingresos, Cantidad Total y Total de Pedidos: Crear un gráfico de barras que muestre las 5 pizzas menos vendidas basadas en los ingresos, la cantidad total y los pedidos totales. Este gráfico nos permitirá identificar las opciones de pizza menos populares o con bajo rendimiento.

3. Crear Database en SQL Server e importar file
4. Crear consultas para cada KPI y gráfico de visualización en SQL Server para posteriormente crear un reporte con el objetivo de realizar corroboraciones futuras.
   Consultas para cada KPI:

a) Total revenue

SELECT SUM(total_price) AS Total_revenue
FROM pizza_sales
Output:
 

b) Average Order Value

SELECT SUM(total_price)/COUNT(DISTINCT order_id) AS Average_order_value
FROM pizza_sales
Output:
 

c) Total Pizzas Sold
	
SELECT SUM(quantity) AS Total_Pizzas_Sold
FROM pizza_sales
Output:
 


d) Total Orders

SELECT COUNT(DISTINCT order_id) AS Total_orders
FROM pizza_sales

Output:
 

e) Average Pizzas per Order

SELECT SUM(quantity)/COUNT(DISTINCT order_id) AS Average_Pizzas_per_Order
FROM pizza_sales

Output:
 

f) Average Pizzas per Order 2 DECIMALS
	
SELECT CAST(CAST(SUM(quantity) AS DECIMAL (10,2)) / 
CAST(COUNT(DISTINCT order_id) AS DECIMAL (10,2)) AS DECIMAL (10,2)) AS Average_Pizzas_per_Order
FROM pizza_sales
Output:
 

Consultas en SQL para Gráficos:

a)	Hourly Trend for Total Pizzas Sold:

SELECT DATEPART(HOUR, order_time) AS order_hour,
      SUM(quantity) AS Total_pizzas_Sold
FROM pizza_sales
GROUP BY DATEPART(HOUR, order_time)
ORDER BY DATEPART(HOUR, order_time)

Output:
 









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
  



c)	Percentage of Sales by Pizza Category:


SELECT pizza_category,
		SUM(total_price) AS Total_sales,
		SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales) AS Percentage_of_sales
FROM pizza_sales
--WHERE MONTH(order_date) = 1 --January / APLICABLE A TODOS LOS QUERIES PARA FILTRAR POR MES/FECHA *TAMBIEN DEBE IR EN SUBQUERY*
GROUP BY pizza_category


Output:

 

d)	Percentage of Sales by Pizza Size:


SELECT pizza_size,
		CAST(SUM(total_price) AS DECIMAL (10,2)) as Total_sales,
		CAST(SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales) AS DECIMAL (10,2)) AS Percentage_of_sales 
FROM pizza_sales
--WHERE pizza_size = 'M' --January / APLICABLE A TODOS LOS QUERIES PARA FILTRAR POR MES/FECHA *TAMBIEN DEBE IR EN SUBQUERY*
GROUP BY pizza_size
ORDER BY pizza_size

Output:
 

e)	Total Pizzas Sold by Pizza Category:


SELECT pizza_category, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_category
ORDER BY pizza_category ASC

Output:
 

f)	Top 5 Best Sellers by Revenue, Total Quantity and Total Orders

By Revenue: 

SELECT TOP 5 pizza_name, SUM(total_price) AS Total_revenue
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_revenue DESC

Output:
 







By Quantity: 

SELECT TOP 5 pizza_name, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_quantity DESC

Output:
 

By Orders: 

SELECT TOP 5 pizza_name, COUNT(distinct order_id) AS Total_orders
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_orders DESC

Output:
 




g)	Bottom 5 Best Sellers by Revenue, Total Quantity and Total Orders


By Revenue: 

SELECT TOP 5 pizza_name, CAST(SUM(total_price) AS DECIMAL (10,2)) AS Total_revenue
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_revenue ASC
	
Output:
 

By Quantity:
SELECT TOP 5 pizza_name, SUM(quantity) AS Total_quantity
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_quantity ASC

Output:
 









By Orders:


SELECT TOP 5 pizza_name, COUNT(distinct order_id) AS Total_orders
FROM pizza_sales
GROUP BY pizza_name 
ORDER BY Total_orders ASC

Output:
 

6. Importar datos a Tableau Public.
7. Procesamos los datos en Tableau Public 
8. Creamos Reporte/Tablero 1 “Home”
9. Creamos Reporte/Tablero 2 “Best and Worst Sellers”


### Fuente de Datos

   
### Herramientas, Softwares y Plataformas Utilizadas

### Descubrimientos

### Conclusiones, Limitationes y Recommendationes
