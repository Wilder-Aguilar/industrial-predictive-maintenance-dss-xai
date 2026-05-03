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

⚙️ **Metodología**

El proceso metodológico se estructura en tres bloques interrelacionados que conforman el *pipeline* del sistema:

## 1. Bloque de Datos

* **Análisis Exploratorio:** Identificación de patrones y estados iniciales del dataset AI4I 2020.
* **Preprocesamiento:** Limpieza de datos y balanceo de clases mediante la técnica **SMOTE**.
* **Ingeniería de Características:** Generación de variables derivadas críticas (*Power*, *Temperature_difference* y *Mechanical_stress*).

## 2. Bloque de Modelado

* **Modelado ML:** Implementación y entrenamiento de algoritmos (*Random Forest*, *Gradient Boosting* y *SVM*).
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

* **Modelo seleccionado:** Gradient Boosting.
* **Recall (clase fallo):** 86.8%.
* **Variables más influyentes:** *Rotational speed*, *Power*, *Tool wear*.

El sistema logra una alta capacidad de detección de fallos manteniendo una interpretabilidad total para el operador industrial.

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

📜 **Licencia**
Este proyecto ha sido desarrollado exclusivamente con fines académicos en el marco de un TFM.

---

👤 **Autor**

**Wilder Aguilar**  
Máster en Big Data y Ciencia de Datos
