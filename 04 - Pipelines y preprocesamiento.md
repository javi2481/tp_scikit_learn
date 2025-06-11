# 🧩 04 - Pipelines y Preprocesamiento de Modelos de Machine Learning

## 1️⃣ Introducción 🚀

El proceso de Machine Learning (ML) no se limita al entrenamiento de un modelo: implica una serie de pasos bien organizados que transforman datos crudos en predicciones útiles.  
Uno de los enfoques más potentes para manejar esta complejidad es el uso de **pipelines**, que permiten automatizar, reproducir y versionar el flujo completo.

> 🎯 Un buen pipeline garantiza que las transformaciones aplicadas durante el desarrollo también se apliquen de forma idéntica en producción.

---

## 2️⃣ ¿Qué es un Pipeline de Machine Learning? 🛠️

Un **pipeline de ML** es una secuencia automatizada de pasos que organiza el flujo de trabajo completo:

### 🔄 Etapas típicas:

1. **📥 Ingesta de datos**
2. **🧹 Preprocesamiento**
3. **✂️ División del dataset**
4. **🤖 Entrenamiento del modelo**
5. **📊 Evaluación**
6. **🚀 Despliegue**
7. **📈 Monitoreo**

---

## 🔧 Herramientas populares en producción

- **Gestión de pipelines**: `Scikit-learn`, `MLflow`, `Kubeflow`, `Airflow`  
- **Versionado**: `DVC`, `MLflow`  
- **Automatización**: `Jenkins`, `GitHub Actions`  
- **Tracking de experimentos**: `Weights & Biases`, `MLflow`

---

## 3️⃣ Etapas del Preprocesamiento de Datos 🧼

1. **🧽 Limpieza de datos**
2. **🧩 Imputación de valores faltantes**
3. **📏 Escalado de variables numéricas**
4. **🏷️ Codificación de variables categóricas**
5. **🧠 Feature Engineering**
6. **✂️ Selección de variables**

---

## 4️⃣ Buenas Prácticas 🧠

✅ Automatizar todo dentro del pipeline  
✅ Aplicar las mismas transformaciones en desarrollo y producción  
✅ Evitar *data leakage*  
✅ Separar preprocesamiento del modelado  
✅ Serializar el pipeline completo  
✅ Versionar todo lo que se entrena

---

## 5️⃣ Ejemplo práctico con Scikit-learn 🤖

```python
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.impute import SimpleImputer
from sklearn.compose import ColumnTransformer
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score
import pandas as pd

# Cargar datos
iris = load_iris()
X = pd.DataFrame(iris.data, columns=iris.feature_names)
y = iris.target

# Dividir dataset
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Preprocesamiento numérico
numeric_features = X.columns.tolist()
numeric_transformer = Pipeline([
    ('imputer', SimpleImputer(strategy='mean')),
    ('scaler', StandardScaler())
])

preprocessor = ColumnTransformer([
    ('num', numeric_transformer, numeric_features)
])

# Pipeline completo
pipeline = Pipeline([
    ('preprocessor', preprocessor),
    ('classifier', RandomForestClassifier(n_estimators=100, random_state=42))
])

# Entrenar y evaluar
pipeline.fit(X_train, y_train)
y_pred = pipeline.predict(X_test)
print(f"Accuracy: {accuracy_score(y_test, y_pred):.3f}")
```

---

## 6️⃣ Conclusión 🎓

Los pipelines permiten construir flujos de trabajo robustos, reutilizables y adaptables tanto en desarrollo como en producción.

> ✅ Automatización + reproducibilidad + buenas prácticas = proyectos de ML profesionales y sostenibles.
