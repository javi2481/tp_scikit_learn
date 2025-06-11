# 🔮 08 - Novedades y futuro

Scikit-learn evoluciona constantemente, incorporando mejoras y nuevas funcionalidades que lo mantienen vigente en el ecosistema de ML.

---

## 🚀 Incorporación de nuevos modelos

### 📦 HistGradientBoosting
Una implementación eficiente y rápida de Gradient Boosting basada en histogramas.

✅ Ventajas:
- Muy útil para grandes volúmenes de datos.
- Inspirado en LightGBM y XGBoost.
- Soporta variables categóricas sin codificación previa.

🔗 [Documentación oficial](https://scikit-learn.org/stable/modules/ensemble.html#histogram-based-gradient-boosting)

---

## 🧠 Mejor integración con Pandas

- Conservación de nombres de columnas al usar transformadores.
- Métodos como `.get_feature_names_out()` ahora respetan los `DataFrames`.

Esto mejora la **interpretabilidad** y facilita el debugging.

---

## 📊 Nuevas herramientas de validación

- `HalvingGridSearchCV` y `HalvingRandomSearchCV`: búsqueda de hiperparámetros más rápida y eficiente.
- Compatibles con procesamiento paralelo y menor uso de memoria.

---

## ⚙️ Tendencias y mejoras en desarrollo

🔧 En el roadmap del proyecto:

- Mejor soporte para datos tabulares complejos.
- Integración con AutoML (Auto-sklearn).
- Compatibilidad con entornos distribuidos (como Dask).
- Herramientas para interpretación como SHAP y Feature Importance.

🔗 [Scikit-learn GitHub - Issues y roadmap](https://github.com/scikit-learn/scikit-learn/issues)

---

## 🗓️ Frecuencia de actualizaciones

Desde 2020, se publica una nueva versión cada ~3 meses.  
Cada release incluye:

- Nuevas funciones
- Deprecaciones claras
- Correcciones de bugs
- Documentación ampliada

---

## ✅ Conclusión

Scikit-learn no se detiene. Su evolución apunta a mayor eficiencia, integración con herramientas modernas y facilidad de uso para usuarios nuevos y expertos.

📌 ¡Vale la pena mantenerse al día con sus versiones!
