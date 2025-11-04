# Práctica 2 - Sesión 1: entorno de trabajo y datasets

En la primera sesión nos familiarizaremos con el [entorno de trabajo](#entorno-de-trabajo) y algunos
[conjuntos de datos](#datasets).

# Entorno de trabajo

Para la realización de la práctica, deberemos ser capaces de abrir, modificar y ejecutar los cuadernos Jupyter proporcionados, así como crear nuevos cuadernos. Para ello tenemos tres opciones:

- [Opción a): Google Colab](#opción-a-google-colab)
- [Opción b): Jupyter Notebook en Polilabs](#opción-b-jupyter-notebook-en-polilabs)
- [Opción c): Jupyter Notebook en vuestros PCs](#opción-c-instalación-local-de-jupyter-en-vuestros-pcs-con-kernel-python-propio)


## Opción a): Google Colab

La opción más sencilla y rápida pasa por usar Google Colab. Necesitaréis una cuenta de Google y acceso a internet permanente (lo cual puede ser un inconveniente; ver opción c).

Para abrir los cuadernos de esta práctica:

1. Accede a [Google Colab](https://colab.research.google.com/).
1. Ve a *"Archivo" > "Abrir cuaderno" > "GitHub"*.
1. Escribe el usuario *jsilvestreUPV* y selecciona el repositorio *SIN-EPSA*, o bien introduce directamente la URL de este repositorio: 
    https://github.com/jsilvestreUPV/SIN-EPSA
1. Haz click sobre el cuaderno que quieras abrir en Colab.

Una vez abierto, podrás realizar modificaciones sobre el cuaderno, pero no podrás guardarlas. Si deseas guardar dichas modificaciones, deberás crear una copia local en tu cuenta de Google Drive. Para ello, ve a *"Archivo" > "Guardar una copia en Drive"*. Dicho notebook se almacenará en la carpeta *"Colab Notebooks"* de tu unidad de Google Drive.

## Opción b): Jupyter Notebook en Polilabs

Debéis acceder al escritorio LINUX de los PCs del laboratorio del DSIC, o bien al escritorio DSIC-LINUX de [Polilabs](https://polilabs.upv.es/) si os conectáis desde casa. 

Una vez estéis dentro del escritorio de Ubuntu Mate:

1. Abrir una terminal: 
    + *"Menú" > "Herramientas del Sistema" > "Terminal de Mate"*.
1. Situarse en el directorio W:
    + `cd $HOME/W`
1. Clonar el repositorio git de la asignatura:
    + `git clone https://github.com/jsilvestreUPV/SIN-EPSA.git`
1. Ir al directorio de la práctica 2:
    + `cd SIN-EPSA/B2/Lab`
1. Ejecutar Jupyter:
    + `jupyter notebook`

### "Workaround" para la primera sesión

En la primera sesión (y solo en la primera) haremos uso de la librería `seaborn` de Python, la cual no está instalada en el kernel que usa Jupyter por defecto. Para solucionarlo, seguid estos pasos:

1. Abrir una terminal.
2. Instalar/actualizar el paquete `seaborn` con `pip`:
    + `pip3 install seaborn --upgrade`
3. Lanzar Jupyter desde la misma terminal:
    + `jupyter notebook`

Nota: este "hack" solo perdurará mientras vuestra sesión en polilabsVPN esté activa. 

Como alternativa a este "workaround", podéis optar por [construiros vuestro propio kernel de Python](#construir-un-kernel-python-propio).

### Construir un kernel de Python propio

Si queréis usar el escritorio DSIC-LINUX de Polilabs y al mismo tiempo tener un mayor control sobre el entorno de trabajo, podéis seguir las instrucciones de la [Opción  c) para una instalación local](#opción-c-instalación-local-de-jupyter-en-vuestros-pcs-con-kernel-propio). Esto os permitirá ejecutar la versión más reciente de Jupyter y usar un kernel propio, en lugar del kernel que se os proporciona por defecto. Solo tenéis que tener la precaución de instalar el entorno virtual dentro de vuestro directorio `W`.

## Opción c): Instalación local de Jupyter en vuestros PCs con kernel Python propio

La tercera opción, recomendable para aquellos usuarios que quieran tener el control absoluto del entorno, es realizar una instalación local de Jupyter Notebook, y de un kernel Python3 propio que reúna todas las dependencias.

A continuación se proporcionan instrucciones para sistemas operativos GNU/Linux basados en Debian. Si usas otra distribución (p.e. Fedora) o sistema operativo (p.e. Windows, MacOS), deberás adaptar los pasos 0a y 0b (el resto de pasos deberían ser idénticos). 

### 0a. Instalar Python3 y pip

Si no tienes instalado `python3` y `pip3` en tu sistema, abre una terminal y ejecuta:

`sudo apt update && sudo apt install python3 python3-pip`

### 0b. Instalar virtualenv

A continuación, instalaremos el módulo de terceros [`virtualenv`](https://pypi.org/project/virtualenv/) con `pip` para poder crear entornos virtuales.

`pip3 install virtualenv`

### 1. Crear un entorno virtual de python

Crearemos un entorno virtual de Python3 para instalar los paquetes necesarios para la práctica 2. Este entorno lo integraremos como un nuevo kernel en Jupyter.

En la misma terminal, sitúate en un directorio donde quieras que se guarde el entorno virtual, y ejecuta:

  `python3 -m virtualenv sin-venv` 

Esto creará la carpeta `sin-venv` en el directorio de trabajo actual. 

Uso del entorno:

- Para activar el entorno virtual en la terminal actual:

  `source sin-venv/bin/activate`

- Para desactivar el entorno virtual, simplemente:

  `deactivate`


### 2. Instalar Jupyter Notebook + dependencias

Con el entorno virtual activado en la terminal, ejecutar:

`pip3 install notebook ipykernel scikit-learn pandas seaborn openml numpy matplotlib`

### 3. Registrar el entorno virtual como kernel en Jupyter Notebook

Con el entorno virtual activado en la terminal, ejecutar:

`python3 -m ipykernel install --user --name sin-venv`

Para comprobar que todo ha ido bien, puedes examinar el contenido del fichero `kernel.json`:

`cat $HOME/.local/share/jupyter/kernels/sin-venv/kernel.json`

Además, si quieres, puedes listar los kernels disponibles:

`jupyter kernelspec list`

Y, si necesitas desinstalar el kernel:

`jupyter kernelspec uninstall sin-venv`

### 4. Lanzar Jupyter Notebook y seleccionar el nuevo kernel

Lanza jupyter notebook, abre un cuaderno, y ve a *"Kernel" > "Change kernel"* para cambiar el kernel, seleccionando el nuevo `sin-venv` (marca el checkbox para que se establezca como kernel por defecto).

# Datasets

Estos son los datasets con los que trabajaremos en la práctica 2:

- [Iris](01_iris.ipynb): clasificación de flores de la familia Iris a partir de características extraídas por expertos.
- [Digits](02_digits.ipynb): clasificación de dígitos manuscritos a partir de imágenes.
- [Olivetti](03_olivetti.ipynb): clasificación de caras a partir de imágenes.
- [Repositorio OpenML](04_openml.ipynb): repositorio abierto de datasets y tareas de clasificación.