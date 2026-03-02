# Promesa vs. Realidad: Optimización Logística en Superstore

Este proyecto fue desarrollado como parte de la entrega de Ciencia de Datos. El objetivo es analizar los tiempos de entrega y la rentabilidad de una empresa de retail, utilizando técnicas de **Análisis Exploratorio de Datos (EDA)** y **Machine Learning**.

## Motivación y Audiencia
El mercado actual exige inmediatez. Sin embargo, la brecha entre lo que se promete al cliente y la capacidad de despacho real puede generar pérdidas críticas. 
* **Audiencia:** Dirección de Experiencia del Cliente y Gerencia de Operaciones.
* **Problema:** Incumplimiento sistemático en la categoría de Tecnología y saturación logística en meses específicos.

## Tecnologías Utilizadas
* **Lenguaje:** Python, Google Colab
* **Librerías:** Pandas, Numpy, Scikit-Learn, Matplotlib, Seaborn.
* **Fuentes Externas:** Conexión vía API a [Nager.Date](https://date.nager.at/) para la obtención de feriados nacionales en EE.UU.

## Hallazgos Clave
1. **Puntos Críticos:** La categoría de Furniture presenta grandes perdidas en la Region Central.
2. **Impacto Estacional:** Los feriados atrasan los pedidos. Los meses de abril y mayo muestran colapsos operativos con tasas de retraso superiores.
3. **Rentabilidad:** El exceso de descuentos en la Región Central es el principal predictor de pérdidas financieras.

## Modelos de Machine Learning
Se implementaron dos enfoques principales:
* **Clasificación (Random Forest):** Para predecir la probabilidad de retraso de un pedido antes de ser despachado.
* **Regresión (Linear & Random Forest):** Para estimar el beneficio proyectado de cada venta en función de sus características.

## Estructura del Repositorio
* `Cinthia_Debenedetto_Superstore_cd2.ipynb`: Notebook con el proceso completo de ETL, EDA y Modelado.
* `Presentacion y conclusiones Superstore.pdf`: Resumen de insights para la dirección.
* `Proyecto Superstore.ppt`: Presentacion en PowerPoint del proyecto.
*Data
     * `Sample - Superstore.csv`: Dataset original.
     *  `superstore_enriquecido.csv`: Nuevo Dataset enriquecido con datos de API.
     *  `feriados_usa.csv`: Datos obtenidos mediante API.


