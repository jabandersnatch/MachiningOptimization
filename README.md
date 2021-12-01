# Optimización procesos Mecanizado
---------------------------------------
### !Bienvenidos!
En este repositorio se realizo un proyecto que busca ayudar a los talleres de mecanizado a tomar decisiones para mejorar aspectos como rentabilidad, el costo real de remover material y el costo de las herramientas para realizar los procesos de mecanizado. Se encuentra respaldado por una teoria robusta basada en el análisis dimensional que permite optimizar y reducir costos usando numeros admiencionales que describen las caracteristicas de la operación de mecanizado.

Este es un proyecto de libre uso, esta diseñado para que personas con poco o nulo conocimiento de programación sean capaces de usarlo y implementarlo en su negocio.
## Contenido
- [Propósito](#propósito)
- [Introducción](#introducción)
- [Herramientas necesarias para correr el proyecto](#herramientas-necesarias-para-correr-el-proyecto)
  - [Anaconda](#anaconda)
  - [Python](#python)
  - [VS Code](#vs-code)
  - [Google Colab](#google-colab)
- [Teoría](#teoría)
- [Toma de datos](#toma-de-datos)
- [Carga de datos](#carga-de-datos)
  - [Excel](#excel)
  - [CSV](#csv)
- [Grafica de los indicadores](#grafica-de-los-indicadores)
- [Generación de la superficie](#generación-de-la-superficie)
- [Grafica de la superficie](#grafica-de-la-superficie)
  - [Grafica de la superficie 3D](#grafica-de-la-superficie-3d)
  - [Grafica de la superficie 3D por material](#grafica-de-la-superficie-3d-por-material)
  - [Grafica de contorno](#grafica-de-contorno)
  - [Grafica de contorno por material](#grafica-de-contorno-por-material)
- [Selección de indicadores optimos](#selección-de-indicadores-optimos)
- [Optimización de procesos](#optimización-de-procesos)
- [Grafica de optimización](#grafica-de-optimización)
- [Exportación de datos](#exportación-de-datos)
- [Consideraciones](#consideraciones)
- [Referencias](#referencias)

#  Propósito
La razón de realizar este proyecto es para acerca a sectores de la industria a las herramientas de desarrollo de software para la toma de decisiones en el negocio. Concretamente este tipo de proyecto es uno de Data Science, es decir, es una herramienta que permite la toma de decisiones basadas en datos. En los talleres de mecanizado se realizan multiples operaciones a diario y se necesita una herramienta que permita tomar decisiones para mejorar la rentabilidad de los procesos.

# Introducción
En este proyecto se va a implementar el analisis dimensional que permite optimizar y reducir costos usando numeros adimensionales que describen las caracteristicas de la operación de mecanizado. Esta teoría se basa en una investigación publicada en el 8° congreso iberoamericano de ingeniería mecánica realizada por un estudiante de Maestria y un profesor de la universidad de los Andes. Donde estudiaron las principales variables que influyen en la rentabilidad, costos y tiempos de los procesos de mecanizado. 
# Herramientas necesarias para correr el proyecto
Para utilizar este proyecto es necesario tener una cuenta de GitHub. Si no tiene una cuenta de GitHub puede crear una en siguiendo los pasos que describe en el siguiente enlace [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fgithub.com%2Fjoin&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk), tambien es necesario instalar git siguiendo el siguiente tutorial [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fgit-scm.com%2Fbook%2Fen%2Fv2%2FGetting-Started-Installing-Git&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk).
Una ves instalado git se debe crear una carpeta en la cual se guardaran los archivos necesarios para correr el proyecto se hace un gir fork al repositorio de este proyecto. Despues de esto se realiza un git clone del repositorio del proyecto dentro de los repositorios personales. Finalmente desde git se realiza un git clone del repositorio dentro de la carpeta que se desea guardar el proyecto. Puede seguir la guía de clonar un repositorio en el siguiente [Link](https://www.youtube.com/watch?v=CKcqniGu3tA)

Para correr el proyecto existe las siguientes alternativas:
* (Recomendado) Correr el proyecto usando Anaconda.
* Correr el proyecto desde python.
* Correr el proyecto desde Google Colab.
## Anaconda
Desde el siguiente link se puede descargar Anaconda y se debe instalar en el computador. [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fwww.anaconda.com%2Fdownload%2F&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk)
No es necesario ningun proceso adicional para correr el proyecto, VS Code auto detecta el entorno de Anaconda y lo corre sin problemas. Adicionalmente Anaconda viene con las librerias necesarias para correr el proyecto entre otras que pueden resultar utiles si deciden expander sobre el proyecto.
## Python
Desde el siguiente link se puede descargar python y se debe instalar en el computador. [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fwww.python.org%2Fdownloads%2F&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk)


Adicionalmente se recomienda crear un ambiente virtual de python.
Para esto se debe correr las siguientes lineas de codigo en el terminal:

Para crear un ambiente  virtual.
```
python -m venv env
```
Para activar el ambiente virtual.
```
env/bin/activate
```
Luego de esto se debe correr el siguiente comando para instalar las librerias necesarias.
```
pip install -r requirements.txt
```
## VS Code
Independientemente de la herramienta que se utilice para correr el proyecto, es necesario tener instalado Vs Code. [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fcode.visualstudio.com%2Fdownload%2F&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk). Luego instale el pulgin de python siga el video tutorial [Link](https://www.youtube.com/watch?v=-IyA_Yvs8IQ), este pulgin deberia instalar el pulgion de jupyter notebook, si no agregué este manualmente.
## Google Colab
Para usar Google Colab no necesita instalar ninguna herramienta adicional. Simplemente abra el siguiente link . [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fcolab.research.google.com%2F&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk). Copie el link de este repositorio dirijase a la pestaña de GitHub y pegue el link del repositorio en la barra de direcciones de ahi haga click al botón de busqueda y seleccione el notebook, este generara una copia del archivo. Es importante que suba los datos y tenga en cuenta el camino relativo de la carpeta donde se encuentra el notebook.

# Teoría
Este proyecto se basa en la teoría de el análisis dimensional. Concretamente se implementa en teorema pi de Vaschy - Buckingham. Este teorema dicta que si existe un sistema de n ecuaciones que describa los comportamientos de la masa, tiempo y longitud con k constantes, entonces existe una ecuación compuesta de numeros adminecionales que tambien cumpla con las mismas condiciones.

De este teorema se escogio una serie de numeros adimencionales que mejor describen el comportamiento de las operaciones de mecanizado. Estos numeros se representan como pi_1, pi_2$ y pi_3.

Para establecer como se hallan estos numeros primero se tiene que presentar los datos que los componen. Los cuales se encuentran en la siguiente tabla.

|Símbolo  | Descripción                                       |
--------  | --------------------------------------------------|
|T_p      | Tiempo de preparación de la máquina (s).          |
|T_i      | Tiempo de Improductividad (s)                     |
|T_cd     | Tiempo de carga y descarga de material (s).       |
| T_t     | Tiempo de cambio de la herramienta (s).           |
|C_p      | Costo de preparación de la máquina ($).           |
|C_p      | Costo de preparación de la máquina ($).           |
|C_f      | Costo del fluido de corte ($).                    |
|C_om     | Costo de operacion de la máquina ($).             |
|V_b      | Desgaste de operación  de la máquina ($\mu m$).   |
|A_v      | Velocidad de avance del movimiento                |
|P_c      | Profundidad de corte (mm)                         |
|L_m      | Longitud mecanizada de material (mm)              |
|T        | Tiempo efectivo de mecanizado (min)               |
|V_MR     | Volumen de material retirado (mm^3)               |
|T_OHP    | tiempo de operación de la herramienta (s)         |
|C_MP     | Costo de materia prima ($).                       |
|V_MP     | Volumen de materia prima ($mm^3$)                 |
|V_p      | Valor de la producción ($).                       |
|V_v      | Valor de la venta ($).                            |

Para información sobre como hallar esto valores referirse a la sección de [toma de datos](#toma-de-datos). Una vez hallados los datos se procede a hallar los numeros adimencionales. 

<img src="https://render.githubusercontent.com/render/math?math=\pi_1= \frac{\frac{C_p+C_i+C_f+C_{om}}{V_{MR}}}{\frac{C_{MP}}{V_{MP}}}">

<img src="https://render.githubusercontent.com/render/math?math=V_{MR}=P_c\times L_m \times A_v \times T_{OHP}">

<img src="https://render.githubusercontent.com/render/math?math=C_1=C_p \oplus C_i \oplus C_f \oplus C_{om}">

<img src="https://render.githubusercontent.com/render/math?math=C_{HF}=\left(\frac{C_H\times T_{OHP}}{NF\times T_{TM}}\right)">

<img src="https://render.githubusercontent.com/render/math?math=\pi_2=\frac{\frac{C_1}{V_b}}{\frac{C_{HF}}{L_m}}">


<img src="https://render.githubusercontent.com/render/math?math=\pi_3=\frac{V_v}{V_p}">





Estos indicadores responden a 3 preguntas:

1. ¿Cuanto cuesta retirar un $mm^3$ de material de la máquina?
2. ¿Cuanto cuesta comprar y usar una herramienta de corte?
3. ¿Cuanto es la rentabilidad de un proceso de maquinado?

Así pues pi_1, pi_2 y pi_3 son los indicadores que nos permiten hallar los costos de operación de la máquina. Donde pi_1 es el costo de producción, pi_2 es el costo de herramienta y pi_3 es el margen de rentabilidad.

# Toma de datos
Para hallar los datos se realizo un handbook que lo encuentran el la carpeta de documentos en el folder llamado Data Collection Guide. En este se encuentran una guía extensiva de como realizar la toma de datos, esta parte se considera una de las mas importantes para el análisis dimensional.

# Carga de datos

Para cargar los datos a la aplicación se pueden tomar 2 pasos:

* Mediante archivos de excel
* Mediante archivos csv

Los formatos se encuentran en el folder [`data\templates`](#data-templates).

Se recomienda subir los datos en la carpeta `data` para que sean leidos por la aplicación. para esto tendra que modificar la variable `path` en el notebook del repositorio, notese que solo necesita colocar la ruta relativa, por ejemplo el repositorio por defecto tiene el `path=./data/example_data/` y para cargar los datos se debe colocar `path=./data/`

## Excel

Para importar los datos desde excel es necesario que el archivo contenga una hoja llamada `Machine materials` en esta se encontrarán los nombres de los materiales de la herramienta de corte, para cada uno de estos nombres debe existir una hoja con el nombre del material. Ademas de la hoja `Machine materials` se encuentra se debe tener unas dos hojas adicionales: `Costs` y la segunda es `Time and Volume` refierase a el archivo `tooling_data_template.xlsx` en [`data\templates`](#data-templates) para ver que parametros debe tener cada hoja. Es importante que los nombres de las columnas esten bien escritos, sin espacios adicionales. No importa el orden de estas.

## CSV
Este proceso es similar al proceso de excel, pero se debe tener en cuenta que los archivos csv deben estar separados por comas. Adicionalmente en vez de tener una hoja con los nombres de los materiales se debe tener un archivo csv con los nombres del material. En la carpeta `data\templates` se encuentra el archivo `labels_temp.csv` que contiene los nombres de los materiales. Este archivo se carga en el programa y se deserializa en un `DataFrame` que se guarda en la variable `labels`. Con este `DataFrame` se accede a los datos de la columna y se carga los archivos csv que esten guardados con ese nombre.

# Grafica de los indicadores

En esta parte el nootebook realiza una grafica 3D de los indicadores adimencionales. Se marca de un color distinto cada uno de los materiales. Aca su labor es revisar que los indicadores sean los correctos, usualmente se evidencia que la escala de Pi_1 se encuentra en 10^2, mientras que Pi_2 se encuentra en 10^3, finalmente Pi_3 se encuentra en rangos de 0.7 a 3,4. En dado caso que los indicadores no sean los correctos se debe revisar que los datos sean correctos.

# Generación de la superficie

Para la generación de la superficie de mejor ajuste se utilizó la herramienta `scipy.optimize.curve_fit` que permite hallar la función que mejor se ajusta a los datos. Para esto se ingreso una función general de la forma **A*x^b*y^c + d*x^(b+1)*y^(c+1)** lo que hace esta función es iterar con los parametros **a,b,c,d** y hallar la curva que menor error cuadratico tenga. Si la superficie presenta errores altos es recomendable cambiar la función general por **A*x^b*y^c** esta función presentara un comportamiento adecuando pero no tan descriptivo como la anterior. Es un proceso iterativo, la función en si no representa ningun comportamiento real de los indicadores es simplemte una relacion que se evidencio para el caso del taller en donde se tomaron los datos.

# Grafica de la superficie

En esta seccion se va a graficar  la superficie de mejor ajuste en conjunto a una grafica de dispersión de los datos. Para esto se utilizo la libreria `matplotlib.pyplot` y la funcion `scipy.optimize.curve_fit` para hallar la superficie de mejor ajuste. Se empleo un mapa de calor para hacer mas evidente los altos y los bajos de la superficie.

En esta sección se grafica 4 tipos de graficas:
## Grafica de la superficie 3D
La primera grafica es la superficie de mejor ajuste, con dispersion de los datos en 3D. Esta grafica no hace la distición del material de la herramienta. Sirve para revisar que el comportamiento de la superficie sea adecuado. Al decir adecuado se refiere a que la superficie no presente errores altos y el comportamiento sea concorde a lo que representa los numeros adimencionales.
## Grafica de la superficie 3D por material
Es similar a la primera grafica, pero se hace la distinción de los materiales. Sirve para revisar a nivel global la distribución de los datos con respecto al material.
## Grafica de contorno
Se grafica la superficie de mejor ajuste, pero con una distribución de los datos en 2D. Esta grafica sirve para revisar el comportamiento de la superficie en el plano xy. Con esta se puede apreciar que las curvas de nivel son la rentabilidad de la operación de maquinado. Con esta se puede apreciar la distribución general de los indicadores en el plano xy.
## Grafica de contorno por material
Se grafica la superficie de mejor ajuste, pero con una distribución de los datos en 2D. Esta grafica sirve para revisar el comportamiento de la superficie en el plano xy. Con esta se puede apreciar la distribución de los indicadores en el plano xy. El sección de [Optimización de procesos](#optimizacion-de-procesos) esta grafica se implementa para revisar cual es el mejor material para la herramienta de corte.
# Selección de indicadores optimos
En esta parte el usuario escoge los indicadores que sean los mejores para la herramienta de corte. Uno de los indicadores mas útiles para optimizar es el de la rentabilidad de la operación de maquinado (Pi_3). Para esto  se realiza una función que unicamente colorea las curvas de nivel que esten por encima del indicador Pi_3 dado por el usuario. La razón por la cual se implemento esta función es que el usuario puede decidir que tan alta debe ser el indicador Pi_3 para que la herramienta de corte sea optima. Esto evita colocar condiciones que sean imposibles de cumplir.

# Optimización de procesos
En esta parte usando las ecuaciones planteadas en el la parte de [Teoria](#teoria) se implementa el algoritmo de optimización de procesos. Para esto se utiliza la libreria `scipy.optimize.fsolve`. Se puede resolver para multiples condiciones lo importante a tener en cuenta es que es un sistema de ecuaciones 2x2 , asi que solo puede haber un maximo de 2 incognitas, `fsolve` permite resolver ecuaciones no lieales entre otras. Potencialmente usando el indicador Pi_3 se podria expandir el sistema de ecuaciones a 3x3, pero no es necesario. En este codigo se esta optimizado para `V_b` que es el desgaste y `T_POH` que es el tiempo de operación de la herramienta de corte. En dado caso para resolver usando los otros parametros de la herramienta de corte se debe modificar el codigo. En este debe proveer todos los parametros que no se van hallar y cambiar en el metodo `optimal_cost` sus respectivos lambdas donde se coloca el nombre de la variable que se quiera optimizar. Es importante tener en cuenta las dimensiones y el significado de cada variable, si su optimizacion le da un valor negativo juegue con los demas parametros cosa de que le de una solución optima y real.

# Grafica de optimización

En esta seccion se realiza una grafica de barras para evidenciar los cambios significativos de los parametros optimos con respecto a los evidenciados en la toma de datos.
# Exportación de datos
Para la exportacíon de datos simplemente corra el codigo, este lo ayudara a exportar los datos a un excel o a un csv. Aca se añaden las columans Pi 1, Pi 2 y Pi 3. 
# Consideraciones

Esta es una herramienta que asiste a las tomas de decisiones de la empresa, no es un remplazo a tecnicas como flujos de caja libre, intuición de procedimientos, etc. Simplemente es una herramienta mas que busca concienciar de la importacia de la reducción de costos y de la mejora de la calidad de la herramienta de corte. El objetivo es acercar a esta industria de la manufactura a soluciones TI. 
# Referencias



[1] 	J. Grueso, «DESARROLLO DE UNA METODOLOGÍA PARA LA EVALUACIÓN TÉCNICO-ECONÓMICA DEL DESEMPEÑO DE HERRAMIENTAS DE CORTE APOYADO EN EL ANÁLISIS DIMENSIONAL.,» 8º CONGRESO IBEROAMERICANO DE INGENIERIA MECANICA, p. 9, 2007. 

[2] 	V. P. Astakhov, «The assessment of cutting tool wear,» International journal of machine tools & manufacture , design research and application, vol. 44, nº 2004, p. 11, 2003. 

[3]     DeGarmo's Materials and Processes in Manufacturing; J. T. Black,Ronald A. Kohser; Wiley; 2019; Enhanced eTex, 13th Edition; ISBN: 978-1-119-66519-9D
