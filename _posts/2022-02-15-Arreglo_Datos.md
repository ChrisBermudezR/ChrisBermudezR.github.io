---
title: "Introducción al lenguaje R: Tipos de Datos"
output:
  md_document:
    variant: gfm+footnotes
    preserve_yaml: TRUE
knit: (function(inputFile, encoding) {
  rmarkdown::render(inputFile, encoding = encoding, output_dir = "../_posts") })
date: '2022-02-15'
permalink: /posts/2022/02/RLanguage
excerpt_separator: <!--more-->
toc: true
tags:
- Programación en R
- Operadores de programación
- R Studio
---
En este *post* explicaré el manejo de algunos tipos de datos básicos en el lenguaje de programación R. Definiré qué son las variables y qué son los objetos y explicaré como asignar variables a objetos. Además, explicaré como usar los comandos que nos dan información sobre la naturaleza de los datos.

<!--more-->

# Definición de  Variables y Objetos.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M100.59 334.24c48.57 3.31 58.95 2.11 58.95 11.94 0 20-65.55 20.06-65.55 1.52.01-5.09 3.29-9.4 6.6-13.46zm27.95-116.64c-32.29 0-33.75 44.47-.75 44.47 32.51 0 31.71-44.47.75-44.47zM448 80v352a48 48 0 0 1-48 48H48a48 48 0 0 1-48-48V80a48 48 0 0 1 48-48h352a48 48 0 0 1 48 48zm-227 69.31c0 14.49 8.38 22.88 22.86 22.88 14.74 0 23.13-8.39 23.13-22.88S258.62 127 243.88 127c-14.48 0-22.88 7.84-22.88 22.31zM199.18 195h-49.55c-25-6.55-81.56-4.85-81.56 46.75 0 18.8 9.4 32 21.85 38.11C74.23 294.23 66.8 301 66.8 310.6c0 6.87 2.79 13.22 11.18 16.76-8.9 8.4-14 14.48-14 25.92C64 373.35 81.53 385 127.52 385c44.22 0 69.87-16.51 69.87-45.73 0-36.67-28.23-35.32-94.77-39.38l8.38-13.43c17 4.74 74.19 6.23 74.19-42.43 0-11.69-4.83-19.82-9.4-25.67l23.38-1.78zm84.34 109.84l-13-1.78c-3.82-.51-4.07-1-4.07-5.09V192.52h-52.6l-2.79 20.57c15.75 5.55 17 4.86 17 10.17V298c0 5.62-.31 4.58-17 6.87v20.06h72.42zM384 315l-6.87-22.37c-40.93 15.37-37.85-12.41-37.85-16.73v-60.72h37.85v-25.41h-35.82c-2.87 0-2 2.52-2-38.63h-24.18c-2.79 27.7-11.68 38.88-34 41.42v22.62c20.47 0 19.82-.85 19.82 2.54v66.57c0 28.72 11.43 40.91 41.67 40.91 14.45 0 30.45-4.83 41.38-10.2z"/></svg>

## Variables.

En programación, un concepto básico es el de variable. Una variable se define como una *"cosa"* que es susceptible de ser modificada, de cambiar, en función de un evento que puede ser determinado o indeterminado. 

Muchas veces, en el campo científico y técnico, el término variable alude a cosas que presentan poca estabilidad en el tiempo y que nunca son constantes (*e.g.* el clima, la estatura de un niño, la velocidad de un proyectil).

Dependiendo de la forma de medirla, una variable puede ser **cualitativa** o **cuantitativa**. Las variables cualitativas se definen como aquellas que expresan o describen cualidades o características diferentes de un fenómeno. Las variables cuantitativas son las que expresan valores netamente numéricos y por lo general son tomadas de medidas escalares.

Las variables **cualitativas** se pueden clasificar en:

1. **Ordinales:** La variable puede tomar un valor de un número o una letra, pero expresarán un ordenamiento de los valores con respecto a una escala determinada por el usuario. *Ej:* los grados de un colegio (*e.g* grado 1A, grado 1B, grado 1C).

2. **Nominales:** Las variables no tienen valores que reflejen algún tipo de orden.*Ej:* los nombres de los países (*e.g.* Alemania, Francia, Colombia, Zimbabwe)

