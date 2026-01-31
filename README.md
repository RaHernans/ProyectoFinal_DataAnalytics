## 1. PROYECTO FINAL DATA ANALYTICS: 
Análisis de Ventas Retail.

## 2. DESCRIPCIÓN DEL PROYECTO.
Este proyecto consiste en un análisis de ventas de una empresa retail a partir de datos históricos. 
El objetivo es comprender el comportamiento de las ventas, clientes y rentabilidad mediante un análisis exploratorio de datos (EDA) y la construcción de un dashboard interactivo en Power BI.
El trabajo incluye la carga, limpieza y transformación de los datos con Python, así como la definición de KPIs clave y visualizaciones que permiten analizar la evolución temporal, la segmentación por categorías, mercados y clientes, y la rentabilidad del negocio. 

## 3. ESTRUCTURA DEL PROYECTO.
├── data/
│ ├── raw_data/ # Datos originales sin transformar
│ └── processed_data/ # Dataset final tras limpieza y transformación
│
├── notebooks/
│ ├── 01_load_and_check_data.ipynb
│ ├── 02_data_cleaning_transformation.ipynb
│ └── 03_analysis_and_insights.ipynb
│
├── dashboard/
│ └── ProyectoFinal_dashboard.pbix

│
├── reports/
│ └── (opcional para informes o documentación adicional que puedan surgir)
│
└── README.md # Descripción general del proyecto

## 4. Intalación y requisitos. 
Para la realización de este proyecto se han utilizado las siguientes herramientas y tecnologías:

- Python
- Pandas
- Jupyter Notebook
- Visual Studio Code
- Power BI Desktop
- GitHub

Para ejecutar los notebooks es necesario disponer de un entorno Python con las librerías
básicas de análisis de datos.
El dashboard puede abrirse directamente con Power BI Desktop.

## 5. Análisis y resultados.

Durante el desarrollo del proyecto se llevaron a cabo distintas tareas de limpieza,
transformación y análisis con el objetivo de garantizar la coherencia de los resultados y
una correcta interpretación de los datos.

# Limpieza y tratamiento de los datos
- Durante la fase de preparación de los datos se corrigió la interpretación de columnas
numéricas mediante el uso de la configuración regional, con el fin de evitar errores
derivados del separador decimal y asegurar la correcta lectura de los valores numéricos.

- El conjunto de datos no especifica la moneda asociada a los importes de venta. Por este
motivo, los análisis económicos se han realizado utilizando la unidad monetaria
original del dataset, sin aplicar conversiones externas, con el objetivo de mantener la
coherencia de los resultados y evitar suposiciones no documentadas.

- El campo Sales se encontraba expresado como valor entero. Para facilitar la
interpretación de los resultados y mantener magnitudes coherentes, se realizó una
normalización de la escala de importes, dividiendo los valores por un factor
constante. El mismo criterio se aplicó posteriormente al campo Profit, garantizando la
consistencia entre ventas y beneficio.

# Análisis general de ventas
Las ventas muestran una evolución estable a lo largo del tiempo. No
obstante, este comportamiento global tiende a ocultar patrones relevantes. Por ello, se
profundiza en el análisis por categoría, segmento de cliente y mercado, donde sí se
observan diferencias significativas tanto en el comportamiento de compra como en la
rentabilidad.
El análisis temporal por categoría muestra un crecimiento sostenido de Technology,
frente a un crecimiento más moderado de Furniture y Office Supplies, lo que indica
dinámicas diferenciadas entre líneas de producto.

# Segmentación de clientes
El segmento Consumer concentra el mayor volumen de ventas. El ticket medio es
ligeramente superior en este segmento, aunque las diferencias entre tipos de cliente no
son muy acusadas, lo que sugiere un comportamiento de compra relativamente
homogéneo entre segmentos.
El ticket medio presenta valores elevados, lo cual se explica por la naturaleza del
conjunto de datos, que incluye pedidos corporativos de mobiliario y equipamiento tecnológico, 
además de productos de oficina. En este contexto, un único pedido puede
concentrar un elevado número de unidades y un alto valor económico.

# Análisis geográfico
El análisis geográfico se realiza a nivel de Market (Mercado), que agrupa grandes
áreas geográficas como Europa, América, Asia-Pacífico, entre otras. Este nivel de
agregación permite una comparación clara entre grandes mercados globales,
evitando la confusión derivada de subregiones internas con denominaciones poco
representativas a nivel internacional.
En este sentido, mercados como África y EMEA, presentan crecimiento en ventas a lo largo del tiempo, pero con beneficios y márgenes negativos. Este comportamiento indica un crecimiento no rentable, quizá por posibles problemas de costes, descuentos excesivos o ineficiencias operativas en estos mercados sobre los que habría que trabajar.

# Análisis de rentabilidad
Tras la normalización de las variables económicas, el negocio presenta un margen
global del 14,32 %, lo que indica una rentabilidad moderada y coherente con un
modelo de distribución retail. El beneficio total asciende aproximadamente a 46
millones en la unidad monetaria del dataset.
El análisis del margen por categoría muestra diferencias significativas:
    - Technology presenta una alta rentabilidad.
    - Office Supplies muestra un margen correcto y estable.
    - Furniture registra un margen reducido, lo que indica que, aunque vende
    volumen, apenas genera beneficio.
En cuanto al margen por mercado, se observan comportamientos diferenciados:
    - US / Canada presentan márgenes elevados.
    - EMEA / Europa muestran márgenes más bajos.
    - LATAM y Africa presentan márgenes muy ajustados, lo que sugiere que el
    crecimiento en ciertos mercados no siempre es rentable.

Durante el análisis de rentabilidad se detectaron valores de margen superiores al 100 % 
en determinados mercados, como US. Este comportamiento se explica por un volumen de ventas
relativamente bajo combinado con beneficios positivos, lo que provoca que el margen 
(calculado como Beneficio / Ventas) se vea distorsionado. Por este motivo, el margen debe 
interpretarse junto con el volumen de ventas y no como un indicador aislado.

Se incluye una página específica en el dashboard para contextualizar este KPI y evitar
conclusiones erróneas sobre la rentabilidad por mercado.

Interactividad del dashboard

El dashboard incorpora segmentadores por año, con opción de selección múltiple y
“seleccionar todo”, lo que permite alternar entre un análisis global y un análisis
temporal específico de forma dinámica y flexible.

## 6. Próximos pasos.

- Profundizar en el análisis de rentabilidad a nivel de subcategoría.
- Incorporar modelos predictivos para estimar ventas futuras.
- Mejorar el diseño visual del dashboard con una identidad gráfica más definida. 

## 7. Contribuciones.

Si deseas mejorar este proyecto, puedes abrir un pull request en el repositorio.Toda propuesta se agradece.

## 8. Autor. 

Raquel Hernández Santos
Github: https://github.com/RaHernans/ProyectoFinal_DataAnalytics.git