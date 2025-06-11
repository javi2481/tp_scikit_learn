# 🤖 01 - Usos comunes y algoritmos

## 🔍 Clasificación

Predicción de etiquetas o clases. Algunos modelos populares:

- **LogisticRegression**: útil para clasificación binaria y multiclase.
- **RandomForestClassifier**: basado en árboles múltiples, robusto y eficaz.
- **SVC (Support Vector Classifier)**: eficaz con márgenes maximizados.

📌 Enlaces recomendados:
- [Documentación oficial de LogisticRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
- [Random Forest Classification with Scikit-learn – DataCamp](https://www.datacamp.com/tutorial/random-forests-classifier-python)

---

## 📈 Regresión

Para predecir valores continuos como precios:

- **LinearRegression**
- **Ridge** (regresión lineal con penalización L2)
- **Lasso** (penalización L1)

📌 Usos comunes: estimación de precios inmobiliarios, predicción de ventas, forecasting económico.

---

## 🧩 Clustering

Agrupa datos sin etiquetas usando similitud:

- **KMeans**: divide en k grupos con minimización de distancias.
- **DBSCAN**: agrupa según densidad, detecta “clusters” y ruido.

📌 Enlace útil:
- [Clustering with Scikit‑Learn in Python (Programming Historian)](https://programminghistorian.org/en/lessons/clustering-with-scikit-learn-in-python)

---

## 🎨 Reducción de dimensionalidad

Técnicas para simplificar datos sin perder relevancia:

- **PCA**: útil para visualizar y reducir features.
- **t-SNE**: excelente para exploración visual de alta dimensión.

📌 Usos en visualización y preprocesamiento, especialmente en la sección de visualización.

---

## 🧪 Selección y comparación de modelos

Herramientas para encontrar el mejor modelo y configuraciones:

- `GridSearchCV` 🔍
- `RandomizedSearchCV` 🎯
- `cross_val_score` 🔄

📌 Enlace clave:
- [Classifier comparison – Scikit-learn Docs](https://scikit-learn.org/stable/auto_examples/classification/plot_classifier_comparison.html)

---

## ✅ Conclusión

Scikit-learn ofrece un **ecosistema completo** para:

- Clasificación 🔢
- Regresión 📏
- Clustering 🔍
- Reducción de dimensionalidad 🌌
- Comparación y selección de modelos 🧠

Este enfoque hace que sea ideal tanto para aprendizaje como para producción.
