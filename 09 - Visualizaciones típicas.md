# 📊 12 - Visualizaciones típicas

Visualizar los resultados de modelos de machine learning es fundamental para interpretar su comportamiento y detectar errores.

Scikit-learn incluye herramientas de visualización integradas y también se complementa muy bien con bibliotecas como **matplotlib** y **seaborn**.

---

## 🔲 Matriz de confusión

Permite observar cuántas predicciones fueron correctas y en qué clases se equivocó el modelo.

```python
from sklearn.metrics import ConfusionMatrixDisplay

ConfusionMatrixDisplay.from_estimator(model, X_test, y_test)
```

📌 Se usa principalmente en tareas de clasificación.

---

## 📉 Curvas de validación

Muestran cómo cambia la performance al variar un hiperparámetro.

```python
from sklearn.model_selection import validation_curve
```

✅ Ayuda a detectar **overfitting** (sobreajuste) y **underfitting** (subajuste).

---

## 📈 Curvas de aprendizaje

Permiten visualizar cómo afecta el tamaño del dataset al rendimiento del modelo.

```python
from sklearn.model_selection import learning_curve
```

Se grafican resultados de entrenamiento y validación.

---

## 🧪 ROC y AUC

Evaluación visual para clasificadores binarios.

```python
from sklearn.metrics import RocCurveDisplay

RocCurveDisplay.from_estimator(model, X_test, y_test)
```

Muestra la relación entre el **true positive rate** y el **false positive rate**.

---

## 📌 Importancia de variables

Muchos modelos permiten visualizar qué características (features) fueron más relevantes.

```python
import matplotlib.pyplot as plt

importances = model.feature_importances_
plt.bar(range(len(importances)), importances)
plt.title("Importancia de cada feature")
plt.show()
```

Modelos compatibles: árboles, RandomForest, XGBoost, etc.

---

## ✅ Conclusión

Visualizar modelos permite:

- Comunicar mejor los resultados
- Justificar decisiones de negocio
- Corregir errores de modelado

👁️ ¡Un gráfico vale más que mil predicciones!
