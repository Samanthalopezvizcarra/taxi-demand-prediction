# 🚕 Taxi Demand Prediction

Proyecto para predecir la cantidad de pedidos de taxis por hora en aeropuertos utilizando datos históricos y modelos de machine learning, optimizando precisión y eficiencia.

---

## 📘 Descripción del proyecto
La compañía **Sweet Lift Taxi** quiere anticipar la demanda de taxis durante las horas pico para atraer más conductores y mejorar la disponibilidad.  
El objetivo es predecir el **número de pedidos de taxis (`num_orders`)** para la próxima hora utilizando datos históricos.

**Métrica principal:** RECM (máximo permitido en test: 48)

---

## 🗂 Dataset
Archivo: `/datasets/taxi.csv`  

**Características principales:**
- Datos históricos de pedidos de taxis  
- Agrupados por intervalos de una hora  
- Objetivo: `num_orders` – número de pedidos por hora  

---

## 🛠️ Proceso del proyecto

### 1. Preparación de datos
- Resampleo de los datos originales a intervalos de **una hora**  
- Exploración y análisis de tendencias horarias  

---

### 2. Entrenamiento y evaluación de modelos
Se probaron distintos modelos y configuraciones de hiperparámetros:

- **Random Forest** – menor error (RMSE=40.509), modelo más preciso  
- **Gradient Boosting** – buen desempeño pero ligeramente peor, afectado por búsqueda limitada de hiperparámetros  
- Otros modelos – diferencias menores, considerando tiempos computacionales  

**Conjunto de prueba:** 10% del dataset original  

---

### 3. Observaciones
- Todos los modelos lograron **RMSE ≤ 48** en el conjunto de prueba  
- Random Forest ofrece el mejor balance entre precisión y robustez  
- En datasets grandes, es importante considerar el **tiempo computacional** al elegir modelo  

---

## 🧰 Tecnologías utilizadas
- Python  
- pandas · numpy  
- scikit-learn  
- matplotlib / seaborn  

---

## 🏆 Conclusión
- **Random Forest** es el modelo recomendado por precisión  
- Predicciones horarias permiten planificar mejor la disponibilidad de taxis y mejorar la atención al cliente
