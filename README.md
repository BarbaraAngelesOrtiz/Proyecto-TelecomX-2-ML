# 🎯 Predicción de Abandono de Clientes (Churn Prediction)

Este proyecto utiliza técnicas de machine learning para predecir la probabilidad de que un cliente abandone un servicio. El análisis se basa en un dataset con características demográficas y de comportamiento, aplicando modelos como XGBoost, LightGBM, Random Forest, Logistic Regression y un modelo de ensamble (stacking).

El objetivo es desarrollar modelos capaces de identificar de forma anticipada a los clientes con mayor riesgo de cancelar sus servicios. Esto permitirá a la empresa implementar acciones preventivas para mejorar la retención, apoyándose en un pipeline de modelado sólido desde esta fase inicial. Se estudian patrones en variables contractuales, uso de servicios digitales y métodos de pago, integrando análisis exploratorio, matriz de correlaciones y explicaciones mediante SHAP.

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
├── _src   # Gráficos
├── requirements.txt       # Librerías necesarias para ejecutar el proyecto
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

Métricas principales usadas:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC AUC

---

## 📊 Ejemplo de Visualización

### Recuento de evasión por variables categóricas

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
3. Abrí el notebook en Jupyter, VSCode o Google Colab:

4. Ejecutá las celdas secuencialmente para replicar el análisis completo.

---

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


