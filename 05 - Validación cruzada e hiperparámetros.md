# 🔁 07 - Validación cruzada e hiperparámetros

## 🎯 ¿Por qué validar?

Al entrenar un modelo, queremos asegurarnos de que **generaliza bien** y no simplemente memoriza los datos de entrenamiento.  
Aquí entra en juego la **validación cruzada**, una técnica para evaluar la robustez de un modelo.

---

## 🔄 ¿Qué es la validación cruzada?

Consiste en dividir los datos en varias particiones o *folds*. El modelo se entrena en algunos folds y se prueba en otros.  
La variante más común es la **k-fold cross-validation** (por ejemplo, k=5).

✅ Ventajas:
- Evalúa el rendimiento promedio
- Disminuye el riesgo de overfitting
- Aumenta la confiabilidad del modelo

🔗 [Explicación detallada en Scikit-learn](https://scikit-learn.org/stable/modules/cross_validation.html)

---

## 🔧 Ajuste de hiperparámetros

Los **hiperparámetros** no se aprenden del dataset, sino que se configuran manualmente o mediante búsqueda.  
Ejemplos: `n_estimators`, `max_depth`, `kernel`, `alpha`.

### Herramientas de Scikit-learn:

- `GridSearchCV`: prueba todas las combinaciones posibles 🔍  
- `RandomizedSearchCV`: selecciona combinaciones al azar 🎲  
- `HalvingGridSearchCV`: búsqueda eficiente y escalable ⚡

---

## 📉 Ejemplo: curva de validación

```python
from sklearn.datasets import load_digits
from sklearn.svm import SVC
from sklearn.model_selection import validation_curve
import numpy as np
import matplotlib.pyplot as plt

X, y = load_digits(return_X_y=True)
param_range = np.logspace(-6, -1, 5)

train_scores, test_scores = validation_curve(
    SVC(), X, y, param_name="gamma", param_range=param_range, cv=5, scoring="accuracy"
)

plt.plot(param_range, test_scores.mean(axis=1))
plt.xscale("log")
plt.title("Curva de validación")
plt.xlabel("gamma")
plt.ylabel("Accuracy")
plt.show()
```

---

## 📊 Curva de aprendizaje

Permite ver cómo se comporta un modelo a medida que se entrena con más datos.

```python
from sklearn.model_selection import learning_curve

train_sizes, train_scores, test_scores = learning_curve(
    SVC(gamma=0.001), X, y, cv=5, train_sizes=np.linspace(0.1, 1.0, 5)
)
```

---

## ✅ Conclusión

La validación cruzada y el ajuste de hiperparámetros son pasos clave en el desarrollo de modelos.  
Permiten evaluar de forma más justa, evitar errores y encontrar la mejor configuración posible.
