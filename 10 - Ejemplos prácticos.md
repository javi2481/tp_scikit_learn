# 🧪 10 - Ejemplos prácticos explicados

Aquí se presentan ejemplos simples usando Scikit-learn, explicados paso a paso.

---

## 1️⃣ 🎓 ¿Aprobará el examen?

### 🧩 Planteo del problema
Queremos predecir si un estudiante aprobará un examen en base a su cantidad de horas de estudio.

### 🛠️ Resolución
Usamos un modelo de **regresión logística**, que predice valores binarios (0 o 1).

```python
from sklearn.linear_model import LogisticRegression

X = [[1], [2], [3], [4], [5], [6], [7]]  # Horas estudiadas
y = [0, 0, 0, 1, 1, 1, 1]               # 0 = no aprueba, 1 = aprueba

# Entrenamos el modelo
model = LogisticRegression().fit(X, y)

# Predecimos para 3.5 horas
print(model.predict([[3.5]]))  # Resultado: [1]
```

### ✅ Interpretación
El modelo predice que un estudiante con 3.5 horas de estudio **aprobará**.

---

## 2️⃣ 🏠 Precio de una casa

### 🧩 Planteo
Queremos estimar el precio de una casa según su tamaño en m².

### 🛠️ Resolución
Usamos **regresión lineal**, ideal para variables continuas.

```python
from sklearn.linear_model import LinearRegression

X = [[50], [60], [70], [80], [90]]
y = [100, 120, 140, 160, 180]

model = LinearRegression().fit(X, y)
print(model.predict([[75]]))  # Resultado: 150
```

### ✅ Interpretación
Una casa de 75 m² costaría aproximadamente **150 mil unidades** monetarias.

---

## 3️⃣ 🍔 Calorías según grasa

### 🧩 Planteo
Predecir la cantidad de calorías de un alimento según su contenido graso (en gramos).

```python
X = [[2], [5], [8], [11], [14], [17], [20]]
y = [50, 100, 140, 180, 220, 260, 300]

model = LinearRegression().fit(X, y)
print(model.predict([[10]]))  # Resultado: 160
```

### ✅ Interpretación
Un alimento con 10g de grasa tendría aproximadamente **160 calorías**.

---

## 4️⃣ 🚗 Precio de autos eléctricos

### 🧩 Planteo
Estimar el precio de autos eléctricos según la autonomía (en km).

```python
X = [[150], [200], [250], [300], [350], [400], [450]]
y = [30, 35, 40, 50, 55, 60, 70]

model = LinearRegression().fit(X, y)
print(model.predict([[375]]))  # Resultado: 58
```

### ✅ Interpretación
Un auto eléctrico con 375 km de autonomía costaría aproximadamente **58 mil USD**.

---

## 5️⃣ 🎬 Duración vs. puntuación de películas

### 🧩 Planteo
Ver si existe una relación entre la duración de una película y su puntuación en un sitio web.

```python
X = [[80], [90], [100], [110], [120], [130], [140]]
y = [5.5, 6.0, 6.5, 7.0, 7.2, 7.5, 7.8]

model = LinearRegression().fit(X, y)
print(model.predict([[125]]))  # Resultado: 7.3
```

### ✅ Interpretación
Una película de 125 minutos tendría una puntuación estimada de **7.3 puntos**.

---

## 📌 Conclusión

Estos ejemplos muestran cómo resolver problemas reales con datos simples usando Scikit-learn.  
Son ideales para aprender los conceptos básicos de Machine Learning en un contexto cotidiano.
