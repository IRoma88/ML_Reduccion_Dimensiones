# Reconocimiento de Caras usando Eigenfaces

Este proyecto implementa un sistema de reconocimiento facial basado en el método de *eigenfaces* utilizando el dataset **Labeled Faces in the Wild (LFW)**.

## 📌 Objetivo

Dado un conjunto de imágenes de rostros de personas famosas, el sistema debe ser capaz de clasificar correctamente la identidad de una nueva imagen. Por ejemplo, si se introduce una foto del presidente George W. Bush, el sistema debería reconocerlo correctamente.

## 📂 Dataset

El dataset utilizado es una versión preprocesada de **LFW (Labeled Faces in the Wild)** con al menos 70 imágenes por persona:

📥 Descarga: [http://vis-www.cs.umass.edu/lfw/lfw-funneled.tgz](http://vis-www.cs.umass.edu/lfw/lfw-funneled.tgz)

El dataset es automáticamente descargado por `scikit-learn` mediante la función `fetch_lfw_people`.

## 🔧 Tecnologías utilizadas

- Python 3
- scikit-learn
- matplotlib
- numpy
- PCA (Análisis de Componentes Principales)
- SVM (Máquinas de Vectores de Soporte)

## 🧪 Pasos del proyecto

1. **Carga del dataset**: Se utilizan imágenes con al menos 70 apariciones por persona.
2. **Preprocesamiento**:
   - Reducción de tamaño de las imágenes.
   - Estandarización de los datos (`StandardScaler`).
3. **Reducción de dimensionalidad con PCA**:
   - Se extraen los 150 componentes principales para formar las *eigenfaces*.
   - Se transforman los datos originales al nuevo espacio reducido (`X_pca`).
4. **Visualización de Eigenfaces**:
   - Se muestran los rostros base que forman la base del espacio PCA.
5. **Entrenamiento y evaluación (no incluido en este snippet)**:
   - Se utiliza un clasificador SVM con búsqueda de hiperparámetros para obtener un modelo final robusto.
6. **Validación del ejercicio con token SHA256**:
   - Se genera un hash para verificar que el PCA se aplicó correctamente.

## 🖼 Ejemplo de visualización de eigenfaces

Se muestran las 150 *eigenfaces* aprendidas por el PCA, que forman la base del espacio facial para la clasificación.

## 📄 Requisitos

Asegúrate de instalar las dependencias listadas en `requirements.txt`.

## 📬 Contacto

Este proyecto es parte de un módulo de aprendizaje sobre Machine Learning con imágenes. Para dudas o colaboración, puedes abrir un issue o enviar un pull request.
