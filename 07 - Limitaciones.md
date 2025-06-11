# ⚠️ 07 - Limitaciones

Scikit-learn es una de las bibliotecas más populares para Machine Learning en Python.  
Sin embargo, como toda herramienta, tiene sus **limitaciones**.

---

## ❌ 1. No soporta Deep Learning

Scikit-learn no está diseñado para redes neuronales profundas.  
Para eso existen bibliotecas como:

- [TensorFlow](https://www.tensorflow.org/)
- [Keras](https://keras.io/)
- [PyTorch](https://pytorch.org/)

---

## 🚫 2. No utiliza GPU

Todos los cálculos se realizan en CPU.  
Esto puede ser una desventaja frente a librerías que aceleran operaciones con GPU como:

- XGBoost (con soporte CUDA)
- LightGBM
- TensorFlow

---

## 🐘 3. Escalabilidad limitada

Scikit-learn funciona bien con datasets pequeños y medianos.  
Pero con millones de registros puede volverse ineficiente.

🔁 Alternativas para Big Data:
- [Dask-ML](https://ml.dask.org/)
- [Spark MLlib](https://spark.apache.org/mllib/)

---

## 🔧 4. No incluye AutoML nativo

No viene con AutoML “out-of-the-box”.  
Para tareas de automatización del pipeline existen herramientas como:

- [Auto-sklearn](https://automl.github.io/auto-sklearn/)
- [TPOT](http://epistasislab.github.io/tpot/)
- [H2O AutoML](https://docs.h2o.ai/h2o/latest-stable/h2o-docs/automl.html)

---

## 🧱 5. Menos personalizable en arquitectura

Scikit-learn ofrece algoritmos predefinidos con APIs simples.  
Pero no permite construir arquitecturas personalizadas como:

- Redes con múltiples salidas
- Modelos secuenciales complejos
- Procesamiento multimodal (imágenes + texto)

---

## ✅ Conclusión

Scikit-learn es ideal para tareas de ML tradicional como clasificación, regresión, clustering y reducción de dimensionalidad.  
Para casos más avanzados (deep learning, big data o autoML), puede ser necesario complementar con otras herramientas.
