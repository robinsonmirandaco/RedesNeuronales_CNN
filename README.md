# 📌 Clasificación de Imágenes CIFAR-10 con Redes Neuronales Convolucionales  
### Máster Universitario en Inteligencia Artificial – UNIR  
### Actividad Individual – Redes Neuronales  
**Estudiante:** Robinson Miranda  

---

## 📖 Descripción del proyecto

Este repositorio contiene el desarrollo completo de la actividad individual sobre **Redes Neuronales Convolucionales (CNN)** aplicada al dataset **CIFAR-10**.  
El objetivo principal es entrenar, comparar y analizar distintas arquitecturas de redes neuronales para clasificar imágenes en 10 categorías.

El proyecto incluye:

- análisis exploratorio del dataset,
- entrenamiento de un modelo *fully connected* como baseline,
- construcción de diferentes modelos CNN,
- uso de *Batch Normalization* y *Dropout*,
- implementación de *data augmentation*,
- evaluación con métricas por clase y matriz de confusión,
- análisis visual de errores.

Este trabajo fue realizado como parte del Máster en Inteligencia Artificial de UNIR.

---

## 🎯 Objetivos

- Comprender las limitaciones de un modelo totalmente conectado en visión por computador.
- Evaluar mejoras progresivas mediante arquitecturas convolucionales.
- Aplicar técnicas de regularización y normalización.
- Analizar el comportamiento del modelo mediante métricas, gráficas y visualizaciones.
- Construir un modelo CNN robusto que generalice correctamente sobre CIFAR-10.

---

## 🗂 Dataset: CIFAR-10

- 60 000 imágenes en color (32×32 px)
- 10 clases balanceadas:
  `avión, coche, ave, gato, ciervo, perro, rana, caballo, barco, camión`
- 50 000 imágenes para entrenamiento (de las cuales se separan 10 000 para validación)
- 10 000 imágenes para test

---

## 🧪 Modelos implementados

### 1️⃣ **Modelo Fully Connected (Baseline)**  
- Imagen aplanada → capas densas de 512 y 256 neuronas  
- Dropout  
- ~1.7 millones de parámetros  
- **Exactitud en test:** ~35 % (se usa solo como punto de partida)

---

### 2️⃣ **CNN Simple**
- 3 bloques Conv2D + MaxPooling  
- Capa densa final  
- **Exactitud en test:** ~74 %

---

### 3️⃣ **CNN Profunda con BatchNorm + Dropout**
- Bloques convolucionales con Batch Normalization  
- Capas de Dropout para reducir sobreajuste  
- Capa densa de 512 neuronas  
- **Exactitud en test:** ~80 %  
- **Pérdida en test:** ~0.58  

Este modelo es el mejor del proyecto.

---

## 📊 Métricas (modelo final)

- **Accuracy global:** ~81 %
- **Clases mejor clasificadas:** coche, camión, barco  
- **Clases con más confusión:** ave, gato, perro  
- **Recall destacado:** rana (0.95), caballo (0.91), avión (0.90)

---

## 🔍 Matriz de confusión

(Insertar imagen aquí si la subes al repo)

---

## 👁️ Análisis visual de errores

(Insertar imagen aquí si la subes al repo)

Los errores se concentran en:

- animales con fondos complejos,
- imágenes poco definidas,
- confusiones entre especies (gato ↔ perro, ave ↔ gato),
- posiciones o colores atípicos.

---

## 📈 Gráficas de entrenamiento

Se incluyen:

- pérdida y accuracy del modelo fully connected  
- desempeño de la CNN simple  
- curvas del modelo final con *data augmentation*  

(Insertar imágenes si las agregas al repo)

---

## 🏁 Conclusiones

- Las CNN superan ampliamente a los modelos totalmente conectados en visión por computador.  
- Batch Normalization y Dropout ayudan a estabilizar y controlar el sobreajuste.  
- Data augmentation genera mejoras reales en la capacidad de generalización.  
- El modelo final alcanza un rendimiento competitivo para ser una arquitectura construida desde cero.  
- El análisis de clases y errores permite entender los límites reales del modelo.

---


---

## 🛠 Tecnologías utilizadas

- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  
- Scikit-learn  

---


**Robinson Miranda**  
Máster Universitario en Inteligencia Artificial – UNIR  

