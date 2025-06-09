# ⚖️ 04 - Comparación con otros frameworks

## 🧠 ¿Por qué comparar?

En el ecosistema de Machine Learning, existen varias bibliotecas con enfoques distintos. Scikit-learn es ideal para ML clásico, pero ¿cómo se compara con otras alternativas como TensorFlow o XGBoost?

---

## 🔍 Comparativa general

| Característica              | Scikit-learn ✅        | TensorFlow 🔵        | XGBoost 🌲           |
|-----------------------------|------------------------|-----------------------|----------------------|
| Deep Learning               | ❌ No soportado         | ✅ Sí                 | ❌ Limitado          |
| Modelos tradicionales       | ✅ Fuerte               | ❌ Poca prioridad     | ✅ Sí, pero enfocados |
| Curva de aprendizaje        | 🟢 Baja (fácil de usar) | 🔴 Alta (más compleja)| 🟡 Media             |
| Interpretabilidad           | ✅ Alta                 | ⚠️ Media-baja         | ⚠️ Media             |
| Velocidad (entrenamiento)  | 🟡 Aceptable            | ⚡ Muy rápida (GPU)   | ⚡ Muy rápida (CPU+GPU) |
| Comunidad                   | 🌍 Amplia               | 🌐 Enorme             | 📈 En crecimiento    |
| Producción (ML clásico)     | ✅ Ideal                | ⚠️ Exceso de complejidad| ✅ Muy usado        |

---

## 🔬 ¿Cuándo usar Scikit-learn?

✅ Casos ideales:
- Educación y formación en ML 🧑‍🏫  
- Prototipado rápido de modelos  
- Modelos interpretables para negocios  
- Proyectos con datasets medianos  
- Problemas de clasificación/regresión/tablas estructuradas

---

## ❌ ¿Cuándo NO usar Scikit-learn?

⚠️ Escenarios donde otras herramientas brillan:

- Deep Learning (visión, audio, texto largo): usar TensorFlow/Keras o PyTorch  
- Entrenamiento distribuido masivo (big data): usar Spark ML, Dask-ML  
- Búsqueda automática de modelos (AutoML): usar Auto-sklearn, H2O, TPOT

---

## 🔗 Enlaces útiles

- [Comparación de herramientas en GitHub (discusión)](https://github.com/scikit-learn/scikit-learn/issues/9900)
- [Documentación oficial de XGBoost](https://xgboost.readthedocs.io/)
- [TensorFlow vs Scikit-learn – Towards Data Science](https://towardsdatascience.com/tensorflow-vs-scikit-learn-1d3b4912ad8b)

---

## ✅ Conclusión

Scikit-learn brilla en tareas clásicas de machine learning. Es simple, robusto y ampliamente adoptado.  
Para proyectos más complejos, existen opciones complementarias y especializadas que se pueden integrar.
