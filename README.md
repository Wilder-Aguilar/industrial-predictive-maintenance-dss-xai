# Desarrollo de un sistema de recomendación de intervenciones de mantenimiento preventivo para máquinas industriales

## 📌 **Descripción General**

Este repositorio contiene la implementación de un **Sistema de Soporte a la Decisión (DSS)** orientado al mantenimiento predictivo en maquinaria industrial, desarrollado como parte del **Trabajo de Fin de Máster** en la Universidad Internacional de Valencia - VIU.

El sistema integra:

* **Modelos de Machine Learning** para la predicción de fallos.
* **Técnicas de Inteligencia Artificial Explicable (SHAP)** para la transparencia de los modelos.
* **Ingeniería de Características** mediante la generación de variables derivadas.
* **Dataset estructurado** optimizado para la toma de decisiones.
* **Dashboard interactivo** desarrollado en Power BI para visualización de riesgos.

El objetivo principal es anticipar fallos y recomendar intervenciones de mantenimiento, optimizando la operación industrial y reduciendo riesgos operativos.

---

## 🛠️ Tecnologías y Herramientas

<p align="left">
  <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" />
  <img src="https://img.shields.io/badge/XGBoost-black?style=for-the-badge&logo=xgboost&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" />
</p>

* **Core:** Python (Pandas, NumPy) para ETL e Ingeniería de Características.
* **ML:** **XGBoost** (Clasificación), Scikit-Learn (Pipelines) y SMOTE para balanceo.
* **XAI:** **SHAP** para la interpretación de la "caja negra".
* **DSS:** Power BI + **DAX** para el sistema de recomendación interactivo.

---

## ⚙️ **Metodología**

El proceso metodológico se estructura en tres bloques interrelacionados que conforman el *pipeline* del sistema:

### 1. Bloque de Datos

* **Análisis Exploratorio:** Identificación de patrones y estados iniciales del dataset AI4I 2020.
* **Preprocesamiento:** Limpieza de datos y balanceo de clases.
* **Ingeniería de Características:** Generación de variables derivadas críticas (*Power*, *Temperature_difference* y *Mechanical_stress*).

### 2. Bloque de Modelado

* **Modelado ML:** Implementación y entrenamiento de algoritmos (*Random Forest*, *Gradient Boosting*, *SVM* y *XGBoost*).
* **Evaluación de Modelos:** Análisis de rendimiento basado en *Accuracy*, *Recall*, *F1-score*  y *Precision*.
* **Predicción de Fallos:** Selección del modelo óptimo para la generación de predicciones.

### 3. Bloque de Toma de Decisiones

* **Sistema de Recomendación (DSS):** Traducción de las predicciones en niveles de riesgo y recomendaciones de mantenimiento preventivo.
* **Dashboard:** Visualización interactiva de resultados y monitoreo de activos para el soporte a la decisión.
* **Interpretabilidad:** Integración de **valores SHAP** para explicar la causa raíz de las alarmas generadas.

---

## 📊 **Dataset**

El proyecto utiliza el dataset **AI4I 2020 Predictive Maintenance**, que simula condiciones reales de operación industrial. El conjunto de datos final incluye variables operativas, derivadas, salidas del modelo, valores SHAP y variables de decisión.

---

## 📈 Resultados del Modelo

<p align="left">
  <img src="https://img.shields.io/badge/Algorithm-XGBoost-blue?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Model_Accuracy-98.4%25-brightgreen?style=flat-square&logo=target" />
  <img src="https://img.shields.io/badge/Precision-0.76-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/Recall-0.75-yellow?style=flat-square" />
  <img src="https://img.shields.io/badge/F1--Score-0.76-red?style=flat-square" />
</p>

* **Variables clave:** *Rotational speed*, *Power*, *Tool wear*.
* **Interpretación:** Gracias a los **valores SHAP**, el sistema no solo predice el fallo, sino que identifica cuál de estas variables es la responsable, permitiendo un mantenimiento preventivo dirigido.

<img width="1002" height="600" alt="plot_5_7_model_comparison" src="https://github.com/user-attachments/assets/1b06b60d-dad7-4d22-bcea-6a0c3d08d2da" />

---

## 📊 **Dashboard (Power BI)**
Los resultados se visualizan mediante un dashboard estructurado en dos paneles:

* **Panel 1: Monitoreo Global:** Vista general del estado de las máquinas.
<img width="1493" height="838" alt="plot_7_3_pbip1" src="https://github.com/user-attachments/assets/6b7714e9-f182-4bcf-9d1c-85e601053324" />
  
* **Panel 2: Análisis Detallado:** Desglose por activo para identificar causas raíz y recomendaciones.
<img width="1494" height="836" alt="plot_7_4_pbip2" src="https://github.com/user-attachments/assets/4728de0f-1702-4590-9970-a4a149643d85" />

---

## 🌱 **Impacto en Sostenibilidad**

Este sistema contribuye directamente a:

* Reducción del desperdicio de componentes mecánicos.
* Optimización de rutas e intervenciones de mantenimiento.
* Alineación con los **ODS 9** (Industria, Innovación e Infraestructura) y **ODS 12** (Producción y Consumo Responsables).

---

## 🚀 **Instrucciones de Ejecución**

Siga estos pasos para replicar el análisis y ejecutar el Sistema de Soporte a la Decisión (DSS) en su entorno local:

### 1. Requisitos Previos

* Cuenta de Google (para utilizar Google Colab).
* Power BI Desktop instalado (para visualizar el dashboard .pbix).
* El dataset original ai4i2020.csv (incluido en la carpeta /datasets).

### 2. Procesamiento de Datos y Modelado (Python)

* Acceda a la carpeta /notebooks y abra el archivo TFM_AguilarWilder_SistemaRecomendacion.ipynb en Google Colab.
* Cargue el archivo ai4i2020.csv cuando el notebook lo solicite.
* Ejecute todas las celdas del cuaderno. Este proceso realizará:
    * Limpieza e Ingeniería de Características.
    * Entrenamiento del modelo XGBoost.
    * Cálculo de valores SHAP para interpretabilidad.
* Al finalizar, el notebook generará un archivo llamado dashboard_mantenimiento.csv. Descargue este archivo.

### 3. Visualización en Power BI (DSS)

* Abra el archivo TFM_AguilarWilder_SistemaRecomendacion.pbix ubicado en la carpeta raíz del repositorio mediante Power BI Desktop.
* Si el dashboard no carga los datos automáticamente, diríjase a:
    * Inicio > Transformar datos > Configuración de origen de datos.
    * Cambie la ruta del origen para que apunte al archivo dashboard_mantenimiento.csv que descargó en el paso anterior.
    * Haga clic en Aplicar cambios para actualizar las visualizaciones con los resultados del modelo.

### 4. Exploración del Sistema

* Panel de Monitoreo Global: Evalúe el estado general de los activos industriales.
* Panel de Análisis Detallado: Seleccione una máquina específica para ver sus probabilidades de fallo y las recomendaciones de mantenimiento basadas en la IA explicable.

---

## 📜 **Licencia**

Este proyecto ha sido desarrollado exclusivamente con fines académicos en el marco de un TFM.

---

## 👤 **Autor**

**Wilder Aguilar**  
Máster en Big Data y Ciencia de Datos
