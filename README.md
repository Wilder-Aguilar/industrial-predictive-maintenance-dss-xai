# Sistema de Mantenimiento Predictivo con DSS y AI Explicable

📌 **Descripción General**

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

El proyecto se ha desarrollado utilizando un stack tecnológico moderno, integrando herramientas de computación en la nube, lenguajes de programación estadística y plataformas de inteligencia de negocios:

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![XGBoost](https://img.shields.io/badge/XGBoost-black?style=for-the-badge&logo=xgboost&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

* **Lenguaje de Programación:** **Python (v3.10+)** utilizado para el procesamiento de datos y modelado.
* **Ciencia de Datos y ML:**
    * **XGBoost:** Algoritmo principal seleccionado por su elevado rendimiento predictivo y robustez en la clasificación de fallos.
    * **Scikit-Learn:** Empleado para la construcción de pipelines, preprocesamiento y evaluación de métricas.
    * **Imbalanced-learn (SMOTE):** Técnica utilizada para corregir el desbalance de clases en el conjunto de entrenamiento.
* **IA Explicable (XAI):**
    * **SHAP (SHapley Additive exPlanations):** Implementado para cuantificar la contribución de cada variable y eliminar el efecto "caja negra" del modelo.
* **Visualización y DSS:**
    * **Power BI:** Plataforma donde se aloja el Sistema de Soporte a la Decisión (DSS) interactivo.
    * **DAX (Data Analysis Expressions):** Utilizado para operativizar el sistema de recomendación dentro del dashboard.

---

⚙️ **Metodología**

El proceso metodológico se estructura en tres bloques interrelacionados que conforman el *pipeline* del sistema:

## 1. Bloque de Datos

* **Análisis Exploratorio:** Identificación de patrones y estados iniciales del dataset AI4I 2020.
* **Preprocesamiento:** Limpieza de datos y balanceo de clases mediante la técnica **SMOTE**.
* **Ingeniería de Características:** Generación de variables derivadas críticas (*Power*, *Temperature_difference* y *Mechanical_stress*).

## 2. Bloque de Modelado

* **Modelado ML:** Implementación y entrenamiento de algoritmos (*Random Forest*, *Gradient Boosting*, *SVM* y *XGBoost*).
* **Evaluación de Modelos:** Análisis de rendimiento basado en *Accuracy*, *Recall* y *F1-score*.
* **Predicción de Fallos:** Selección del modelo óptimo para la generación de predicciones.

## 3. Bloque de Toma de Decisiones

* **Sistema de Recomendación (DSS):** Traducción de las predicciones en niveles de riesgo y recomendaciones de mantenimiento preventivo.
* **Dashboard:** Visualización interactiva de resultados y monitoreo de activos para el soporte a la decisión.
* **Interpretabilidad:** Integración de **valores SHAP** para explicar la causa raíz de las alarmas generadas.

---

📊 **Dataset**

El proyecto utiliza el dataset **AI4I 2020 Predictive Maintenance**, que simula condiciones reales de operación industrial. El conjunto de datos final incluye variables operativas, derivadas, salidas del modelo, valores SHAP y variables de decisión.

---

📈 **Resultados**

* **Modelo seleccionado:** XGBoost.
* **Accuracy:** 98.35%.
* **F1-score:** 0.76
* **Variables más influyentes:** *Rotational speed*, *Power*, *Tool wear*.
* **XAI:** Se logró eliminar el efecto "caja negra" mediante valores SHAP, permitiendo al operador entender por qué una máquina tiene riesgo alto.

---

📊 **Dashboard (Power BI)**
Los resultados se visualizan mediante un dashboard estructurado en dos paneles:

* **Panel 1: Monitoreo Global:** Vista general del estado de las máquinas.
<img width="1841" height="1062" alt="plot_7 3_pbip1" src="https://github.com/user-attachments/assets/ca87f029-063c-464a-b92a-035d49eadc9a" />

  
* **Panel 2: Análisis Detallado:** Desglose por activo para identificar causas raíz y recomendaciones.
<img width="1839" height="1048" alt="plot_7 4_pbip2" src="https://github.com/user-attachments/assets/be5fb300-7de3-4f41-aea2-bb91722a8840" />

---

🌱 **Impacto en Sostenibilidad**
Este sistema contribuye directamente a:

* Reducción del desperdicio de componentes mecánicos.
* Optimización de rutas e intervenciones de mantenimiento.
* Alineación con los **ODS 9** (Industria, Innovación e Infraestructura) y **ODS 12** (Producción y Consumo Responsables).

---
🚀 **Instrucciones de Ejecución**
Siga estos pasos para replicar el análisis y ejecutar el Sistema de Soporte a la Decisión (DSS) en su entorno local:

## 1. Requisitos Previos
* Cuenta de Google (para utilizar Google Colab).
* Power BI Desktop instalado (para visualizar el dashboard .pbix).
* El dataset original ai4i2020.csv (incluido en la carpeta /datasets).

## 2. Procesamiento de Datos y Modelado (Python)
* Acceda a la carpeta /notebooks y abra el archivo TFM_Aguilar_Wilder_Mantenimiento.ipynb en Google Colab.
* Cargue el archivo ai4i2020.csv cuando el notebook lo solicite o súbalo directamente a la sesión de Colab.
* Ejecute todas las celdas del cuaderno. Este proceso realizará:
Limpieza e Ingeniería de Características.
Entrenamiento del modelo XGBoost.
Cálculo de valores SHAP para interpretabilidad.
* Al finalizar, el notebook generará un archivo llamado dashboard_mantenimiento.csv. Descargue este archivo.

## 3. Visualización en Power BI (DSS)
* Abra el archivo tfm.pbix ubicado en la carpeta raíz del repositorio mediante Power BI Desktop.
* Si el dashboard no carga los datos automáticamente, diríjase a:
Inicio > Transformar datos > Configuración de origen de datos.
Cambie la ruta del origen para que apunte al archivo dashboard_mantenimiento.csv que descargó en el paso anterior.
Haga clic en Aplicar cambios para actualizar las visualizaciones con los resultados del modelo.

## 4. Exploración del Sistema
* Panel de Monitoreo Global: Evalúe el estado general de los activos industriales.
* Panel de Análisis Detallado: Seleccione una máquina específica para ver sus probabilidades de fallo y las recomendaciones de mantenimiento basadas en la IA explicable.

---

📜 **Licencia**
Este proyecto ha sido desarrollado exclusivamente con fines académicos en el marco de un TFM.

---

👤 **Autor**

**Wilder Aguilar**  
Máster en Big Data y Ciencia de Datos
