# Optimización procesos Mecanizado
---------------------------------------
### !Bienvenidos!
En este repositorio se realizo un proyecto que busca ayudar a los talleres de mecanizado a tomar desciones para mejorar aspectos como rentabilidad, el costo real de remover material y el costo de las herramientas para realizar los procesos de mecanizado. Se encuentra respladado por una teoria robusta basada en el analísis dimensional que permite optimizar y reducir costos usando numeros admiencionales que describen las caracteristicas de la operación de mecanizado.

Este es un proyecto de libre uso, esta diseñado para que personas con poco o nulo conocimento de programación sean capaces de usarlo y implementarlo en su negocio.
## Contenido
<!-- !toc (minlevel=2 omit="Table of Contents") -->
* [Proposito](#proposito)
* [Introducción](#introducción)
* [Herramientas necesarias para correr el proyecto](#herramientas-necesarias-para-correr-el-proyecto)
   * [Anaconda](#anaconda)
   * [Python](#python)
   * [Google Colab](#google_colab)
* [¿Cual es teoria que soporta este proyecto?](#theory)
* [Toma de datos](#data_collection)
* [Carga de datos](#load_data)
    * [csv](#csv)
    * [excel](#excel)
    * [google docs](#google_docs)
* [Grafica de los indicadores](#Graph_indicators)
* [Generación de la superficie](#gen_surface)
* [Grafica de la superficie](#surf_graph)
*  [Selección de indicadores optimos](#opt_index)
*  [Optimización de procesos](#process_opt)
*  [Grafica de optimización](#graph_opt)
*  [Recursos del proyecto](#resources)

#  Proposito
La razón de realizar este proyecto es para acerca a sectores de la industria a las herramientas de desarrollo de software para la toma de decisiones en el negocio. Concretamente este tipo de proyecto es uno de Data Science, es decir, es una herramienta que permite la toma de decisiones basadas en datos. En los talleres de mecanizado se realizan multiples operaciones a diario y se necesita una herramienta que permita tomar decisiones para mejorar la rentabilidad de los procesos.

# Introducción
En este proyecto se va a implementar el analisis dimensional que permite optimizar y reducir costos usando numeros admiencionales que describen las caracteristicas de la operación de mecanizado. Esta teoría se basa en una investigación publicada en el 8° congreso iberoamericano de ingeniería mecánica realizada por un estudiante de Maestria y un profesor de la universidad de los Andes. Donde estudiaron las principales variables que influyen en la rentabilidad, costos y tiempos de los procesos de mecanizado. 
# Herramientas necesarias para correr el proyecto
Para utilizar este proyecto es necesario tener una cuenta de GitHub. Si no tiene una cuenta de GitHub puede crear una en siguiendo los pasos que describe en el siguiente enlace [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fgithub.com%2Fjoin&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk), tambien es necesario instalar git siguiendo el siguiente tutorial [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fgit-scm.com%2Fbook%2Fen%2Fv2%2FGetting-Started-Installing-Git&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk).
Una ves instalado git se debe crear una carpeta en la cual se guardaran los archivos necesarios para correr el proyecto se hace un gir fork al repositorio de este proyecto. Despues de esto se realiza un git clone del repositorio del proyecto dentro de los repositorios personales. Finalmente desde git se realiza un git clone del repositorio dentro de la carpeta que se desea guardar el proyecto.

Para correr el proyecto existe las siguientes alternativas:
* (Recomendado) Correr el proyecto usando Anaconda.
* Correr el proyecto desde python.
* Correr el proyecto desde Google Colab.
## Anaconda
Desde el siguiente link se puede descargar Anaconda y se debe instalar en el computador. [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fwww.anaconda.com%2Fdownload%2F&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk)
## Python
Desde el siguiente link se puede descargar python y se debe instalar en el computador. [Link](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwip9qCttb_0AhU3QzABHWxeD5cQFnoECAUQAQ&url=https%3A%2F%2Fwww.python.org%2Fdownloads%2F&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk)

Adicionalmente se recomienda crear un ambiente virtual de python.
Para esto se debe correr las siguientes lineas de codigo en el terminal:

Para crear un abiente  virtual.
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

