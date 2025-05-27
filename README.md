# TelecomX-Analysis: Análisis de Evasión de Clientes

## Propósito del análisis
Este proyecto tiene como objetivo analizar los datos de clientes de Telecom X para identificar los factores que contribuyen a la alta tasa de evasión (churn). A través de un Análisis Exploratorio de Datos (EDA), se busca extraer patrones y tendencias que permitan al equipo de Data Science desarrollar modelos predictivos y estrategias para reducir la pérdida de clientes.

## Estructura del proyecto
- **data/**: 
  - `TelecomX_Data.json`: Datos originales en formato JSON.
  - `TelecomX_Data_clean.csv`: Dataset limpio tras desanidar columnas JSON.
  - `TelecomX_Data_corrected.csv`: Dataset corregido tras solucionar inconsistencias.
  - `TelecomX_Data_final.csv`: Dataset final tras imputar valores nulos.
  - `TelecomX_Data_with_daily.csv`: Dataset con la columna `Cargos_Diarios`.
  - `TelecomX_Data_standardized.csv`: Dataset estandarizado con variables binarias y nombres en español.
- **notebooks/**: 
  - `01_carga_datos.ipynb`: Carga inicial de datos desde la API.
  - `02_exploracion_datos.ipynb`: Exploración inicial de columnas y estadísticas.
  - `03_limpieza_datos.ipynb`: Limpieza y desanidado de columnas JSON.
  - `04_correccion_datos.ipynb`: Corrección de `Churn` y tipos de datos.
  - `05_manejo_nulos.ipynb`: Imputación de nulos en `Cargos_Totales`.
  - `06_creacion_cuentas_diarias.ipynb`: Creación de `Cargos_Diarios`.
  - `07_estandarizacion_datos.ipynb`: Estandarización de variables binarias y renombramiento.
  - `08_analisis_evasion.ipynb`: Análisis de la distribución de `Evasión` con gráficos.
- **img/**:
  - `churn_count.png`: Gráfico de conteo de `Evasión`.
  - `churn_pie.png`: Gráfico de pastel de `Evasión`.
- **scripts/**: Scripts reutilizables en Python (pendiente).
- **visualizations/**: Visualizaciones interactivas (pendiente).
- **README.md**: Descripción del proyecto y guías de ejecución.
- **requirements.txt**: Dependencias necesarias.

## Instrucciones para ejecutar el notebook
1. Clona el repositorio: `git clone https://github.com/<tu-usuario>/TelecomX-Analysis.git`
2. Instala las dependencias: `pip install -r requirements.txt`
3. Abre Google Colab y carga los notebooks desde la carpeta `notebooks/`.
4. Asegúrate de tener acceso al archivo `TelecomX_Data.json` o `TelecomX_Data_standardized.csv` en la carpeta `data/` o usa la URL directa.
5. Ejecuta las celdas del notebook en orden.

## Gráficos e insights
- **Exploración inicial**: Se identificaron 6 columnas, incluyendo `Churn` (variable objetivo) y columnas anidadas. La columna `Churn` tenía valores vacíos.
- **Limpieza de datos**: Se desanidaron columnas JSON, obteniendo 21 variables. No se encontraron duplicados.
- **Corrección de datos**: Se corrigieron 224 valores vacíos en `Churn` y un problema de tipo en `Cargos_Totales`.
- **Manejo de nulos**: Se imputaron 11 nulos en `Cargos_Totales`.
- **Creación de variables**: Se añadió `Cargos_Diarios` (`Cargos_Mensuales` / 30).
- **Estandarización**: Variables binarias convertidas a 1/0 y columnas renombradas a español.
- **Análisis de Evasión**:
  - La distribución de `Evasión` se visualizó con un gráfico de conteo y un gráfico de pastel.
  - **Gráfico de conteo**:
    ![Distribución de Evasión](img/churn_count.png)
  - **Gráfico de pastel**:
    ![Proporción de Evasión](img/churn_pie.png)

## Dependencias
- Python 3.8+
- pandas
- numpy
- requests
- seaborn
- matplotlib
- plotly
