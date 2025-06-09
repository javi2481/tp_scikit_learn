# 🧩 06 - Pipelines y Preprocesamiento de Modelos de Machine Learning

## 1️⃣ Introducción 🚀

El proceso de Machine Learning (ML) no se limita al entrenamiento de un modelo: implica una serie de pasos bien organizados que transforman datos crudos en predicciones útiles.  
Uno de los enfoques más potentes para manejar esta complejidad es el uso de **pipelines**, que permiten automatizar, reproducir y versionar el flujo completo.

> 🎯 Un buen pipeline garantiza que las transformaciones aplicadas durante el desarrollo también se apliquen de forma idéntica en producción.

---

## 2️⃣ ¿Qué es un Pipeline de Machine Learning? 🛠️

Un **pipeline de ML** es una secuencia automatizada de pasos que organiza el flujo de trabajo completo:

### 🔄 Etapas típicas:

1. **📥 Ingesta de datos**
   - Carga desde archivos, APIs, bases de datos.
   - Control de versiones con herramientas como DVC.

2. **🧹 Preprocesamiento**
   - Limpieza, imputación, escalado, codificación, ingeniería de variables.

3. **✂️ División del dataset**
   - Separación en entrenamiento, validación y test.

4. **🤖 Entrenamiento del modelo**
   - Elección del algoritmo.
   - Ajuste de hiperparámetros (GridSearch, RandomizedSearch).

5. **📊 Evaluación**
   - Validación cruzada, métricas y visualizaciones.
   - Interpretabilidad con SHAP, LIME.

6. **🚀 Despliegue**
   - Serialización con `joblib`, `pickle`, `ONNX`.
   - Exposición como API, procesos batch, o dispositivos edge.

7. **📈 Monitoreo**
   - Seguimiento de métricas en producción.
   - Detección de _data drift_ y _model drift_.

---

## 🔧 Herramientas populares en producción

- **Gestión de pipelines**: `Scikit-learn`, `MLflow`, `Kubeflow`, `Airflow`  
- **Versionado**: `DVC`, `MLflow`  
- **Automatización**: `Jenkins`, `GitHub Actions`  
- **Tracking de experimentos**: `Weights & Biases`, `MLflow`

---

## 3️⃣ Etapas del Preprocesamiento de Datos 🧼

Un buen preprocesamiento mejora la calidad de los datos y el rendimiento del modelo.

### Etapas comunes:

1. **🧽 Limpieza de datos**  
   - Quitar duplicados, corregir errores, detectar valores atípicos.

2. **🧩 Imputación de valores faltantes**  
   - Usar media, mediana o modelos predictivos.

3. **📏 Escalado de variables numéricas**  
   - `StandardScaler`: media 0, desvío estándar 1  
   - `MinMaxScaler`: escala los valores entre 0 y 1

4. **🏷️ Codificación de variables categóricas**  
   - `OneHotEncoder`, `LabelEncoder`, o embeddings

5. **🧠 Feature Engineering**  
   - Crear nuevas variables útiles

6. **✂️ Selección de variables**  
   - Usar métodos como `SelectKBest`, `RFE`, o análisis de correlación

> ⚠️ Un preprocesamiento deficiente puede introducir sesgos o afectar la precisión del modelo.

---

## 4️⃣ Buenas Prácticas 🧠

✅ Automatizar todo dentro del pipeline  
✅ Aplicar las mismas transformaciones en desarrollo y producción  
✅ Evitar *data leakage* (usar datos del test sin querer)  
✅ Separar claramente preprocesamiento y modelado  
✅ Serializar el pipeline completo  
✅ Versionar el modelo y los transformadores

---

## 5️⃣ Ejemplo práctico con Scikit-learn 🤖

```python
import pandas as pd
import numpy as np
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.impute import SimpleImputer
from sklearn.compose import ColumnTransformer
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score

# 🌸 1. Cargar dataset Iris
iris = load_iris()
X = pd.DataFrame(iris.data, columns=iris.feature_names)
y = iris.target

# ✂️ 2. Dividir en train/test
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# 🧹 3. Preprocesamiento numérico
numeric_features = X.columns.tolist()
numeric_transformer = Pipeline(steps=[
    ('imputer', SimpleImputer(strategy='mean')),       # Imputar valores faltantes con la media
    ('scaler', StandardScaler())                       # Escalar los datos numéricos
])

# 🔄 4. Armar ColumnTransformer (solo numérico en este caso)
preprocessor = ColumnTransformer(transformers=[
    ('num', numeric_transformer, numeric_features)
])

# 🏗️ 5. Crear pipeline completo
pipeline = Pipeline(steps=[
    ('preprocessor', preprocessor),                    # Primer paso: preprocesar
    ('classifier', RandomForestClassifier(n_estimators=100, random_state=42))  # Segundo paso: modelo
])

# 🧠 6. Entrenar modelo
pipeline.fit(X_train, y_train)

# 📊 7. Predecir y evaluar
y_pred = pipeline.predict(X_test)
print(f"Accuracy: {accuracy_score(y_test, y_pred):.3f}")
```

---

## 6️⃣ Conclusión 🎓

Los pipelines permiten construir flujos de trabajo robustos, reutilizables y adaptables tanto en desarrollo como en producción.

> ✅ Automatización + reproducibilidad + buenas prácticas = proyectos de ML profesionales y sostenibles.
