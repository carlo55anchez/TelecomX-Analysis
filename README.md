# TelecomX-Analysis: Análisis de Evasión de Clientes

## Propósito del análisis
Este proyecto tiene como objetivo analizar los datos de clientes de Telecom X para identificar los factores que contribuyen a la alta tasa de evasión (churn). A través de un Análisis Exploratorio de Datos (EDA), se busca extraer patrones y tendencias que permitan al equipo de Data Science desarrollar modelos predictivos y estrategias para reducir la pérdida de clientes.

## Estructura del proyecto
- **data/**: 
  - `TelecomX_Data.json`: Datos originales en formato JSON.
  - `TelecomX_Data_clean.csv`: Dataset limpio tras desanidar columnas JSON.
  - `TelecomX_Data_corrected.csv`: Dataset corregido tras solucionar inconsistencias.
  - `TelecomX_Data_final.csv`: Dataset final tras imputar valores nulos.
  - `TelecomX_Data_with_daily.csv`: Dataset con la columna `Cuentas_Diarias` añadida.
- **notebooks/**: 
  - `01_carga_datos.ipynb`: Carga inicial de datos desde la API y conversión a DataFrame.
  - `02_exploracion_datos.ipynb`: Exploración inicial de columnas, tipos de datos y estadísticas descriptivas.
  - `03_limpieza_datos.ipynb`: Limpieza de datos, incluyendo desanidado de columnas JSON.
  - `04_correccion_datos.ipynb`: Corrección de valores vacíos en `Churn` y problemas de tipo.
  - `05_manejo_nulos.ipynb`: Imputación de 11 valores nulos en `account_Charges.Total`.
  - `06_creacion_cuentas_diarias.ipynb`: Creación de la columna `Cuentas_Diarias` para facturación diaria.
- **img/**: Imágenes generadas a partir de las visualizaciones (pendiente).
- **scripts/**: Scripts reutilizables en Python para tareas específicas (pendiente).
- **visualizations/**: Visualizaciones exportadas (pendiente).
- **README.md**: Descripción del proyecto y guías de ejecución.
- **requirements.txt**: Dependencias necesarias para ejecutar el proyecto.

## Instrucciones para ejecutar el notebook
1. Clona el repositorio: `git clone https://github.com/<tu-usuario>/TelecomX-Analysis.git`
2. Instala las dependencias: `pip install -r requirements.txt`
3. Abre Google Colab y carga los notebooks desde la carpeta `notebooks/`.
4. Asegúrate de tener acceso al archivo `TelecomX_Data.json` o `TelecomX_Data_with_daily.csv` en la carpeta `data/` o usa la URL directa.
5. Ejecuta las celdas del notebook en orden.

## Gráficos e insights
- **Exploración inicial**: Se identificaron 6 columnas, incluyendo `Churn` (variable objetivo) y columnas anidadas (`customer`, `phone`, `internet`, `account`). La columna `Churn` tenía 3 valores únicos, incluyendo un valor vacío.
- **Limpieza de datos**: Se desanidaron las columnas JSON, obteniendo 21 variables. No se encontraron valores nulos ni duplicados.
- **Corrección de datos**: Se corrigieron 224 valores vacíos en `Churn` y un problema de tipo en `account_Charges.Total`.
- **Manejo de nulos**: Se imputaron 11 valores nulos en `account_Charges.Total` usando `account_Charges.Monthly` para clientes con `customer_tenure` ≤ 1.
- **Creación de variables**: Se añadió la columna `Cuentas_Diarias`, calculada como `account_Charges.Monthly` dividido por 30, para analizar la facturación diaria.

## Dependencias
- Python 3.8+
- pandas
- numpy
- requests
- seaborn
- matplotlib
- plotly
