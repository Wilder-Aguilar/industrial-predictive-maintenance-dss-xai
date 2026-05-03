# Sistema de Mantenimiento Predictivo con DSS y AI Explicable

📌 **Descripción General**

Este repositorio contiene la implementación de un **Sistema de Soporte a la Decisión (DSS)** orientado al mantenimiento predictivo en maquinaria industrial, desarrollado como parte de un **Trabajo de Fin de Máster**.

El sistema integra:
* **Modelos de Machine Learning** para la predicción de fallos.
* **Técnicas de Inteligencia Artificial Explicable (SHAP)** para la transparencia de los modelos.
* **Ingeniería de Características** mediante la generación de variables derivadas.
* **Dataset estructurado** optimizado para la toma de decisiones.
* **Dashboard interactivo** desarrollado en Power BI para visualización de riesgos.

El objetivo principal es anticipar fallos y recomendar intervenciones de mantenimiento, optimizando la operación industrial y reduciendo riesgos operativos.

---

⚙️ **Metodología**

El proyecto sigue un flujo estructurado compuesto por las siguientes fases:

1.  **Preprocesamiento de datos**
    * Limpieza y transformación de datos brutos.
    * Balanceo de clases mediante la técnica **SMOTE**.
2.  **Ingeniería de características**
    * Generación de variables derivadas críticas: *Power*, *Temperature_difference* y *Mechanical_stress*.
3.  **Modelado**
    * Algoritmos evaluados: Random Forest, Gradient Boosting y Support Vector Machine (SVM).
    * **Modelo seleccionado:** Gradient Boosting.
4.  **Evaluación de modelos**
    * Métricas clave: Accuracy, Recall (métrica prioritaria para evitar falsos negativos) y F1-score.
5.  **Interpretabilidad**
    * Uso de **valores SHAP** para análisis de importancia global y local (por activo).
6.  **Sistema DSS**
    * Generación automatizada de predicción de fallo, probabilidad, nivel de riesgo y recomendaciones de mantenimiento.

---

📊 **Dataset**

El proyecto utiliza el dataset **AI4I 2020 Predictive Maintenance**, que simula condiciones reales de operación industrial. El conjunto de datos final incluye variables operativas, derivadas, salidas del modelo, valores SHAP y variables de decisión.

---

📁 **Estructura del Repositorio**

```text
├── data/
│   └── dataset_final.csv           # Datos procesados para el modelo
├── notebooks/
│   └── mantenimiento_predictivo.ipynb  # Proceso completo en Google Colab
├── src/                            # Scripts modulares
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── modeling.py
│   ├── shap_analysis.py
│   └── dss_generation.py
├── images/                         # Figuras y diagramas del TFM
├── README.md                       # Documentación principal
└── requirements.txt                # Librerías necesarias

🚀 **Ejecución del Proyecto**

---

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)

Instalar dependencias:
   ```bash
pip install -r requirements.txt

Ejecutar el notebook:
   ```bash
jupyter notebook notebooks/mantenimiento_predictivo.ipynb

---

📈 **Resultados**

*   **Modelo seleccionado:** Gradient Boosting.
*   **Recall (clase fallo):** 86.8%.
*   **Variables más influyentes:** *Rotational speed*, *Power*, *Tool wear*.

El sistema logra una alta capacidad de detección de fallos manteniendo una interpretabilidad total para el operador industrial.

---

📊 **Dashboard (Power BI)**

Los resultados se visualizan mediante un dashboard estructurado en dos paneles:

*   **Panel 1: Monitoreo Global:** Vista general del estado de la planta.
*   **Panel 2: Análisis Detallado:** Desglose por activo para identificar causas raíz y recomendaciones.

---

🌱 **Impacto en Sostenibilidad**

Este sistema contribuye directamente a:
*   Reducción del desperdicio de componentes mecánicos.
*   Optimización de rutas e intervenciones de mantenimiento.
*   Alineación con los **ODS 9** (Industria, Innovación e Infraestructura) y **ODS 12** (Producción y Consumo Responsables).

---

📜 **Licencia**

Este proyecto ha sido desarrollado exclusivamente con fines académicos en el marco de un TFM.

---

👤 **Autor**

**Wilder Aguilar**  
*Máster en Big Data y Ciencia de Datos*