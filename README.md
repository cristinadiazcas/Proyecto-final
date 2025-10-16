# Proyecto-final

## 📊 Proyecto Final Data Analytics

### 🗒️ Descripción del proyecto y objetivo

Este trabajo constituye la entrega final del curso de Data Analytics. El proyecto tiene como objetivo demostrar la capacidad de aplicación de los conceptos teóricos aprendidos en los diferentes módulos, como Python, el proceso a seguir para realizar un análisis EDA y la creación de tablas dinámicas y Dashboards en Excel o Google Sheets, entre otros.

El proyecto analiza un dataset combinando dos fuentes de datos diferentes, con el objetivo de analizar el mercado laboral global relacionado con Inteligencia Artificial (IA) y su relación con el nivel de desarrollo de la IA en diferentes países. Las fuentes de datos son las siguientes:

- **AI Global Index Dataset** (fuente: Kaggle): contiene indicadores por país sobre el grado de desarrollo del ecosistema de IA (investigación, desarrollo, talento, infraestructura, estrategia gubernamental, y comercial). → https://www.kaggle.com/datasets/katerynameleshenko/ai-index/data
- **Global AI Job Market & Salary Trends 2025** (fuente: Kaggle): incluye información de salarios, tipo de empleo, nivel de experiencia, ubicación geográfica y tendencias del mercado laboral en IA. → https://www.kaggle.com/datasets/bismasajjad/global-ai-job-market-and-salary-trends-2025?select=ai_job_dataset.csv

### Enfoque y técnicas utilizadas

La **metodología** de cara a realizar el proyecto ha sido la siguiente:

1. **Carga y validación de las rutas aportadas en VSC**, comprobando la correcta lectura de los archivos y sus datos.
2. **Limpieza y depuración de los datos**:
    - Homogeinización de nombres de columnas para evitar errores en la manipulación de los datos. Por ejemplo, para unir ambos datasets utilicé el campo de país: en un dataset la columna se llama “country” y en otro “company_location”, y estandaricé los nombres para que se llamaran de la misma forma (ejemplo: Estados Unidos → “United States of America”, en lugar de “United States”, “U.S.”, “U.S.A”).
    - Combinación de los datasets: elegí combinarlos mediante un inner join, porque hay un dataset que contiene más países que otro, por tanto para este análisis me interesaba únicamente mantener las coincidencias entre los dos datasets.
    - Conversión de tipos de datos (campo “date”, “total_score”, “salario_usd”).
    - Eliminación de valores nulos.
3. **EDA**: el análisis se centró en explorar relaciones clave entre las variables del mercado laboral y las del índice global de IA por región, país y tipo de empleo.
4. **Unión de la versión depurada de los dos datasets** (”bank-additional.csv” y “customer-details.xlsx”)
5. **Cálculo de métricas principales** para las conclusiones del análisis
6. **Creación de tablas dinámicas y dashboard en Excel**

Las **herramientas** principales utilizadas han sido Python, concretamente las librerías de numpy, y pandas, y Excel.

## 🗂️ Estructura del proyecto

Proyecto_final/

— datos_brutos/

    — ai_global_index_db.csv

    — ai_job_dataset.csv

— datos_procesados/

    — ai_global_index_limpio.csv

    — ai_job_dataset_limpio.csv

    — ai_merged_limpio.csv

    — correlaciones_previas.csv

    — paises_sin_coincidencia.csv

— notebook/

    — notebook_proyecto_final.ipynb

— dashboard/

    — excel ai.merged_limpio.xlsx

## 🖥️ Instalación y Requisitos

- **Python** versión 3.10+
- **Plataforma Visual Studio Code** o una similar en la que se pueda instalar Python. **Extensión** VSC de Jupyter Notebook.
- **Paquetes**: pandas, numpy

## 📦 Datos analizados

- Dimensión temporal: el dataset cubre los años 2024-2025.

## 📈 Resultados y Conclusiones

### **Panorama general**

- El desarrollo en IA del país y los salarios de empresas localizadas en estos están relacionados, aunque de forma moderada. Los países con mejores ecosistemas de IA tienden a tener salarios más altos (sobretodo aquellos con mayor puntuación en las áreas de investigación y talento).
- América y Europa dominan tanto en salarios como en madurez del ecosistema de IA, ya que muestran los valores más altos en investigación, infraestructura y desarrollo. No obstante, la región de Asia-Pacífico crece como mercado emergente en IA, ya que a pesar de tener salarios más bajos, tiene un crecimiento en talento técnico.

### **Datos**

1. Salario medio global: 116.800 USD
2. Rango de salarios: entre 40.000 y 400.000 USD
3. Regiones con mayor media salarial: (1) América, (2) Europa, (3) Asia-Pacífico, (4) Oriente Medio
4. Roles más frecuentes: Data Scientist, AI Engineer, ML Specialist.
5. A pesar de que la correlación observada es débil, las métricas del AI Global Index con mayor correlación con el nivel salarial son el talento, seguido de la investigación y la infraestructura.

### Conclusiones

En conclusión, el análisis del mercado laboral en Inteligencia Artificial y del desarrollo de este ecosistema a nivel nacional revela una relación positiva, aunque moderada, entre el nivel de madurez tecnológica de los países y la retribución de los profesionales. 

Las regiones con mayor inversión en investigación, talento e infraestructura (principalmente América y Europa) concentran los salarios más altos y las oportunidades laborales de mayor especialización, mientras que Asia-Pacífico emerge como potencia de crecimiento en desarrollo y talento. La experiencia profesional se confirma como el factor más determinante en el nivel salarial. 

En conjunto, los resultados reflejan un mercado en el que la formación, experiencia y ecosistema de innovación juegan un papel clave en la trayectoria profesional de los trabajadores y la competitividad del mercado laboral en el país.

### 🗂️ Entregables

- Datos brutos, datos depurados y dataset combinado
- Notebook con la limpieza de los dataset y análisis EDA
- README con el resumen del proyecto y las conclusiones principales del análisis

### 🖋️ Autores

Cristina Díaz Castillo
