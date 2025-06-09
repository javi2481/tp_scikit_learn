# 🧪 13 - Ejemplos prácticos explicados para principiantes

En esta sección, exploramos casos reales y sencillos de machine learning usando Scikit-learn.  
Cada ejemplo incluye código y una breve explicación para facilitar la comprensión.

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

📊 Visualización sugerida:  
![Gráfico aprobación examen](imagenes/aprobacion_examen.png)

---

## 2. 🏠 Estimar el precio de una casa

Regresión lineal con una sola variable.

```python
from sklearn.linear_model import LinearRegression

X = [[50], [60], [70], [80], [90]]
y = [100, 120, 140, 160, 180]

model = LinearRegression().fit(X, y)
print(model.predict([[75]]))  # Resultado: 150
```

📊  
![Gráfico precio casas](imagenes/precio_casas.png)

---

## 3. 🍔 Calorías según grasa

Relación entre gramos de grasa y cantidad de calorías.

```python
X = [[2], [5], [8], [11], [14], [17], [20]]
y = [50, 100, 140, 180, 220, 260, 300]

model = LinearRegression().fit(X, y)
print(model.predict([[10]]))  # Resultado: 160
```

📊  
![Gráfico calorías grasa](imagenes/calorias_grasa.png)

---

## 4. 🚗 Precio de autos eléctricos

Ejemplo con regresión simple.

```python
X = [[150], [200], [250], [300], [350], [400], [450]]
y = [30, 35, 40, 50, 55, 60, 70]

model = LinearRegression().fit(X, y)
print(model.predict([[375]]))  # Resultado: 58
```

📊  
![Gráfico precio autos eléctricos](imagenes/precio_autos.png)

---

## 5. 🎬 Duración vs puntuación de películas

```python
X = [[80], [90], [100], [110], [120], [130], [140]]
y = [5.5, 6.0, 6.5, 7.0, 7.2, 7.5, 7.8]

model = LinearRegression().fit(X, y)
print(model.predict([[125]]))  # Resultado: 7.3
```

📊  
![Gráfico puntuación películas](imagenes/puntuacion_peliculas.png)

---

## ✅ Conclusión

Estos ejemplos muestran cómo aplicar Scikit-learn en situaciones cotidianas y fáciles de entender.  
📌 ¡Son ideales para empezar tu camino en el machine learning!
