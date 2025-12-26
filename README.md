# 🎯 Modelos de machine learning: predicción de Abandono de Clientes (Churn Prediction)

Este proyecto utiliza técnicas de machine learning para predecir la probabilidad de que un cliente abandone un servicio. El análisis se basa en un dataset con características demográficas y de comportamiento, aplicando modelos como XGBoost, LightGBM, Random Forest, Logistic Regression y un modelo de ensamble (stacking).

El objetivo es desarrollar modelos capaces de identificar de forma anticipada a los clientes con mayor riesgo de cancelar sus servicios. Esto permitirá a la empresa implementar acciones preventivas para mejorar la retención, apoyándose en un pipeline de modelado sólido desde esta fase inicial. Se estudian patrones en variables contractuales, uso de servicios digitales y métodos de pago, integrando análisis exploratorio, matriz de correlaciones y explicaciones mediante SHAP.

> 🔄 **Este repositorio corresponde a la segunda etapa del proyecto**, enfocada en *Machine Learning*.  
> La primera parte, dedicada al **análisis e ingeniería de datos** sobre el mismo dataset, puede consultarse aquí: [Challenge2-Alura-Store](https://github.com/BarbaraAngelesOrtiz/Challenge2-Alura-Store).


---

## ✏️Metas Principales

- Realizar un tratamiento exhaustivo de los datos, incluyendo limpieza, codificación y escalado.  
- Analizar la relación entre variables para seleccionar las más relevantes para la predicción.  
- Entrenar y comparar diferentes modelos de clasificación para detectar abandono.  
- Evaluar los modelos con métricas que reflejen su desempeño real.  
- Analizar la importancia de las variables y su impacto en la predicción.  
- Presentar conclusiones con recomendaciones basadas en los factores clave que impulsan la cancelación.

---

## 💡Actividades Desarrolladas

- Procesamiento y preparación de datos para alimentar los modelos de machine learning.  
- Construcción, entrenamiento y validación de modelos predictivos.  
- Interpretación de resultados para extraer insights valiosos.  
- Elaboración de comunicación técnica orientada a la toma de decisiones estratégicas.

---

## 📁 Estructura del Proyecto

```bash
├── TelecomX_LATAM2_es.ipynb  #Código en español        
├── TelecomX_LATAM2_en.ipynb  #Código en inglés          
├── imag                      # Gráficos
├── src                       # Dataset
└── requirements.txt          # Librerías necesarias para ejecutar el proyecto
```

---

## 🛠️ Tecnologías y Librerías Utilizadas

Python 3.x
Google Colab (entorno de desarrollo)
Pandas, NumPy (manipulación y análisis de datos)
Matplotlib, Seaborn, Plotly (visualización)
scikit-learn (modelado y evaluación)
XGBoost, LightGBM (modelos de boosting)
imbalanced-learn (manejo de datos desbalanceados)
SHAP (interpretabilidad de modelos)
Requests (conexión con APIs externas)
Jupyter Notebooks

---

## 📚Datos

El dataset contiene variables como:

- Tipo de contrato (mensual, dos años)
- Tipo de conexión a internet (fibra óptica, DSL, sin internet)
- Uso de servicios digitales (streaming, facturación electrónica)
- Métodos de pago (cheque electrónico, tarjeta, débito automático)
- Antigüedad del cliente (tenure)
- Variables de soporte técnico y seguridad online
- Variable objetivo: churn (abandono)

---

## ⚖️ Modelos y Evaluación

Se implementan y comparan los siguientes modelos:

- Logistic Regression
- Random Forest
- XGBoost
- LightGBM
- Stacking Ensemble
- K-nearest neighbors 

Métricas principales usadas:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC AUC

---

## 🔖 Comparativa de Modelos

Según métricas:

| Modelo                 | Accuracy | Precision | Recall   | F1 Score | ROC AUC  | Observaciones                                            |
| ---------------------- | -------- | --------- | -------- | -------- | -------- | -------------------------------------------------------- |
| **XGBoost**            | 0.783   | 0.575    | 0.701   | 0.631   | 0.845   | Buen balance general, excelente ROC AUC y recall alto  |
| **LightGBM**           | 0.774   | 0.560    | 0.703   | 0.623   | 0.843   | Muy parecido a XGBoost, buen recall y precisión        |
| **LogisticRegression** | 0.744  | 0.511   | 0.786   | 0.620   | 0.843   | Mejor recall (sensibilidad), menor precisión           |
| **RandomForest**       | 0.776   | 0.560    | 0.722   | 0.631   | 0.841   | Recall alto, buen balance general                      |
| **Stacking Ensemble**  | 0.779   | 0.578    | 0.623  | 0.600  | 0.834  | Mejor precisión, un poco menor recall y F1             |
| **KNN**                | 0.714  | 0.475   | 0.725   | 0.574  | 0.794  | Menor accuracy y precisión, pero recall aceptable      |

Según Matriz de Confusión:

| Modelo                  | TN  | FP  | FN  | TP  | Observaciones                                                                  |
| ----------------------- | --- | --- | --- | --- | ------------------------------------------------------------------------------ |
| **KNN**                 | 735 | 300 | 103 | 271 |  Buen Recall (TP alto) <br>  Muchos Falsos Positivos (FP altos)            |
| **LightGBM**            | 828 | 207 | 111 | 263 |  Buen equilibrio <br>  Algo más FN que KNN, pero menos FP                   |
| **XGBoost**             | 841 | 194 | 112 | 262 |  Mejor TN (FP bajo) <br>  FN similar a LightGBM                             |
| **RandomForest**        | 823 | 212 | 104 | 270 |  Balanceado <br>  FN ligeramente mejor que XGBoost                          |
| **LogisticRegression**  | 754 | 281 | 80  | 294 |  Mejor FN (menos falsos negativos) <br>  Más FP (riesgo de costos mayores)  |
| **Ensamble (Stacking)** | 865 | 170 | 141 | 233 |  Mejor TN (menos FP) <br>  Más FN (riesgo de perder clientes que abandonan) |


🎯 Modelo seleccionado: **XGBoost** ya que entrega un modelo robusto, con buen poder predictivo y balanceado, ideal para minimizar tanto la pérdida de clientes (por recall alto) como evitar falsos alarmas (por precisión razonable). Es un modelo que se adapta bien a la mayoría de los casos de negocio donde hay que manejar el trade-off entre capturar abandonos y no sobre-reaccionar.

---

## 📊 Ejemplo de Visualización

#### Curvas ROC comparativas de todos los modelos
<img width="691" height="547" alt="Curvas ROC comparativas de todos los modelos" src="https://github.com/user-attachments/assets/f004beb9-8c7d-4e6b-9568-b290baa9097b" />

#### Comparación de modelos métricas de clasificación
<img width="846" height="548" alt="Comparación de modelos métricas de clasificación" src="https://github.com/user-attachments/assets/cbaa9079-bac5-47aa-84e3-d16b6441f5fa" />

#### Comparativa de desempeño entre modelos
<img width="863" height="690" alt="Comparativa de desempeño entre modelos" src="https://github.com/user-attachments/assets/106b72fc-2d66-4d0c-9b9e-41397754ca3c" />

#### Curvas Precision-Recall comparativas de todos los modelos
<img width="691" height="547" alt="Curvas Precision-Recall comparativas de todos los modelos" src="https://github.com/user-attachments/assets/21cb3e6a-b952-439d-b0f0-dfd5592820bb" />

---

## 🛠️ Instrucciones para Ejecutar el Notebook

1. Cloná o descargá este repositorio:

```bash
git clone https://github.com/usuario/proyecto-churn.git 
```
2. Instalá las dependencias necesarias (recomendado: usar un entorno virtual):

```bash
pip install pandas matplotlib seaborn numpy plotly math matplotlib requests
```
3. Abrí el notebook en Jupyter, VSCode o Google Colab

4. Ejecutá las celdas secuencialmente para replicar el análisis completo.

----

## 📂 Project Access

- [Notebook in Spanish](./TelecomX_LATAM2_es.ipynb)
- [Notebook in English](./TelecomX_LATAM2_en.ipynb)

---

## Author
**Bárbara Ángeles Ortiz**

<img src="https://github.com/user-attachments/assets/30ea0d40-a7a9-4b19-a835-c474b5cc50fb" width="115">

[LinkedIn](https://www.linkedin.com/in/barbaraangelesortiz/) | [GitHub](https://github.com/BarbaraAngelesOrtiz)

![Status](https://img.shields.io/badge/status-finished-brightgreen) 📅 Agosto 2025

![Python](https://img.shields.io/badge/python-3.10-blue)

![NumPy](https://img.shields.io/badge/numpy-1.26.0-blue)

![Pandas](https://img.shields.io/badge/pandas-2.1.0-blue)


## Agradecimientos 

<img width="180" height="180" alt="Screenshot 2025-08-13 034705" src="https://github.com/user-attachments/assets/bdfa03bc-d44a-4848-b622-6bac4e2dbc95" />

<img width="180" height="180" alt="images" src="https://github.com/user-attachments/assets/8ca15294-1738-45a7-af65-7a390e468937" />

<img width="180" height="180" alt="Oracle-Next-Education--e16783040" src="https://github.com/user-attachments/assets/8912c5a0-58d7-45af-ba13-d2a9f42cde5a" />


