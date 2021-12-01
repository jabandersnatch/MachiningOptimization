# Optimización procesos Mecanizado
---------------------------------------
### !Bienvenidos!
En este repositorio se realizo un proyecto que busca ayudar a los talleres de mecanizado a tomar decisiones para mejorar aspectos como rentabilidad, el costo real de remover material y el costo de las herramientas para realizar los procesos de mecanizado. Se encuentra respaldado por una teoria robusta basada en el análisis dimensional que permite optimizar y reducir costos usando numeros admiencionales que describen las caracteristicas de la operación de mecanizado.

Este es un proyecto de libre uso, esta diseñado para que personas con poco o nulo conocimiento de programación sean capaces de usarlo y implementarlo en su negocio.
## Contenido
<!-- !toc (minlevel=2 omit="Table of Contents") -->
- [Proposito](#proposito)
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
- [Referencias](#referencias)

#  Proposito
La razón de realizar este proyecto es para acerca a sectores de la industria a las herramientas de desarrollo de software para la toma de decisiones en el negocio. Concretamente este tipo de proyecto es uno de Data Science, es decir, es una herramienta que permite la toma de decisiones basadas en datos. En los talleres de mecanizado se realizan multiples operaciones a diario y se necesita una herramienta que permita tomar decisiones para mejorar la rentabilidad de los procesos.

# Introducción
En este proyecto se va a implementar el analisis dimensional que permite optimizar y reducir costos usando numeros adimensionales que describen las caracteristicas de la operación de mecanizado. Esta teoría se basa en una investigación publicada en el 8° congreso iberoamericano de ingeniería mecánica realizada por un estudiante de Maestria y un profesor de la universidad de los Andes. Donde estudiaron las principales variables que influyen en la rentabilidad, costos y tiempos de los procesos de mecanizado. 
# Herramientas necesarias para correr el proyecto
Para utilizar este proyecto es necesario tener una cuenta de GitHub. Si no tiene una cuenta de GitHub puede crear una en siguiendo los pasos que describe en el siguiente enlace [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fgithub.com%2Fjoin&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk), tambien es necesario instalar git siguiendo el siguiente tutorial [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fgit-scm.com%2Fbook%2Fen%2Fv2%2FGetting-Started-Installing-Git&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk).
Una ves instalado git se debe crear una carpeta en la cual se guardaran los archivos necesarios para correr el proyecto se hace un gir fork al repositorio de este proyecto. Despues de esto se realiza un git clone del repositorio del proyecto dentro de los repositorios personales. Finalmente desde git se realiza un git clone del repositorio dentro de la carpeta que se desea guardar el proyecto.

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

De este teorema se escogio una serie de numeros adimencionales que mejor describen el comportamiento de las operaciones de mecanizado. Estos numeros se representan como $\pi_1$, $\pi_2$ y $\pi_3$.

Para establecer como se hallan estos numeros primero se tiene que presentar los datos que los componen. Los cuales se encuentran en la siguiente tabla.

|Símbolo  | Descripción                                       |
-------- | ---------------------------------------------------|
|$T_p$    | Tiempo de preparación de la máquina (s).          |
|$T_i$    | Tiempo de Improductividad (s)                     |
|$T_{cd}$ | Tiempo de carga y descarga de material (s).       |
|$T_{t}$   | Tiempo de cambio de la herramienta (s).          |
|$C_p$    | Costo de preparación de la máquina ($).           |
|$C_i$    | Costo de improductividad ($).                     |
|$C_p$    | Costo de preparación de la máquina ($).           |
|$C_f$    | Costo del fluido de corte ($).                    |
|$C_{om}$ | Costo de operacion de la máquina ($).             |
|$V_b$    | Desgaste de operación  de la máquina ($\mu m$).   |
|$A_v$    | Velocidad de avance del movimiento                |
$P_c$    | Profundidad de corte (mm)                          |
|$L_m$    | Longitud mecanizada de material (mm)              |
|$T$      | Tiempo efectivo de mecanizado (min)               |
|$V_{MR}$ | Volumen de material retirado (mm^3)               |
|$T_{OHP}$| tiempo de operación de la herramienta (s)         |
|$C_{MP}$ | Costo de materia prima ($).                       |
|$V_{MP}$ | Volumen de materia prima ($mm^3$)                 |
|$V_p$    | Valor de la producción ($).                       |
|$V_v$    | Valor de la venta ($).                            |

Para información sobre como hallar esto valores referirse a la sección de [toma de datos](#toma-de-datos). Una vez hallados los datos se procede a hallar los numeros adimencionales. 
$$V_{MR}=P_c\times L_m \times A_v \times T_{OHP}$$
$$\pi_1= \frac{\frac{C_p+C_i+C_f+C_{om}}{V_{MR}}}{\frac{C_{MP}}{V_{MP}}}$$
$$C_1=C_p+C_i+C_f+C_{om}$$
$$C_{HF}=\left(\frac{C_H\times T_{OHP}}{NF\times T_{TM}}\right)$$
$$\pi_2=\frac{\frac{C_1}{V_b}}{\frac{C_{HF}}{L_m}}$$
$$\pi_3=\frac{V_v}{V_p}$$

Estos indicadores responden a 3 preguntas:

1. ¿Cuanto cuesta retirar un $mm^3$ de material de la máquina?
2. ¿Cuanto cuesta comprar y usar una herramienta de corte?
3. ¿Cuanto es la rentabilidad de un proceso de maquinado?

Así pues $\pi_1$, $\pi_2$ y $\pi_3$ son los indicadores que nos permiten hallar los costos de operación de la máquina. Donde $\pi_1$ es el costo de producción, $\pi_2$ es el costo de herramienta y $\pi_3$ es el margen de rentabilidad.

# Toma de datos
Para hallar los datos se realizo un handbook que lo encuentran el la carpeta de documentos en el folder llamado Data Collection Guide. En este se encuentran una guía extensiva de como realizar la toma de datos, esta parte se considera una de las mas importantes para el análisis dimensional.

# Carga de datos

Para cargar los datos a la aplicación se pueden tomar 2 pasos:

* Mediante archivos de excel
* Mediante archivos csv

Los formatos se encuentran en el folder [`data\templates`](#data-templates).

## Excel

Para importar los datos desde excel es necesario que el archivo contenga una hoja llamada `Machine materials` en esta se encontrarán los nombres de los materiales de la herramienta de corte, para cada uno de estos nombres debe existir una hoja con el nombre del material. Ademas de la hoja `Machine materials` se encuentra se debe tener unas dos hojas adicionales: `Costs` y la segunda es `Time and Volume` refierase a el archivo `tooling_data_template.xlsx` en [`data\templates`](#data-templates) para ver que parametros debe tener cada hoja. Es importante que los nombres de las columnas esten bien escritos, sin espacios adicionales. No importa el orden de estas.

## CSV
Este proceso es similar al proceso de excel, pero se debe tener en cuenta que los archivos csv deben estar separados por comas. Adicionalmente en vez de tener una hoja con los nombres de los materiales se debe tener un archivo csv con los nombres del material. En la carpeta `data\templates` se encuentra el archivo `labels_temp.csv` que contiene los nombres de los materiales. Este archivo se carga en el programa y se deserializa en un `DataFrame` que se guarda en la variable `labels`. Con este `DataFrame` se accede a los datos de la columna y se carga los archivos csv que esten guardados con ese nombre.

# Referencias

RB1:DeGarmo's Materials and Processes in Manufacturing; J. T. Black,Ronald A. Kohser; Wiley; 2019; Enhanced eTex, 13th Edition; ISBN: 978-1-119-66519-9