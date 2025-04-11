# Proyecto Análisis de Cancelación de Clientes para Interconnect

**Objetivo:**  
Desarrollar un prototipo de modelo de machine learning que permita al operador de telecomunicaciones **Interconnect** predecir con precisión qué clientes tienen mayor probabilidad de cancelar sus contratos, con el fin de activar campañas de retención personalizadas.

---

## Descripción del Proyecto

Interconnect desea reducir su tasa de cancelación de clientes mediante acciones preventivas. Para lograrlo, este proyecto analiza datos contractuales y personales de los clientes para entrenar modelos predictivos. El enfoque se centra en:

- Preprocesamiento y limpieza de datos
- Ingeniería de características
- Evaluación de múltiples algoritmos de clasificación
- Identificación de patrones clave en la cancelación de contratos

Este prototipo permite detectar clientes en riesgo de cancelar, facilitando así la oferta de promociones personalizadas y estrategias de fidelización.

---

## Hallazgos Clave

- **Los primeros meses de contrato** son críticos: es cuando más cancelaciones ocurren.
- **Pagos mensuales altos** y **el uso de métodos como el cheque electrónico** aumentan la probabilidad de cancelación.
- **Contratos a largo plazo** y **altos cargos acumulados** se asocian con menor probabilidad de churn.
  
El mejor modelo fue un **Random Forest Classifier**, con:

- AUC-ROC: `0.88`
- F1-score: `0.66`
- Precisión: `0.80`

---

##  Metodología

### 1. Preprocesamiento de Datos
- Limpieza de datos faltantes
- Tratamiento de outliers
- Corrección del desbalance de clases

### 2. Ingeniería de Características
- One-Hot Encoding para variables categóricas
- Normalización de variables numéricas
- División del dataset en `train`, `validation` y `test`

### 3. Selección de Modelos
- Se probaron: Random Forest, Logistic Regression, Decision Tree, entre otros
- Ajuste de hiperparámetros mediante **GridSearchCV**
- Evaluación con **AUC-ROC**, **F1-score** y otras métricas

### 4. Evaluación Final
- Comparación de modelos
- Selección del mejor balance entre precisión y recall
- Interpretación de resultados y variables importantes

---

##  Conclusiones

Este proyecto ofrece una solución práctica para el área de marketing y retención de Interconnect. Con un modelo robusto y explicable, la empresa puede anticipar cancelaciones y tomar acciones preventivas, mejorando significativamente la lealtad del cliente y reduciendo la pérdida de ingresos.

---

## Archivos Incluidos

- `interconnect_churn_analysis.ipynb` – Notebook principal del análisis
- `requirements.txt` – Dependencias del proyecto
- `README.md` – Descripción general del proyecto

Los datos utilizados en este proyecto fueron proporcionados por Tripleten con fines educativos. Por razones de privacidad y propiedad intelectual, no se incluyen en este repositorio.

Si deseas replicar este análisis, puedes sustituir los datos con un conjunto similar de clientes.

---

## Tecnologías Usadas

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
- Jupyter Notebook

---