Las variables **cuantitativas** se pueden clasificar en:

1. **Discretas:** La variable tendrá valores enteros y definidos entre la variación de la escala seleccionada. *Ej:* el número de niños en un salón de clase (*e.g.* 50 niños).

2. **Continuas:** La variable podrá adquirir cualquier valor entre el intervalo de valores en una escala. *Ej:* la temperatura de un salón de clase (*e.g.* 30.5°C).

Dependiendo la influencia que tengan este último tipo de variable, se pueden de nuevo clasificar en:

1. **Variable independiente:** El valor que se expresa esta variable no depende de otra variable. Este tipo de variables cuando se analizan en un plano cartesiano, se representa en el eje de las abscisas (eje x). *Ej:* el brillo de las estrellas.

2. **Variable dependiente:** El valor que se expresa esta variable depende de otra variable. Este tipo de variables cuando se analizan en un plano cartesiano, se representa en el eje de las ordenadas (eje y). *Ej:* la temperatura ambiental en una calle.


## Objetos.

Los objetos en programación se consideran como la información que manipulamos, a la cual se le puede aplicar algún tipo de operación o análisis. Estos objetos vienen definidos por una serie de atributos que pueden ser los que describen a qué tipo de variable corresponden. Los objetos se guardan en la memoria temporal de la consola de R que de ahora en adelante se conocerá como *"Environment"*. Para llamar los objetos desde el *"Environment"*, es necesario escribir su nombre en la consola como veremos más adelante.

En el lenguaje de programación R, los objetos pueden adquirir muchísimas formas y se les puede asignar diferentes variables que van desde la asignación de un valor numérico simple como el número uno, hasta la asignación de un archivo que represente un video o una pista musical (*si, usted leyó bien, UNA PISTA MUSICAL!!!!*). En lo anterior, radica la versatilidad y el poder de los tipos de lenguajes de programación orientados a objetos.


# Asignación de valores a un objeto.

Para asignar un valor de una variable de cualquier tipo a un objeto, se pueden utilizar los símbolos <- ó = de la siguiente manera:

```json
a <- 4 
a = 4
```


Cualquiera de la dos formas de asignación de valores a un objeto, tendrá el mismo resultado.

Para llamar el objeto a que creamos con el valor 4, se debe solo digitar el nombre del objeto en la consola de la siguiente manera.

```json
a
4
```


Esto índica que el objeto a tiene un valor de 4.

El símbolo **<-** se conoce como *"become"* que en inglés significa **"Convertirse en"**. Sin embargo, también puede interpretarse como una flecha que apunta hacia la dirección de la asignación, ya que podemos asignar valores con el símbolo **->** de la siguiente manera:

```json
4->a
```


Lo anterior, también asigna el valor 4 al objeto a como en el primer código.

Una vez que se tiene creado un objeto, a este se le puede aplicar cualquier operación como la siguiente:

```json
a + 6
10
```


Lo que obtenemos a partir de esta operación, que matemáticamente no tiene sentido, salvo que el objeto a en este caso está guardado en la memoria de lenguaje de programación y representa el valor 4. Al hacer la operación con una constate como el número 6, el resultado final será 10.

Los objetos se les puede nombrar de cualquier manera pero con algunas restricciones. Un objeto puede tener un nombre largo como por ejemplo *Inversiones* y se le puede asignar cualquier valor o conjunto de valores. Sin embargo, la forma de nombrar objetos tiene restricciones de tipo **valor**, esto quiere decir que un objeto no puede ser nombrado con un valor numérico, pero si con un valor simbólico. Para ser mas claro, no se puede nombrar un objeto para la variable 4 con un valor numérico de 3, porque se generaría un error lógico asi:

```json 
3=4
```



Este error significa que no se puede asignar el valor izquierdo (*inválido (do_set) lado izquierdo de la asignación*) al valor derecho, y esto es debido a que ambos son constantes. 

Otra condición necesaria para asignar nombres es que estos siempre deben empezar con una letra:

```json
3_clientes = 34

```


Este error indica que no es esperado la entrada *3_*, lo cuál debe ser corregido asignando cualquier tipo de letra antes que el número:

```json 
A3_clientes = 34
```


