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

* **Core:** Python (Pandas, NumPy) para procesos de ETL e Ingeniería de Características.
* **Modelado ML:** Aunque **XGBoost** fue seleccionado como el modelo óptimo, el estudio incluyó la implementación y evaluación comparativa de **Random Forest**, **Gradient Boosting** y **SVM**.
* **Librerías de Soporte:** Scikit-Learn (Pipelines y métricas) e Imbalanced-learn (SMOTE) para el tratamiento del desbalance de clases.
* **XAI:** **SHAP** (SHapley Additive exPlanations) para garantizar la interpretabilidad y transparencia del modelo.
* **DSS:** Power BI + **DAX** para la arquitectura del sistema de soporte a la decisión interactivo.



## 🛠️ Tecnologías y Herramientas

<p align="left">
  <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" />
  <img src="https://img.shields.io/badge/XGBoost-black?style=for-the-badge&logo=xgboost&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
</p>

> **Modelos evaluados durante la fase de experimentación:**
> ![Random Forest](https://img.shields.io/badge/Random_Forest-00441b?style=flat-square) ![Gradient Boosting](https://img.shields.io/badge/Gradient_Boosting-00441b?style=flat-square) ![SVM](https://img.shields.io/badge/SVM-00441b?style=flat-square)

* **Core:** Python (Pandas, NumPy) para procesos de ETL e Ingeniería de Características [cite: 5feb76d8-65ee-45f4-9bef-8f1835d35244, 256f8897-9e3c-4e85-ae25-c30460df63a5, b7ed26b9-1ce0-48a9-8429-869430e08693, 446c08de-9ddf-40a7-bf93-c29686a5810d, 250cf209-2d4f-4e8d-ad32-c3f42b6133a4, dceb8e5f-77db-48e1-81e9-960d786b8e42, 9d6d7465-1ead-406f-bb3e-560aa3160626, 9ddea030-7483-4cb0-be08-b5a73998d182].
* **Modelado ML:** Aunque **XGBoost** fue seleccionado como el modelo óptimo, el estudio incluyó la evaluación comparativa de **Random Forest**, **Gradient Boosting** y **SVM** [cite: 5feb76d8-65ee-45f4-9bef-8f1835d35244, 256f8897-9e3c-4e85-ae25-c30460df63a5, b7ed26b9-1ce0-48a9-8429-869430e08693, 446c08de-9ddf-40a7-bf93-c29686a5810d, 250cf209-2d4f-4e8d-ad32-c3f42b6133a4, dceb8e5f-77db-48e1-81e9-960d786b8e42, 9d6d7465-1ead-406f-bb3e-560aa3160626, 9ddea030-7483-4cb0-be08-b5a73998d182].
* **XAI:** **SHAP** para garantizar la interpretabilidad y transparencia del modelo [cite: 5feb76d8-65ee-45f4-9bef-8f1835d35244, 256f8897-9e3c-4e85-ae25-c30460df63a5, b7ed26b9-1ce0-48a9-8429-869430e08693, 446c08de-9ddf-40a7-bf93-c29686a5810d, 250cf209-2d4f-4e8d-ad32-c3f42b6133a4, dceb8e5f-77db-48e1-81e9-960d786b8e42, 9d6d7465-1ead-406f-bb3e-560aa3160626, 9ddea030-7483-4cb0-be08-b5a73998d182].

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

<img width="1002" height="500" alt="plot_5_7_model_comparison" src="https://github.com/user-attachments/assets/1b06b60d-dad7-4d22-bcea-6a0c3d08d2da" />

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

## 📂 Estructura del Repositorio

* **`📂 datasets/`**: Contiene el dataset original `ai4i2020.csv` y el archivo de salida `dashboard_mantenimiento.csv`.
* **`📂 notebooks/`**: Incluye `TFM_AguilarWilder_SistemaRecomendacion.ipynb`, el cual está optimizado para su ejecución en **Google Colab**.
* **`📂 dashboard/`**: Contiene el archivo de Power BI `TFM_AguilarWilder_SistemaRecomendacion.pbix`, que aloja el Sistema de Soporte a la Decisión (DSS).
* **`📂 docs/`**: Documentación complementaria, capturas de pantalla del dashboard y diagramas metodológicos.

---

## 🚀 Instrucciones de Ejecución

Siga estos pasos para replicar el análisis y ejecutar el Sistema de Soporte a la Decisión (DSS):

### 1. Requisitos Previos
* Cuenta de Google (para ejecutar el notebook en **Google Colab**).
* Power BI Desktop instalado.
* Dataset `ai4i2020.csv` (disponible en la carpeta `/datasets`).

### 2. Procesamiento de Datos y Modelado
1. Acceda a la carpeta `/notebooks` y abra el archivo `TFM_AguilarWilder_SistemaRecomendacion.ipynb` directamente en **Google Colab**.
2. Cargue el archivo `ai4i2020.csv` cuando el script lo solicite.
3. Ejecute todas las celdas. El proceso generará automáticamente un archivo de salida llamado `dashboard_mantenimiento.csv`. **Descárguelo**.

### 3. Visualización en Power BI
1. Abra el archivo `TFM_AguilarWilder_SistemaRecomendacion.pbix` (ubicado en la carpeta `/dashboard`).
2. Para actualizar los datos con su nueva ejecución:
   * Vaya a **Inicio** > **Transformar datos** > **Configuración de origen de datos**.
   * Cambie la ruta para que apunte al archivo `dashboard_mantenimiento.csv` que descargó de Colab.
   * Haga clic en **Aplicar cambios**.

---

## 📜 **Licencia**

Este proyecto ha sido desarrollado exclusivamente con fines académicos en el marco de un TFM.

---

## 👤 **Autor**

**Wilder Aguilar**  
Máster en Big Data y Ciencia de Datos
