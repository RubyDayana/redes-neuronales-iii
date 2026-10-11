# Redes Neuronales III

Proyecto académico orientado a la implementación, optimización y evaluación de redes neuronales con **TensorFlow y Keras**. Incluye prácticas de preprocesamiento de datos, comparación de optimizadores, regularización y evaluación de modelos de clasificación binaria y multiclase.

## Información académica

- **Estudiante:** Ruby Dayana Cárdenas Gómez
- **Universidad:** Universidad de Cundinamarca
- **CADI:** Deep Learning — Conceptos
- **Docente:** Nidia Stella García Roa

## Objetivo

Aplicar técnicas que permitan mejorar el rendimiento, la estabilidad y la capacidad de generalización de modelos de Deep Learning. El proyecto estudia la relación entre hiperparámetros, optimización, regularización, distribución de los datos y métricas de evaluación.

## Contenido del repositorio

| Archivo | Práctica | Conjunto de datos |
|---|---|---|
| `01_Optimizacion_Regularizacion.ipynb` | Comparación de SGD con momentum, RMSprop y Adam; aplicación de Dropout, regularización L2 y Early Stopping | Breast Cancer Wisconsin |
| `02_Evaluacion_Multiclase.ipynb` | Clasificación multiclase, matriz de confusión, métricas macro y análisis de errores | Digits de scikit-learn |
| `Informe_Redes_Neuronales_III.docx` | Documento técnico con metodología, resultados, conclusiones y evidencias | Resultados de ambas prácticas |

## Abrir los notebooks en Google Colab

> Los siguientes botones funcionarán cuando los archivos se encuentren en la rama `main` de un repositorio llamado `redes-neuronales-iii`.

[![Abrir práctica 1 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RubyDayana/redes-neuronales-iii/blob/main/01_Optimizacion_Regularizacion.ipynb)

[![Abrir práctica 2 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RubyDayana/redes-neuronales-iii/blob/main/02_Evaluacion_Multiclase.ipynb)

También es posible descargar cada archivo `.ipynb` y abrirlo desde **Google Colab → Archivo → Subir notebook**.

## Práctica 1: optimización y regularización

Se utilizó el conjunto de datos Breast Cancer Wisconsin para construir un clasificador binario. Los datos fueron distribuidos en conjuntos de entrenamiento, desarrollo y prueba con una proporción aproximada de **70 % / 15 % / 15 %**. El escalado se ajustó únicamente con los datos de entrenamiento para evitar fuga de información.

### Comparación de optimizadores

| Optimizador | Accuracy de desarrollo | Pérdida de desarrollo |
|---|---:|---:|
| SGD con momentum | 97,65 % | 0,0421 |
| RMSprop | 97,65 % | 0,0422 |
| Adam | 97,65 % | 0,0468 |

SGD con momentum fue seleccionado por presentar la menor pérdida en el conjunto de desarrollo. Posteriormente se entrenó el modelo regularizado con **Dropout**, penalización **L2** y **Early Stopping**.

### Resultados finales

| Métrica | Resultado en prueba |
|---|---:|
| Accuracy | 96,51 % |
| Precision | 98,11 % |
| Recall | 96,30 % |
| F1 Score | 97,20 % |

Matriz de confusión obtenida: `[[31, 1], [2, 52]]`.

## Práctica 2: evaluación multiclase

Se trabajó con el conjunto Digits de scikit-learn, formado por imágenes de dígitos escritos a mano. El modelo utiliza una red neuronal multicapa con salida *softmax*, optimizador Adam, Dropout, regularización L2, Early Stopping y reducción automática de la tasa de aprendizaje.

### Resultados finales

| Métrica macro | Resultado en prueba |
|---|---:|
| Accuracy | 98,52 % |
| Precision | 98,54 % |
| Recall | 98,50 % |
| F1 Score | 98,52 % |

El modelo clasificó correctamente **266 de 270** observaciones del conjunto de prueba. La matriz de confusión y el reporte por clase se encuentran dentro del notebook.

## Técnicas aplicadas

- Separación de datos en conjuntos **train/dev/test**.
- Preprocesamiento y escalado sin fuga de información.
- Ajuste de hiperparámetros.
- Comparación de los optimizadores SGD con momentum, RMSprop y Adam.
- Regularización mediante Dropout y L2.
- Early Stopping para controlar el sobreajuste.
- Reducción de la tasa de aprendizaje.
- Evaluación con Accuracy, Precision, Recall y F1 Score.
- Matrices de confusión y análisis de errores.
- Uso de semillas aleatorias para favorecer la reproducibilidad.

## Ejecución

Los notebooks están preparados para ejecutarse en Google Colab sin necesidad de cargar conjuntos de datos externos.

1. Abra uno de los notebooks mediante su botón de Google Colab.
2. Seleccione **Entorno de ejecución → Ejecutar todas**.
3. Espere a que finalice el entrenamiento.
4. Revise las gráficas, métricas, matrices de confusión y conclusiones generadas.

Para una ejecución local se recomienda Python 3.10 o superior y las siguientes bibliotecas:

```text
tensorflow
scikit-learn
pandas
numpy
matplotlib
seaborn
```

## Estructura sugerida

```text
redes-neuronales-iii/
├── 01_Optimizacion_Regularizacion.ipynb
├── 02_Evaluacion_Multiclase.ipynb
├── Informe_Redes_Neuronales_III.docx
└── README.md
```

## Trabajos anteriores

- [Redes neuronales básicas](https://github.com/RubyDayana/redes-neuronales-basicas)
- [Redes Neuronales II](https://github.com/RubyDayana/redes-neuronales-ii)

## Autora

**Ruby Dayana Cárdenas Gómez**  
Universidad de Cundinamarca