Este código asigna el valor 34 al objeto A3_clientes, pero si el nombre tuviera un símbolo o caracter especial, este no podría ser asignado, com por ejemplo:

```json 
A3_)clientes = 34
```


Este error sugiere que en el código no tiene sentido el símbolo ")" ya que estos se usan en otras circunstancias que máss adelante serán tratadas.

En el lenguaje de programación de R, existe una posibilidad contraintuitiva que nos plantearon en nuestras clases de matemáticas básicas cuando eramos niños, la posibilidad de sumar peras con manzanas. Esto solo es posible a través de la creación de objetos como lo veremos a continuación.

```json
manzanas= 56
peras= 45

manzanas + peras

```


Lo anterior solo es posiible porque las manzanas y las peras son objetos con valores numéricos.

Un objeto también puede ser creado a partir del resultado de una operación de dos objetos, de la siguiente manera:

```json
resultado<-manzanas - peras

resultado
```


En este último ejemplo, el resultado de la operación de resta se guarda en el nuevo objeto *resultado*.

# Tipos de Datos.

En los lenguajes de programación se ven reflejados los diferentes tipos de variables que hemos visto, sin embargo, cuando creamos un objeto con esas variables, este objeto adquiere unos atributos que son universales para cualquier cálculo o análisis con las herramientas dadas por el lenguaje; lo cual debe ser muy claro para el usuario, porque de esto dependerá el tipo de operación que se pueda llevar a cabo con el objeto.

Existen diferentes tipos de datos dentro del lenguaje de programación R, que a su vez se pueden almacenar en diferentes tipos de arreglos de datos para análisis más complejos.

## Datos Numéricos.

#### *Numeric:*
Los números reales en el lenguaje de R se representan con el tipo *numeric* (*e.g.* 7.12). Con éste tipo de números se pueden realizar operaciones de cualquier tipo.

#### *Integer:*

Los números enteros se representan a través de un tipo de número especial llamado *Integer* (*e.g.* 7). Para especificar que un número es entero, se debe anadir la letra L en mayuscula como sufijo. 

```json
cuarenta<-40L
cuarenta
```



## Datos de texto.

Cualquier dato alfanumérico o cadenas (*strings*) y que no sea exclusivamente un número es interpretado como un *character*. Un ejemplo de esto es:

```json
"Aprendiendo R"
```


Los datos de tipo *character* se asignan siempre entre comillas, para indicarle al lenguaje que es una cadena de texto.

## Datos lógicos.

El tipo de datos lógicos es la forma para los datos binarios y se conocen como *logical*. Estos se usan en pruebas lógicas y toman los valores TRUE y FALSE los cuales pueden ser abreviados como T y F en mayúscula.



```json
10 > 5
```

## Datos ausentes.

Muchas veces cuando se realizan tomas de muestras, algunos datos no es posible tomarlos o estos pueden perderse. Para indicarle al lenguaje de programación sobre esta situación se debe establecer un valor para estos datos. Por lo general se utiliza el símbolo NA que traduce *"Not Available"*. 

```json
A=NA
A
```

## Datos Temporales.

Los datos temporales son datos complejos que pueden presentar retos de manejo en los diferentes conjuntos de datos. Estos por lo general se basan en diferentes calendarios, horas, días, o meses; y esto hay que tenerlo en cuenta a la hora de calcular la fecha y la hora inicial. Como introducción por el momento se mostrará una forma de crear datos temporales, pero mas adelante se tratará el tema a fondo

```json
as.Date("2021-06-19")
```



# Ejercicios


## Ejercicio 1

Asignar el valor de 5600 a un objeto que se llame R34.

## Ejercicio 2

Corregir el problema de asignación de valores en el siguiente código.

```json

valor-> 4

```


## Ejercicio 3

Asignar un valor de tipo *"numeric"* que sea un número real y que tenga dos cifras decimáles.

## Ejercicio 4

Asignar un valor a un objeto que se llame Ciudades y que cuyo valor sea de tipo "*character"*

## Ejercicio 5

Asignar un valor numérico a un objeto que se llame Z435T y sumarlo al objeto R34 del ejercicio 1.

## Reto

Comparar los objetos del ejercicio anterior y determinar si son iguales, mayor que o menor que y obtener las respuestas como datos lógicos.





