---
title: 'Instalación del Anaconda *Navigator*'
date: 2022-06-07
permalink: /posts/2022/02/blog-post/
tags:
  - Lenguajes de Programación
  - IDE
  - Python
  - R
  - Julia
---
<img src = "\files\svg\anaconda.svg" alt="Anaconda. " width="50px" height="25px"/> - En este *post* explicaré cómo instalar el Anaconda *Navigator* en Windows y cómo establecer un ambiente de trabajo (*Environment*) y un ***Jupyter notebook*** basado en **Python**, **R** y **Julia**.



- [Instalación del Anaconda *Navigator* y creación de ambientes (*Environment*) de trabajo.](#instalación-del-anaconda-navigator-y-creación-de-ambientes-environment-de-trabajo)
  - [¿Qué es Anaconda?.](#qué-es-anaconda)
  - [¿Qué es Anaconda *Navigator*?](#qué-es-anaconda-navigator)
  - [¿Cómo instalar Anaconda *Navigator*?](#cómo-instalar-anaconda-navigator)
  - [Problemas con la instalación.](#problemas-con-la-instalación)
  - [Creando ambientes de trabajo (*Environments*).](#creando-ambientes-de-trabajo-environments)
    - [Julia](#julia)
    - [R](#r)


# Instalación del Anaconda *Navigator* y creación de ambientes (*Environment*) de trabajo.

## ¿Qué es Anaconda?.
Anaconda es una distribución de los lenguajes de programación Python, R, Julia y otros, que tiene multiples usos, desde la ciencia de datos hasta los análisis predictivos y los análisis científicos. Su principal objetivo es el manejo de paquetes y su despliegue de una manera centralizada. Esta distribución es ejecutable en las plataformas Windows, Linux y MacOS.


La distribución de Anaconda viene con más de 250 paquetes de análisis y se pueden instalar más de 7000 adicionales, los cuales son completamente *Open-Source*. Todos los paquetes pueden instalarse con el *Python Package Index* a través del  Instalador de Paquetes para Python *PIP* (*Package Intaller for Python*) como también con el administrador de paquetes *conda*. La principal diferencia entre ambos adiministradores es cómo los paquetes son administrados. *PIP* por lo general instala un paquete con dependencias o paquetes necesarios, sin chequear su versión, lo cual a veces reemplaza los existentes creando conflicto. Conda sin embargo, analiza el *environment* y estructura una instalación compatible entre todos los paquetes sin deterioralo o advirtiendole al usuario cuando no puede evitar alterarlo.

La distribución también incluye un GUI (Interfaz Gráfica de Usuario - *Graphical User Interface*) llamada ***Anaconda Navigator***.

## ¿Qué es Anaconda *Navigator*?

Anaconda *Navigator* es una Interfaz Gráfica de Usuario (*GUI*) que permite a los usuarios administrar aplicaciones y herramientas para el análisis de datos y sus correspondientes paquetes. Destro de este *GUI* se puede usar el lenguaje de programación **Python** para el cual está orientado, pero tambien se puede contar con el uso del lenguaje de programción **R**, **Julia** u **Octave**.

Las aplicaciones que se pueden encontrar en Anaconda *Navigator* son las siguientes.

- **JupyterLab**: Es un entorno de desarrollo basado en la web con el cual se pueden construir cuadernos de trabajo, código y analizar datos. Con esta herramienta se pueden organizaar flujos de trabajo en ciencia de datos, computación científica y muchas otras cosas.
- *****Jupyter notebook*****: Es una aplicación que nos permite construir cuadernos para escribir nuestros flujos de análisis.
- **Spyder**: Es un entorno de desarrollo integrado (*IDE*) para programación científica en el lenguaje de **Python**.
- **Orange**: Es una aplicación para programación visual que se basa fuertemente en la visualización de los datos, *machine learning*, mineria de datos y análisis de datos.
- **Visual Studio Code**: Esta aplicación es un editor de código fuente con funciones para corrección rápida de sintaxis y puede usarse con el programa de control de versiones **Git**.
- **R-Studio**: Es un entorno de desarrollo integrado orientado para el lenguaje de programación.

## ¿Cómo instalar Anaconda *Navigator*?

Debemos ir a la página de  [Anaconda](https://www.anaconda.com/) y descargamos el ejecutable en el siguiente link:

![](https://repo.anaconda.com/archive/Anaconda3-2022.05-Windows-x86_64.exe)

Una vez descargado el archivo y se ejecuta le damos *next*:

![](Python/Anaconda/Instalar_Anaconda/Fig01.png)

Aceptamos la licencia de uso:

![]()

Por seguridad en el equipo se debe escoger el uso simple:

![](Fig04.png)

Seleccionamos un folder de instalación preferiblemente con una ruta que no contenga espacios y luego seleccionamos registrar Anaconda3 como python 3.9 por defecto. Damos *next* hasta finalizar la instalación:

![](Vid01.gif)

Una vez instalada podemos encontrar la aplicación en el menú de inicio en la carpeta **Anaconda3 (64-bit)**.

![](Fig05.png)

## Problemas con la instalación.

Algunas veces al instalar el Anaconda *Navigator* encontramos algunos problemas, como por ejemplo **errores de negación de acceso** (***Acess Denied Error***).

Para corregir esto, podemos usar el **Anaconda Prompt (Anaconda3)** y verificar si Anaconda *Navigator* está bien instalado. Para esto podemos desplegar los paquetes instalados con el siguiente comando:

```conda
conda list
```

Si Anaconda *Navigator* está instalado correctamente, se desplegará el listado de paquetes instalados.


```conda
# packages in environment at C:\Users\cbermudezr\Anaconda3:
#
# Name                    Version                   Build  Channel
_anaconda_depends         2020.07                  py38_0
_ipyw_jlab_nb_ext_conf    0.1.0                    py38_0
_tflow_select             2.3.0                     eigen
absl-py                   0.13.0           py38haa95532_0
alabaster                 0.7.12             pyhd3eb1b0_0
anaconda                  custom                   py38_1
...
```

Otra forma de verificarlo es lanzando el lenguaje de programación python con el comando: ```python```. Este comando lanzará el *shell* de Python y si Anaconda está bien instalado , desplegará la información de la versión incluyendo el termino "Anaconda":

```conda
Python 3.8.8 (default, Apr 13 2021, 15:08:03) [MSC v.1916 64 bit (AMD64)] :: Anaconda, Inc. on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Para cerrar este *shell* se debe ejecutar el comando ```quit()```.

Otra forma de corroborar la instalación es tratando de abrir el Anaconda *Navigator* con el comando ```anaconda-navigator```. Si Anaconda está bien instalado, se lanzará el Navegador:

![](Fig06.png)


Algunas veces este último paso falla  y debemos reparar la vía de acceso del Anaconda *Navigator*, esto se puede hacer con una serie de pasos que llevará a la actualización de la versión, solucionando el problema.

Se debe abrir el Anaconda *prompt* y una vez abierto se debe ejecutar el comando:

```conda
conda update conda
```
![](Vid02.gif)

Una vez terminado este comando se debe ejecutar el siguiente comando:

```conda
conda update anaconda-navigator
```

![](Vid03.gif)

El siguiente paso será ejecutar el siguiente comando:

```conda
anaconda-navigator --reset
```

![](Vid04.gif)

Ahora se ejecuta el comando:

```conda
conda update anaconda-client
```

![](Vid05.gif)

Por último se ejecuta el comando:

```conda
conda update -f anaconda-client
```

![](Vid06.gif)

## Creando ambientes de trabajo (*Environments*).

Para crear un ambiente de trabajo para los lenguajes de programación **Python**, [**R**](https://cran.r-project.org/bin/windows/base/) y [Julia](https://julialang.org/downloads/), se deben tener instalados estos tres últimos programas. 


### Julia

Para instalar el paquete necesario para desplegar **Julia** en Anaconda y ***jupyter notebooks*** se debe instalar el paquete IJulia.


```julia
using Pkg
Pkg.add("IJulia")
```
![](Vid07.gif)

Una vez instalado el paquete se puede observar en la pestaña *New* del *****Jupyter notebook***** la instalación de Julia y su número de versión.

![](Fig07.png)

Dándole click a *New* se puede crear un cuaderno de *****Jupyter notebook***** para trabajar con el lenguaje Julia.

![](Fig08.png)

### R
Para que **R** se pueda desplegar en Anaconda *Navigator* hay instalar varias aplicaciones con el ```conda```. Por lo general Anaconda *Navigator* trae instalado por defecto la versión 3.6.1, pero si se desea trabajar con la última versión se debe crear una ambiente vacío dentro de ```conda``` y luego dentro de este ambiente vacío se debe instalar la versión de R deseada.

Los pasos para crear una ambiente vacío son los siguientes:

Se debe abrir el Anaconda Prompt (Anaconda3) y se ejecutan los siguientes comandos uno por uno:

```conda
conda deactivate
conda create --name R4-Base #R4-Base es el nombre que se le dió a este ambiente. Se puede usar cualquier otro nombre.
conda activate R4-Base

```
![](Vid08.gif)

Despues de crear el ambiente vacío y activarlo con el último comando, se debe instalar la versión deseada del R con los siguientes comandos:


```conda
conda install -c conda-forge r-base
conda install -c conda-forge/label/gcc7 r-base
```
![](Vid09.gif)

```conda
conda install -c conda-forge/label/broken r-base
 ```

![](Vid10.gif)

```conda
conda install -c conda-forge/label/cf201901 r-base
 ```
![](Vid11.gif)

```conda
conda install -c conda-forge/label/cf202003 r-base 
```

![](Vid12.gif)

Finalizado la creación e instalación de las bases de **R** se puede instalar la versión deseada por medio del siguiente comando:

```conda
conda install -c conda-forge r-base=4.X.X   #Con este comando puede escoger la versión del R que se desee instalar
```

Una vez hecha esta instalación, se  debe instalar los paquetes de R necesarios para instalar el kernel que va a manejar el ***Jupyter notebook***.

Se debe activar la sesión de **R** en el ambiente creado, en este caso R4-Base:

![](Vid13.gif)

Una vez dentro de la sesión de R activada se deben instalar los paquetes con los siguientes comandos:

```r
install.packages(c("repr", "IRdisplay", "evaluate", "crayon", "pbdZMQ", "devtools", "uuid", "digest"))
```
![](Vid14.gif)


Luego se instala el kernel.


```r
install.packages("IRkernel")
```
![](Vid15.gif)

Una vez instalado se hace disponible para el ***Jupyter notebook***.

```r
IRkernel::installspec()
```

![](Vid16.gif)


Terminada la instalación de los paquetes, se debe salir de la sesión de **R** con el comando ```quit()``` y se procede a activar el ***Jupyter notebook*** con el comando ```jupyter notebook```:

![](Vid17.gif)

Una vez abierto el  ***Jupyter notebook*** se debe crear un nuevo "cuaderno" con el lenguaje **R**:

![](Fig10.png)


Una vez finalizados estos pasos, el Anaconda *Navigator* queda con un *Environment* que contiene la última versión del **R** y **Julia** y se pueden crear ***Jupyter notebooks*** que sean ejecutables con estos lenguajes.


![](Fig11.png)


Al desplegar el ***Jupyter notebook*** desde el Anaconda *Navigator* podemos corroborar que las sesiones se crean con el *R* version 4.1.3.

![](Vid18.gif)