# Práctica 2 - Sesión 3: Regresión logística

## Descripción

En la tercera sesión aplicaremos [regresión logística](../../Teo/T3:%20Aprendizaje%20Supervisado:%20regresión%20logística/T3.4a%20Regresión%20Logística.ipynb) a diferentes tareas para entrenar sistemas de clasificación automática **probabilísticos** basados en [funciones discriminantes lineales](../../Teo/T3:%20Aprendizaje%20Supervisado:%20regresión%20logística/T3.1a%20Funciones%20discriminantes.ipynb)**.

A modo de ejemplo, se proporciona un [cuaderno Jupyter](./01_iris.ipynb) que aplica regresión logística sobre la tarea la tarea de clasificación de [flores de la familia Iris](../P2.S1%20Entorno%20de%20trabajo%20+%20datasets/01_iris.ipynb) usando una [implementación proporcionada por la librería sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html).


## Actividades a realizar

1. Analizar, ejecutar y completar el [cuaderno de regresión logística aplicado al corpus Iris](./01_iris.ipynb), para obtener la menor tasa de error posible en test.
2. Extender el ejemplo anterior a otras tareas, tratando de minimizar la tasa de error en test:
    1. Tarea [Digits](../P2.S1%20Entorno%20de%20trabajo%20+%20datasets/02_digits.ipynb) (clasificación de dígitos manuscritos).
    1. Tarea [Olivetti](../P2.S1%20Entorno%20de%20trabajo%20+%20datasets/03_olivetti.ipynb) (clasificación de caras).

Nota: los conjuntos de test son de libre "confección", y por tanto, privados. Cada equipo puede decidir qué porcentaje de muestras se usa para evaluar, así como el valor de la semilla para el barajado aleatorio de los datos. Por ello, las tasas de error en test no serán comparables, a no ser, claro está, que diferentes equipos usen la misma proporción de datos de test y la misma semilla para el barajado de datos.

## Entrega

El dia de la prueba práctica de laboratorio, se deberán entregar 2 cuadernos Jupyter (ficheros `.ipynb`) correspondientes a las actividades 2.1 y 2.2 descritas en la sección anterior. 