# 🧪 10 - Ejemplos prácticos explicados para principiantes

Exploramos casos sencillos y cotidianos con Scikit-learn.  
Cada ejemplo incluye código, contexto y una breve explicación.

---

## 1. 🎓 ¿Aprobará el examen?

Clasificación binaria con regresión logística.

```python
from sklearn.linear_model import LogisticRegression

X = [[1], [2], [3], [4], [5], [6], [7]]
y = [0, 0, 0, 1, 1, 1, 1]

model = LogisticRegression().fit(X, y)
print(model.predict([[3.5]]))  # Resultado: [1]
```

---

## 2. 🏠 Estimar el precio de una casa

Regresión lineal con una variable.

```python
from sklearn.linear_model import LinearRegression

X = [[50], [60], [70], [80], [90]]
y = [100, 120, 140, 160, 180]

model = LinearRegression().fit(X, y)
print(model.predict([[75]]))  # Resultado: 150
```

---

## 3. 🍔 Calorías según grasa

Regresión para estimar calorías a partir de grasa.

```python
X = [[2], [5], [8], [11], [14], [17], [20]]
y = [50, 100, 140, 180, 220, 260, 300]

model = LinearRegression().fit(X, y)
print(model.predict([[10]]))  # Resultado: 160
```

---

## 4. 🚗 Precio de autos eléctricos

```python
X = [[150], [200], [250], [300], [350], [400], [450]]
y = [30, 35, 40, 50, 55, 60, 70]

model = LinearRegression().fit(X, y)
print(model.predict([[375]]))  # Resultado: 58
```

---

## 5. 🎬 Duración vs puntuación de películas

```python
X = [[80], [90], [100], [110], [120], [130], [140]]
y = [5.5, 6.0, 6.5, 7.0, 7.2, 7.5, 7.8]

model = LinearRegression().fit(X, y)
print(model.predict([[125]]))  # Resultado: 7.3
```

---

## ✅ Conclusión

Estos ejemplos muestran cómo Scikit-learn puede aplicarse en situaciones reales y accesibles.  
📌 Son ideales para empezar el camino en el machine learning sin complejidad innecesaria.
