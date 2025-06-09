# 🔗 05 - Integración con otras bibliotecas

Scikit-learn se destaca por su **interoperabilidad** con otras herramientas del ecosistema de Python para ciencia de datos y machine learning.

---

## 🧮 NumPy y SciPy

- Scikit-learn utiliza **NumPy** para manejar arrays y operaciones numéricas.  
- Emplea funciones estadísticas de **SciPy** en algoritmos como regresión logística, k-means, etc.

🔗 [NumPy - documentación oficial](https://numpy.org/doc/)  
🔗 [SciPy - documentación oficial](https://docs.scipy.org/doc/scipy/)

---

## 📊 Pandas

- Permite manipular y explorar datasets tabulares.  
- Muchos métodos de Scikit-learn aceptan directamente estructuras de Pandas (`DataFrame` y `Series`).

Ejemplo:
```python
import pandas as pd
from sklearn.linear_model import LinearRegression

df = pd.read_csv("datos.csv")
X = df[["col1", "col2"]]
y = df["objetivo"]

model = LinearRegression().fit(X, y)
```

---

## 🎨 Matplotlib y Seaborn

- Usadas para generar gráficos durante el análisis exploratorio y evaluación de modelos.
- Scikit-learn produce visualizaciones como **matriz de confusión** y **curvas de validación**.

🔗 [Guía de visualización con Seaborn](https://seaborn.pydata.org/examples/index.html)

---

## 💾 Joblib y Pickle

- Se usan para guardar modelos entrenados.  
- `joblib` es más eficiente que `pickle` con objetos grandes como árboles o pipelines.

Ejemplo:
```python
from joblib import dump, load

# Guardar modelo
dump(model, 'modelo_entrenado.joblib')

# Cargar modelo
modelo_cargado = load('modelo_entrenado.joblib')
```

---

## 🔬 Otras integraciones útiles

- **MLflow**: tracking de experimentos + versionado + deploy  
- **DVC**: versionado de datos y modelos  
- **XGBoost/LightGBM**: permiten integrarse como estimadores dentro de pipelines

---

## ✅ Conclusión

Scikit-learn está diseñado para trabajar junto a bibliotecas populares.  
Esto facilita el flujo de trabajo, desde la exploración hasta el deploy de modelos, dentro de un entorno Python unificado.
