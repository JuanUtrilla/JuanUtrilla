## Hola, soy Juan Peñas Utrilla

**Machine Learning Engineer** en Madrid. Físico de formación, con un máster en Big Data,
Data Science e Inteligencia Artificial por la Universidad Complutense.

Lo que me interesa es la parte que casi nadie enseña: **qué pasa después de entrenar el
modelo**. Optimizarlo para inferencia, servirlo tras una API, dejarlo monitorizado y saber
—con evidencia, no con intuición— si de verdad mejora al *baseline*.

---

### En lo que trabajo ahora

**[MyTiquet](https://mytiquet.es)** · proyecto cofundado · *visión por computador + NLP*

Digitalización automática de tickets de compra, en explotación con usuarios reales.
Pipeline completo: puerta de calidad y regresor de esquinas para el recorte perspectivo,
detección y reconocimiento de texto en GPU, *parsers* por enseña y clasificación de
productos con BETO. Datalake propio con arquitectura *medallion* y revisión humana para
generar *ground truth* de reentrenamiento.

Lo que más me ha enseñado no es el modelo, son dos decisiones de diseño: que las ramas de
rescate solo se adopten **si mejoran una métrica de calidad explícita** —de forma que una
mejora nunca pueda romper lo que ya funcionaba— y que optimizar la inferencia consiste
sobre todo en **medir y descartar**: la mitad de las cuantizaciones que probé salían más
lentas que el modelo original.

**Sistema de riesgo de incendio forestal** · *ML en producción*

Modelo XGBoost sobre un dataset propio de 76.666 muestras que **bate al índice FWI oficial**
(0,843 frente a 0,488 de AUC-PR), con validación cruzada espacial y cuatro validaciones
externas independientes. Se ejecuta cada mañana: descarga la observación de ~700 estaciones,
interpola a una malla nacional de 1 km y publica el ranking de riesgo, orquestado con GitHub
Actions y con las previsiones **selladas por commit** para que no quepa reajustar a
posteriori.

La parte de la que estoy más satisfecho es incómoda: una de esas validaciones externas
demostró que **mis propias métricas anteriores estaban infladas** por pseudo-replicación.
Las corregí y lo dejé documentado. Y donde el modelo *no* gana —frente a climatología y
persistencia— también está escrito.

*Ambos repositorios son privados por ahora. El del sistema de incendios se abrirá tras la
defensa, en septiembre de 2026.*

---

### Otros proyectos públicos

- [**nlp-finetuning-transformers**](https://github.com/JuanUtrilla/nlp-finetuning-transformers) —
  *Fine-tuning* de RoBERTa para *question answering* extractivo sobre SQuAD 2.0 (con
  preguntas sin respuesta) y clasificación de inferencia textual sobre MNLI.
- [**spark-nyc-taxi**](https://github.com/JuanUtrilla/spark-nyc-taxi) — Millones de
  trayectos procesados con Apache Spark y *spatial join* distribuido con Apache Sedona.
- [**churn-prediction-ml**](https://github.com/JuanUtrilla/churn-prediction-ml) — Pipeline
  de clasificación binaria de extremo a extremo, con selección del umbral de decisión en
  lugar del 0,5 por defecto.
- [**deep-learning-densas-cnn**](https://github.com/JuanUtrilla/deep-learning-densas-cnn) ·
  [**rnn-series-temporales**](https://github.com/JuanUtrilla/rnn-series-temporales) ·
  [**proyecto-modelos-lineales**](https://github.com/JuanUtrilla/proyecto-modelos-lineales) ·
  [**cardmarket_pricing_tool**](https://github.com/JuanUtrilla/cardmarket_pricing_tool)

---

### Stack

**Deep Learning** — PyTorch, Hugging Face Transformers, TensorFlow/Keras, PaddleOCR, CUDA

**Inferencia** — ONNX Runtime, cuantización fp16/int8, TensorRT

**ML clásico** — scikit-learn, XGBoost, Optuna, SHAP

**Producción** — FastAPI, Docker, Podman, GitHub Actions, Gradio

**Datos** — Python, SQL, Apache Spark, Snowflake, SQLite, Parquet

---

### Contacto

[LinkedIn](https://www.linkedin.com/in/juan-penas-utrilla/) · [jpenas.utrilla@gmail.com](mailto:jpenas.utrilla@gmail.com)
