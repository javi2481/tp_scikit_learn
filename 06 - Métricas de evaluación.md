# 📏 06 - Métricas de evaluación

Evaluar un modelo de Machine Learning es tan importante como entrenarlo.  
Las métricas nos ayudan a entender qué tan bien está funcionando el modelo y si realmente cumple con su propósito.

---

## 🟩 Clasificación

Se utiliza cuando queremos predecir **categorías** o **etiquetas discretas** (por ejemplo: "spam" vs. "no spam").

### Métricas principales:

- **Accuracy (Precisión global)** ✅  
- **Precision (Precisión positiva)** 🎯  
- **Recall (Sensibilidad)** 🔍  
- **F1-score** ⚖️  
- **Matriz de confusión** 🔲  

```python
from sklearn.metrics import confusion_matrix, classification_report

y_true = [1, 0, 1, 1, 0, 1]
y_pred = [1, 0, 1, 0, 0, 1]

print(confusion_matrix(y_true, y_pred))
print(classification_report(y_true, y_pred))
```

---

## 📊 Regresión

Se usa cuando el objetivo es predecir un **valor numérico continuo**.

- **MAE (Mean Absolute Error)** 📉  
- **MSE (Mean Squared Error)** 📈  
- **RMSE (Root Mean Squared Error)**  
- **R² Score (Coeficiente de determinación)** 🔢  

---

## 🧪 Visualizaciones complementarias

- **Curvas ROC** y **AUC**  
- **Curvas de validación y aprendizaje**

🔗 [Scikit-learn - Métricas y scoring](https://scikit-learn.org/stable/modules/model_evaluation.html)

---

## ✅ Conclusión

Elegir la métrica adecuada depende del tipo de problema.  
Medir correctamente el rendimiento permite mejorar modelos, comparar alternativas y tomar decisiones basadas en datos reales.
