# Changelog

Todos los cambios notables en este proyecto serán documentados en este archivo.

El formato está basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/)
y este proyecto se adhiere a [Semantic Versioning](https://semver.org/lang/es/).

## [1.0.0] - 2026-10-18

### Añadido
- Implementación de pipeline modularizado de Machine Learning para clasificación de anomalías.
- Preprocesamiento de datos: imputación de nulos, escalado (`StandardScaler`) y codificación One-Hot (`OneHotEncoder`)[cite: 1].
- Entrenamiento y tuning de modelos: Regresión Logística, Random Forest y XGBoost usando `GridSearchCV`.
- Integración con **MLflow** para registro de parámetros, métricas (Accuracy, Precision, Recall, F1, ROC-AUC) y matrices de confusión/curvas ROC.
- Pruebas de hipótesis estadísticas ($t$-Student y Wilcoxon) para validación comparativa de modelos.
- Exportación del dataset limpio a `data/ACT5_dataset_Limpio_Procesado.csv`.
- Estructura del repositorio organizada con directorios `data/` y `Fuentes/`.

### Cambios
- Migración del registro de modelos a `mlflow.sklearn.log_model` para evitar incompatibilidades de tipo `Pipeline`.
- Reestructuración de carpetas en el repositorio remoto de GitHub.
