# Promesa vs. Realidad: Optimización Logística en Superstore

Este proyecto de Ciencia de Datos aplica un enfoque integral de ingeniería para optimizar la cadena de valor de una empresa de retail. A través de modelos de Aprendizaje Supervisado y No Supervisado, se busca predecir fallas logísticas y blindar la rentabilidad financiera.

## Motivación y Audiencia
En un entorno de competencia agresiva, la ineficiencia logística y las políticas de descuentos descontroladas destruyen el margen neto.

## Audiencia: Gerencia de Operaciones y Dirección Financiera.

Problema: Incumplimiento sistemático en entregas "First Class" y erosión del Profit por exceso de descuentos en categorías críticas.

## Tecnologías Utilizadas
Lenguaje: Python (Google Colab).

*Modelado: XGBoost (Extreme Gradient Boosting) y K-Means Clustering.

*Optimización: GridSearchCV para ajuste fino de hiperparámetros.

*Validación: Stratified Cross-Validation (K-Fold) para asegurar robustez estadística.

*Visualización: Matplotlib, Seaborn, Plotly (3D Clustering).

F*uentes Externas: Conexión vía API a Nager.Date para el análisis de estacionalidad por feriados.

## Hallazgos Clave
1. El Mito de los Feriados: Mediante análisis de densidad (KDE), se demostró que los feriados nacionales no impactan significativamente en las demoras. El cuello de botella es estructural y no estacional.

2. Falla Operativa: El modo de envío "First Class" es el principal predictor de retrasos, indicando una saturación en el proceso de despacho prioritario.

3. Umbral de Rentabilidad: Se identificó que descuentos superiores al 20% disparan la probabilidad de pérdida (Profit negativo), especialmente en la categoría de Furniture.

## Modelos de Machine Learning implementados

1. Clasificación (Aprendizaje Supervisado)
   *Modelo: XGBClassifier (Boosting).
   *Objetivo: Predecir la probabilidad de retraso de un pedido.Técnica: Stratified K-Fold CV y balanceo de clases mediante scale_pos_weight.

3. Regresión (Aprendizaje Supervisado)
   *Modelo: XGBRegressor (Boosting).
   *Objetivo: Estimar el Profit proyectado de cada venta.Performance: R^2 de 0.61 y MAE de 9.94 USD, permitiendo una planificación financiera con alta precisión.

5. Segmentación Estratégica (Aprendizaje No Supervisado)
   *Modelo: K-Means Clustering ($k=4$).Métricas:
   *Optimización mediante Método del Codo y Coeficiente de Silhouette.Resultado: Identificación de 4 clústeres de negocio: "Las Joyas", "Hemorragia de Margen", "Volumen Crítico" y "Pedidos Hormiga".
   
## Estructura del Repositorio

* `Cinthia_Debenedetto_Superstore_cd2.ipynb`: Notebook completo con ETL, Pipeline de modelado y optimización.
* `Presentacion y conclusiones Superstore.pdf`: Resumen de insights para la dirección.
* `Proyecto Superstore.ppt`: Presentacion en PowerPoint del proyecto.
*Data
     * `Sample - Superstore.csv`: Dataset original.
     *  `superstore_enriquecido.csv`: Nuevo Dataset enriquecido con datos de API.
     *  `feriados_usa.csv`: Datos obtenidos mediante API.

