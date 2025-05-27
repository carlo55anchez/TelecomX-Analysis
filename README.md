# TelecomX-Analysis: Análisis de Evasión de Clientes

## Propósito del análisis
Este proyecto tiene como objetivo analizar los datos de clientes de Telecom X para identificar los factores que contribuyen a la alta tasa de evasión (churn). A través de un Análisis Exploratorio de Datos (EDA), se busca extraer patrones y tendencias que permitan al equipo de Data Science desarrollar modelos predictivos y estrategias para reducir la pérdida de clientes.

## Estructura del proyecto
- **data/**: Contiene los datos en formato JSON (`TelecomX_Data.json`) obtenidos desde la API.
- **notebooks/**: 
  - `01_carga_datos.ipynb`: Carga inicial de datos desde la API y conversión a DataFrame.
  - `02_exploracion_datos.ipynb`: Exploración inicial de columnas, tipos de datos y estadísticas descriptivas.
- **img/**: Imágenes generadas a partir de las visualizaciones (pendiente).
- **scripts/**: Scripts reutilizables en Python para tareas específicas (pendiente).
- **visualizations/**: Visualizaciones exportadas (pendiente).
- **README.md**: Descripción del proyecto y guías de ejecución.
- **requirements.txt**: Dependencias necesarias para ejecutar el proyecto.

## Instrucciones para ejecutar el notebook
1. Clona el repositorio: `git clone https://github.com/<tu-usuario>/TelecomX-Analysis.git`
2. Instala las dependencias: `pip install -r requirements.txt`
3. Abre Google Colab y carga los notebooks desde la carpeta `notebooks/`.
4. Asegúrate de tener acceso al archivo `TelecomX_Data.json` en la carpeta `data/` o usa la URL directa.
5. Ejecuta las celdas del notebook en orden.

## Gráficos e insights
- **Exploración inicial**: Se inspeccionaron las columnas del dataset, sus tipos de datos y estadísticas descriptivas. Se identificaron variables potencialmente relevantes para el análisis de churn, como demográficas (edad, género), de servicio (tipo de servicio, costo mensual) y la variable objetivo (churn). (Pendiente: agregar gráficos tras el EDA completo.)

## Dependencias
- Python 3.8+
- pandas
- numpy
- requests
- seaborn
- matplotlib
- plotly
