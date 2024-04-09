# Pizza Sales Analysis Report/Dasboard



### Table of content
### EN
- [About the project](#About-the-project)
- [Objectives](#Objectives)
- [Scope](#Scope)
- [Project Steps](#Project-Steps)
- [Source of Data](#Source-of-Data)
- [Used tools, softwares and platforms](#Used-tools-softwares-and-platforms)
- [Findings](#Findings)
- [Conclusions, Limitations and Recommendations](#Conclusions-Limitations-and-Recommendations)

### ES
- [Sobre el proyecto](#Sobre-el-proyecto)
- [Objetivos](#Objetivos)
- [Alcance](#Alcance)
- [Pasos del Proyecto](#Pasos-del-Proyecto)
- [Fuente de Datos](#Fuente-de-Datos)
- [Herramientas, Softwares y Plataformas Utilizadas](#Herramientas-Softwares-y-Plataformas-Utilizadas)
- [Descubrimientos](#Descubrimientos)
- [Conclusiones, limitaciones y recomendaciones](#Conclusiones-limitaciones-y-recomendaciones)


### About the project
This analysis is an Exploratory Data Analysis Project involving transaction data occurring between 01/12/2010 and 09/12/2011 for an online non-physical retail store registered in the United Kingdom. The company mainly sells unique gifts for all occasions. Many of the company's customers are wholesalers: B2B clients. With both numerical and characteristic data, the additional records we will add in step 3 of this project will allow us to conduct both qualitative and quantitative analysis, enabling us to express the study's conclusions in a more comprehensive manner.

### Objectives
This analysis will determine the overall performance of products, grouped by categories, in terms of sales volume, order volume, profit margin, and sales peaks, in order to identify patterns and insights that allow the analyst to pinpoint areas for improvement for later use by the company's management.

### Scope
This project aims to provide an effective ETL process that builds tables related to the sales movements of an Ecommerce in the United Kingdom over the course of a year for subsequent visualization and analysis. The tables will allow the analyst to investigate and find relationships between sales volume, categories, quantity per order, and prices. The goal is to identify patterns, obtain clear, up-to-date, and accessible information for subsequent decision-making.

### Project Steps
1. Obtain data source online, download it to local machine, and store it in a Google Drive folder.

2. Connect to Dataset in Google Drive using Google API and select the sheet and records to use.
![2024-04-07](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/3be9fe50-d482-44a1-a6e9-3728e8b695f3)


3. Perform initial general cleaning and prepare data to create the table from which the analysis will start by adding columns derived from other columns' records, adding a 'Category' column based on a selection of keywords obtained from the product description, rounding 'Float' columns to only 2 decimals, and assigning data types such as 'datetime', 'float', and 'str' to corresponding columns:

   Cleaning   
![2024-04-07 (1)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/b7ecd47b-44b8-4b1e-9422-b6dc47bc7a73)

   Defining and assigning categories using keywords
![2024-04-07 (2)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/c8921a59-4a7c-40fe-845f-e33aca94e05f)


5. Descriptively analyze the resulting content to determine relationships, patterns, trends, insights, and relevant information that support informed decision-making aimed at improving Ecommerce performance. In this step, we also define the elements that will be part of the interactive dashboard. For more information on the data cleaning section for the chart elements, refer to the .rar file.

   Element 1: Interactive row of panels indicating: Total Revenue in the last month, Total Profit in the last month, Total Units sold in the last month.
   
![2024-04-07 (4)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/2de2ba5a-d32f-48d7-8905-d4129497e03c)

   Element 2: Interactive bar chart indicating Total Profits in USD made in each month by category.
![2024-04-07 (5)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/a86c3eb7-7549-4d2a-83b3-b6299237838b)

   Element 3: Bar chart indicating the performance of each category in the last year.
![2024-04-07 (6)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/4406f52c-9b56-4a44-be5b-0439f8846738)

   Element 4: Interactive Summary Table indicating the date, product, quantity, units sold, and profits.
![2024-04-07 (7)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/250b43b0-43a8-432c-937f-9a9345e1d63b)

The fifth element is an Interactive Filter Panel called Category located on the right side of the dashboard, this panel was extracted from element 1 and is applicable to 3 of the 4 elements.

5. Create a dashboard to visually report findings in an easily interpretable manner for audiences with both technical and non-technical backgrounds; accessible and supporting the communication of conclusions drawn from the findings.
![2024-04-07 (8)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/3c4f3ff6-4c13-4d13-8f42-4ce99f7d09e3)

### Source of Data
Source: https://www.kaggle.com/datasets/carrie1/ecommerce-data?resource=download
The dataset was downloaded to the local machine and subsequently uploaded to Google Drive under the name "data".

### Used tools, softwares and platforms
- Python
- Jupyter Notebooks
- Google Drive API

### Findings

Firstly, the panel facilitates dynamic filtering by product category, allowing users to focus on specific segments of interest:

- Monthly insights reveal variations in sales performance, with some categories showing significant fluctuations in revenue, profits, and units sold. Total revenue, total profit, and units sold show an increase in the last month, suggesting a positive growth in the business during that period. It would be important to investigate what factors contributed to this increase in sales. They could include successful promotions, new popular products, or an improvement in customer experience.

- The monthly performance analysis highlights trends in category performance over time and can reveal trends of growth or decline in sales. The annual performance analysis provides an overview of which categories are generating the most profits in absolute terms, helping to identify growth opportunities and areas for improvement. The detailed summary table offers detailed insights into individual product performance, aiding in strategic decision-making and inventory management.

It is observed that some categories may be more profitable than others. It would be helpful to investigate which specific products within those categories are contributing the most to profits.

These findings suggest that sales are increasing, both overall and within certain specific categories. It would be beneficial to delve deeper into the data to better understand the reasons behind these trends and make informed strategic decisions accordingly.

Identifying categories showing consistent growth can help the company focus its marketing and product development efforts on areas with high growth potential.

### Conclusions, Limitations and Recommendations

The data analysis project provides valuable insights into sales performance across different product categories.
The interactive dashboard offers a user-friendly interface for exploring and interpreting data, facilitating informed decision-making.
Recommendations for future improvements may include incorporating predictive analytics models to forecast sales trends and integrating additional data sources for comprehensive and deeper analysis regarding factors affecting the sales performance of each product in each category.

## ES - Analisis de Ventas de Ecommerce
  
### Sobre el proyecto
Este análisis es un Proyecto de Análisis de Datos Exploratorio que involucra los datos de las transacciones ocurridas entre el 01/12/2010 y el 09/12/2011 para una tienda minorista en línea no física registrada en el Reino Unido. La empresa principalmente vende regalos únicos para todas las ocasiones. Muchos clientes de la empresa son mayoristas: clientes B2B. Contando con datos tanto numéricos como característicos, los registros complementarios que añadiremos en el paso 3 de este proyecto nos permitirán efectuar un análisis tanto cualitativo como cuantitativo, permitiéndonos expresar las conclusiones del estudio de una manera más completa.

### Objetivos
Este análisis permitirá determinar el desempeño general de los productos, agrupados por categorías, en términos de volumen de ventas, volumen de pedidos, margen de ganancia y picos de ventas, con el fin de identificar patrones e insights que permitan al analista ubicar áreas de mejora para un uso posterior por parte de la gerencia de la empresa.

### Alcance
Este proyecto busca proporcionar un proceso de ETL efectivo que construya tablas referentes a los movimientos de ventas de un Ecommerce en Reino Unido durante el periodo de un año para su posterior visualizacion y analisis. Las tablas permitiran al analista investigar y encontrar relaciones entre el columen de ventas, categorias, cantidad por orden de compra y precios. Con el fin de identificar patrones, obtener informacion clara, actualizada y accesible para la posterior toma de decisiones.

### Pasos del Proyecto
1. Obtener fuente de datos de manera online, descargarla en maquina local y almacenarla en una carpeta de Google Drive
2. Conectar con Dataset en Google Drive utilizando Google API y seleccionar la hoja y registros a utilizar.

   ![2024-04-07](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/3be9fe50-d482-44a1-a6e9-3728e8b695f3)

3. Realizar una primera limpieza general y preparar los datos para crear la tabla de la cual partira el analisis agregando columnas producto de los registros de otras columnas, agregando columna 'Category' a partir de una seleccion de keywords obtenidos de la descripcion del producto, redondeamos columnas 'Float'para obtener solo 2 decimales y asignamos tipo de datos como 'datetime', 'float' y 'str' a columnas correspondientes:

   Limpieza

![2024-04-07 (1)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/b7ecd47b-44b8-4b1e-9422-b6dc47bc7a73)

  Definimos y asignamos categorias utilizando palabras clave
![2024-04-07 (2)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/c8921a59-4a7c-40fe-845f-e33aca94e05f)


4. Analizar de forma descriptiva el contenido resultantes para determinar relaciones, patrones, tendencias, insights e informacion relevante que de pie a la toma de decisiones informadas con direccion a la mejora del desesmpeño del Ecommerce. En este paso tambien definimos los elementos que formaran parte del tablero interactivo. Para mas informacion sobre la seccion de limpieza de datos para los elementos del grafico revisar el archivo .rar.

   Elemento 1: Fila interactiva de paneles que indican: Ingresos Totales en el último mes, Beneficio Total en el último mes, Unidades Totales vendidas en el último mes.
   
![2024-04-07 (4)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/2de2ba5a-d32f-48d7-8905-d4129497e03c)

   Elemento 2: Gráfico de barras interactivo que indica los Beneficios Totales en USD realizados en cada mes por categoría.
![2024-04-07 (5)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/a86c3eb7-7549-4d2a-83b3-b6299237838b)

   Elemento 3: Gráfico de barras que indica el rendimiento de cada categoría en el último año.
![2024-04-07 (6)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/4406f52c-9b56-4a44-be5b-0439f8846738)

   Elemento 4: Tabla Resumen Interactiva que indica la fecha, producto, cantidad, unidades vendidas y beneficios.
![2024-04-07 (7)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/250b43b0-43a8-432c-937f-9a9345e1d63b)

El quinto elemento es Panel de Filtro Interactivo llamado Categoría que se encuentra al costado derecho del tablero, este panel fue extraido del elemento 1 y es aplicable a 3 de los 4 elementos.

5. Creacion de tablero para reportar de forma visual los hallazgos de una manera facil de interpretar para audiencias con experiencia tenica y no tecnica; accesible y que apoye a la comunicacion de conclusiones obtenidas a partir de los hallazgos
![2024-04-07 (8)](https://github.com/RafaellaGuti/Ecommerce-Python-Project/assets/138822208/3c4f3ff6-4c13-4d13-8f42-4ce99f7d09e3)


### Fuente de Datos
Fuente : https://www.kaggle.com/datasets/carrie1/ecommerce-data?resource=download
El dataset fue descargado en maquina local y posteriormente subido a Google Drive con el nombre de "data"
   
### Herramientas, Softwares y Plataformas Utilizadas
- Lenguaje Python
- Jupyter Notebooks
- Google Drive API

### Descubrimientos

Primeramente, el panel facilita el filtrado dinámico por categoría de producto, permitiendo a los usuarios centrarse en segmentos específicos de interés:

- Los insights mensuales revelan variaciones en el rendimiento de las ventas, con algunas categorías mostrando fluctuaciones significativas en ingresos, beneficios y unidades vendidas. Los ingresos totales, el beneficio total y las unidades vendidas muestran un aumento en el último mes, esto sugiere un crecimiento positivo en el negocio durante ese período. Sería importante investigar qué factores contribuyeron a este aumento en las ventas. Podrían incluir promociones exitosas, nuevos productos populares o una mejora en la experiencia del cliente.

- El análisis de rendimiento mensual destaca las tendencias en el rendimiento de la categoría con el tiempo, puede revelar tendencias de crecimiento o declive en las ventas. 
El análisis de rendimiento anuual proporciona una visión de qué categorías están generando más beneficios en términos absolutos, ayudando a identificar oportunidades de crecimiento y áreas de mejora. 
La tabla de resumen detalladas ofrecen insights detallados sobre el rendimiento individual del producto, ayudando en la toma de decisiones estratégicas y la gestión de inventario.

Se observa que algunas categorías pueden ser más rentables que otras. Sería útil investigar qué productos específicos dentro de esas categorías están contribuyendo más a los beneficios.
  
Estos hallazgos sugieren que las ventas están en aumento, tanto en términos generales como dentro de ciertas categorías específicas. Sería beneficioso profundizar en los datos para comprender mejor las razones detrás de estas tendencias y tomar decisiones estratégicas informadas en consecuencia.

Identificar las categorías que muestran un crecimiento constante puede ayudar a la empresa a centrar sus esfuerzos de marketing y desarrollo de productos en áreas que tienen un alto potencial de crecimiento.
