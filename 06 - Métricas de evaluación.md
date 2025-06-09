# 📏 08 - Métricas de evaluación

Evaluar un modelo de Machine Learning es tan importante como entrenarlo.  
Las métricas nos ayudan a entender qué tan bien está funcionando el modelo y si realmente cumple con su propósito.

---

## 🟩 Clasificación

Se utiliza cuando queremos predecir **categorías** o **etiquetas discretas** (por ejemplo: "spam" vs. "no spam").

### Métricas principales:

- **Accuracy (Precisión global)** ✅  
  Porcentaje de predicciones correctas sobre el total.

- **Precision (Precisión positiva)** 🎯  
  ¿De las predicciones positivas, cuántas fueron correctas?

- **Recall (Sensibilidad)** 🔍  
  ¿Cuántos positivos reales fueron detectados?

- **F1-score** ⚖️  
  Media armónica entre precision y recall. Muy útil si hay clases desbalanceadas.

- **Matriz de confusión** 🔲  
  Muestra los verdaderos positivos, falsos positivos, falsos negativos y verdaderos negativos.

### Ejemplo:

```python
from sklearn.metrics import confusion_matrix, classification_report

y_true = [1, 0, 1, 1, 0, 1]
y_pred = [1, 0, 1, 0, 0, 1]

print(confusion_matrix(y_true, y_pred))
print(classification_report(y_true, y_pred))
```

---

## 📊 Regresión

Se usa cuando el objetivo es predecir un **valor numérico continuo** (por ejemplo: precio de un auto, temperatura, ventas).

### Métricas comunes:

- **MAE (Mean Absolute Error)** 📉  
  Promedio de los errores absolutos.

- **MSE (Mean Squared Error)** 📈  
  Promedio de los errores al cuadrado (penaliza más los grandes errores).

- **RMSE (Root Mean Squared Error)**  
  Raíz cuadrada del MSE, mantiene las unidades originales.

- **R² Score (Coeficiente de determinación)** 🔢  
  Qué porcentaje de la variación en los datos es explicada por el modelo.

---

## 🧪 Visualizaciones complementarias

- **Curvas ROC** y **AUC** para evaluar clasificadores binarios  
- **Curvas de validación y aprendizaje** para observar el comportamiento del modelo

🔗 [Scikit-learn - Métricas y scoring](https://scikit-learn.org/stable/modules/model_evaluation.html)

---

## ✅ Conclusión

Elegir la métrica adecuada depende del tipo de problema.  
Medir correctamente el rendimiento permite mejorar modelos, comparar alternativas y tomar decisiones basadas en datos reales.
