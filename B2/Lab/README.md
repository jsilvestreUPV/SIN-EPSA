# Práctica 2: entrenamiento y evaluación de clasificadores

En esta práctica aprenderemos a construir sistemas de clasificación para diferentes tareas y datasets.

## Datasets y tareas:
- [Iris](P2.S1%20Entorno%20de%20trabajo%20+%20datasets/01_iris.ipynb): clasificación de flores de la familia Iris a partir de características extraídas por expertos.
- [Digits](P2.S1%20Entorno%20de%20trabajo%20+%20datasets/02_digits.ipynb): clasificación de dígitos manuscritos a partir de imágenes.
- [Olivetti](P2.S1%20Entorno%20de%20trabajo%20+%20datasets/03_olivetti.ipynb): clasificación de caras a partir de imágenes.
- [OpenML](P2.S1%20Entorno%20de%20trabajo%20+%20datasets/04_openml.ipynb): repositorio abierto de datasets y tareas de clasificación.

## Técnicas de clasificación:
- [Perceptrón](P2.S2%20Perceptrón/)
- [Regresión logística](P2.S3%20Regresión%20Logística/)

## Herramientas software
- [Python3](https://www.python.org/):
  - [Seminario de Python3](https://dsic.gitbook.io/python3/) by jsilvestre.
  - Librerías:
    - [Numpy](https://numpy.org/): *The fundamental package for scientific computing with Python.*
    - [Scikit-learn](https://scikit-learn.org/): *Machine Learning in Python.*
    - [Pandas](https://pandas.pydata.org/): *Python data analysis library.*
    - [OpenML](https://www.openml.org/): *Open platform for sharing datasets, algorithms, and experiments.*
    - [Seaborn](https://seaborn.pydata.org/): *Statistical data visualization.*
    - [Matplotlib](https://matplotlib.org/): *visualization with Python.*
- [Jupyter Notebooks](https://jupyter.org/)

## Entorno de trabajo

Para la realización de la práctica, deberemos ser capaces de abrir, modificar y ejecutar los cuadernos Jupyter proporcionados, así como crear nuevos cuadernos. Para más detalles, ver las instrucciones de la [Sesión 1](P2.S1%20Entorno%20de%20trabajo%20+%20datasets/README.md).

## Planificación
- [**Sesión 1**](P2.S1%20Entorno%20de%20trabajo%20+%20datasets/): entorno de trabajo + presentación datasets.
- [**Sesión 2**](P2.S2%20Perceptrón/): construcción de clasificadores lineales basados en el algoritmo Perceptrón.
- **Sesión 3**: construcción de clasificadores de regresión logística.
- **Sesión 4**: prueba práctica de laboratorio.

## Tareas a realizar y entrega

El día de la prueba práctica de laboratorio, se entregarán 5 cuadernos Jupyter (`.ipynb`):
- **4 cuadernos** correspondientes a la construcción, desarrollo y evaluación de clasificadores {Perceptrón, Regresión Logística} para las tareas {Digits, Olivetti}.
  + Se pueden realizar individualmente o por parejas (si se hace en pareja, indicarlo en el momento de la entrega).
- **1 cuaderno** correspondiente a la construcción, desarrollo y evaluación de un clasificador de Regresión Logística para una tarea extraída del repositorio OpenML.
  + Realización individual durante la prueba práctica de laboratorio.

## Evaluación

La práctica 2 tiene una valoración máxima de 1.25 puntos:

- **0.5 puntos**: entrega y correcta realización de los 4 cuadernos Jupyter de las sesiones prácticas.
- **0.75 puntos**: evaluación competitiva de la prueba práctica de laboratorio. Se publicará una clasificación de todos los alumnos participantes, ordenados de menor a mayor tasa de error del clasificador entregado. 