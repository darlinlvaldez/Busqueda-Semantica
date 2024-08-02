
# **Proyecto Final: Sistema de Búsqueda Semántica para Artículos Científicos.**


## 🔗 Link del notebook en colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1NR6yesi0TjannGC1pc0dfBu4CYdvhTBU?usp=sharing)



**Descripción:**

Este proyecto implementa un sistema de búsqueda semántica utilizando embeddings generados con el modelo BERT de Transformers. El flujo de trabajo abarca la carga, procesamiento, generación de embeddings, visualización y evaluación de un sistema de búsqueda basado en texto. 


## Componentes del Proyecto.

**1. Generación de Embeddings:**
Utiliza el modelo BERT para convertir texto en representaciones vectoriales semánticas.

**2. Procesamiento de Datos:**
Lee grandes archivos JSON, normaliza y limpia el texto para el análisis.

**3. Validación de Embeddings:**
Verifica la validez y dimensionalidad de los embeddings generados.

**4. Visualización:**
Proporciona visualizaciones en 2D y 3D utilizando PCA para explorar los embeddings y las consultas.

**5. Evaluación de Búsqueda:**
Calcula métricas de precisión, recall y F1-score para evaluar el rendimiento del sistema de búsqueda.


## Instalación

**Para instalar las dependencias del proyecto, asegúrate de tener pip instalado y ejecuta:**

```bash
  pip install transformers torch numpy pandas matplotlib seaborn scikit-learn kaggle
```
    
**Subir el archivo.json descargado desde kaggle.**
```bash
from google.colab import files
files.upload()
```

**Crear el directorio .kaggle si no existe**

```bash
!mkdir -p ~/.kaggle
```

**Mover kaggle.json al directorio .kaggle**

```bash
!cp kaggle.json ~/.kaggle/
```

**Configurar permisos para que solo el usuario pueda leer y escribir el archivo**

```bash
!chmod 600 ~/.kaggle/kaggle.json
```

**Descargar el dataset de arXiv desde Kaggle**

```bash
!kaggle datasets download -d Cornell-University/arxiv
```


**Descomprimir el archivo descargado**

```bash
!unzip arxiv.zip -d arxiv_data
```


## Uso
**Preparación de Datos:**

- Coloca el archivo JSON de datos en la ruta adecuada.

- Usa data_processing.py para cargar y procesar los datos.

**Generación de Embeddings:**

Ejecuta embedding_generation.py para generar embeddings a partir del texto procesado.

**Visualización:**

Utiliza visualization.py para crear gráficos 2D y 3D de los embeddings.

**Evaluación:**

Corre evaluation.py para calcular y mostrar las métricas de evaluación.


### Ejemplo:

```bash
# Ejecutar el procesamiento y generación de embeddings
python data_processing.py
python embedding_generation.py

# Visualizar embeddings
python visualization.py

# Evaluar el sistema de búsqueda
python evaluation.py
```


## Archivos Incluidos

**data_processing.py:** 
Scripts para la carga y limpieza de datos.

**embedding_generation.py:** 
Funciones para generar embeddings utilizando BERT.

**visualization.py:** 
Código para visualizar embeddings en 2D y 3D.

**evaluation.py:** 
Scripts para calcular y mostrar métricas de evaluación.


## Requisitos.

transformers.

torch.

numpy.

pandas.

matplotlib.

seaborn.

scikit-learn.


## **¡IMPORTANTE!**

**Necesitaras una cuenta en Kaggle para descargar el dataset.**

**Usar Google Colab con python.**


## Conclusión:

Este proyecto ha logrado implementar un sistema de búsqueda semántica utilizando embeddings generados por el modelo BERT de transformers. A través de una serie de pasos bien estructurados, se ha demostrado la capacidad de procesar un gran conjunto de datos, limpiar y normalizar textos, generar embeddings de alta calidad, y finalmente, visualizar los resultados en un espacio reducido usando PCA.

