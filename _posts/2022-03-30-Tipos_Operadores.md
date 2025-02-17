---
title: "Introducción al Lenguaje R: Tipos de Operadores"
output:
  md_document:
    variant: gfm+footnotes
    preserve_yaml: TRUE
knit: (function(inputFile, encoding) {
  rmarkdown::render(inputFile, encoding = encoding, output_dir = "../_posts") })
date: '2022-03-30'
permalink: /posts/2022/03/RLanguage
excerpt_separator: <!--more-->
toc: true
tags:
- Programación en R
- Operadores de programación
- R Studio
---
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 581 512"  width="50px" height="50px"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M581 226.6C581 119.1 450.9 32 290.5 32S0 119.1 0 226.6C0 322.4 103.3 402 239.4 418.1V480h99.1v-61.5c24.3-2.7 47.6-7.4 69.4-13.9L448 480h112l-67.4-113.7c54.5-35.4 88.4-84.9 88.4-139.7zm-466.8 14.5c0-73.5 98.9-133 220.8-133s211.9 40.7 211.9 133c0 50.1-26.5 85-70.3 106.4-2.4-1.6-4.7-2.9-6.4-3.7-10.2-5.2-27.8-10.5-27.8-10.5s86.6-6.4 86.6-92.7-90.6-87.9-90.6-87.9h-199V361c-74.1-21.5-125.2-67.1-125.2-119.9zm225.1 38.3v-55.6c57.8 0 87.8-6.8 87.8 27.3 0 36.5-38.2 28.3-87.8 28.3zm-.9 72.5H365c10.8 0 18.9 11.7 24 19.2-16.1 1.9-33 2.8-50.6 2.9v-22.1z"/></svg>
En este *post* explicaré cuales son los tipos de operadores que hay en la programación con el lenguaje R, cómo se utilizan y para que sirven. Al final se pondrán en practica algunos de los conocimientos adquiridos por medio de ejercicios.
<!--more-->

- [Tipos de Operadores](#tipos-de-operadores)
  - [Operadores de asignación](#operadores-de-asignación)
  - [Operadores aritméticos](#operadores-de-aritméticos)
  - [Operadores lógicos](#operadores-lógicos)
  - [Operadores relacionales](#operadores-relacionales)
  - [Reglas de prioridades para las operaciones](#reglas-de-prioridades-para-las-operaciones)
  - [Ejercicios](#ejercicios)

# Tipos de Operadores

Los principales operadores que se usan en R son:

1. Operadores de asignación.
2. Operadores aritméticos.
3. Operadores lógicos.
4. Operadores relacionales.


## Operadores de asignación

Los operadores de asignación son aquellos que nos permiten crear o asignarles valores a objetos. 

| Símbolo | Descripción |
|:-:|:-:|
|= | igual|
|<-| "convertirse" (*become*)  la izquierda|
|->| "convertirse" (*become*)  la derecha|


En el siguiente ejemplo se asignan valores a los objetos *numero* y *letra*.

```r
 numero= 12
"ABC" -> letra 
```
  
```r
numero
 [1]  12
```

```r
letra
"ABC"
```

## Operadores aritméticos

Los operadores aritméticos se usan para realizar operaciones matemáticas.Estas operaciones se pueden llevar a cabo con valores numéricos o con objetos que tienen valores numéricos.

Los operadores aritméticos que se usan en el lenguaje de programación R son:

| Símbolo | Operación |
|:-:|:-:|
|+ | Suma|
|- | Resta|
| * | Multiplicación|
|/ | División|
|^ | Potencia|
|%% | División Entera|


Las sumas se puede llevar a cabo entre valores numéricos:

```r
2 + 3
[1] 5
```


También se pueden realizar operaciones entre objetos pero solo que estos contengan valores numéricos:

```r
cinco = 5
tres = 3
cinco + tres
[1] 8
```

Con los anteriores objetos se puede aplicar los demás operadores:

```r
cinco - tres
[1] 2
```


```r
cinco * tres
[1] 15
```


```r
cinco / tres
[1] 1.666667
```

```r
cinco ^ tres
[1] 125
```

La división entera es un caso especial donde el resultado no es el cociente sino el residuo de la operación:

```r
cinco %% tres
[1] 2
```


```r
cinco %% 4
[1] 1
```


## Operadores Lógicos

Los operadores lógicos se utilizan para hacer comparaciones entre valores, estos pueden ser númericos o no, devolviendo como resultado otro valor que se conoce como *Booleano* que pueden ser ciertos (*TRUE*) o falso (*FALSE*).

Los operadores lógicos son tres y representan la negación, la conjunción y la disyunción.

| Símbolo | Operación |
|:-:|:-:|
|! | Negación|
|& | Conjunción|
| \|| Disyunción|


### Negación (NOT)

El símbolo de negación en el lenguuaje de programación R es !. La negación (NOT) representa una operación que da la negación booleana del objeto al que se le aplique. Este operador es unitario, esto quiere que se aplica a un solo valor. En teoría de conjuntos se entendería como una exclusión.

En el siguiente ejemplo veremos que el valor booleano TRUE al ser negado por el operador lógico ! se convierte en su contrario:

```r
!TRUE
FALSE
!FALSE
TRUE
```


### Conjunción (AND)

El símbolo de conjunción en el lenguaje de programación R es &. La conjunción (AND) representa una operación que da como resultado un valor booleano TRUE solo si ambas proposiciones son ciertas y se identifica con la palabra en español "y". Este operador es binario, esto quiere decir que se aplica a dos valores.En teoría de conjuntos se entendería como una intersección.

En el siguiente ejemplo veremos todas las operaciones de conjunción que se presentan entre los valores booleanos y sus respectivos resultados:

```r
TRUE & TRUE
[1] TRUE
```


```r
TRUE & FALSE
[1] FALSE
```



```r
FALSE & TRUE
[1] FALSE
```

```r
FALSE & FALSE
[1] FALSE
```


### Disyunción (OR)

El símbolo de disyunción en el lenguaje de programación R es \|. La disyunción (OR) representa una operación que da como resultado un valor booleano FALSE solo si ambas proposiciones son falsas y se identifica con la palabra en español “ó”. Este operador también es binario, esto quiere decir que se aplica a dos valores.En teoría de conjuntos se entendería como una unión.

En el siguiente ejemplo veremos todas las operaciones de Disyunción que se presentan entre los valores booleanos y sus respectivos resultados:


```r
TRUE | TRUE
[1] TRUE
```


```r
TRUE | FALSE
[1] TRUE
```



```r
FALSE | TRUE
[1] TRUE
```



```r
FALSE | FALSE
[1] FALSE
```


## Operadores relacionales

Los operadores relacionales son símbolos que se usan para comparar dos valores, cuyo resultado es un valor booleano. Muchas veces estos operadores se ven estrechamente relacionados con los operadores lógicos.

| Símbolo | Operación |
|:-:|:-:|
|\< | Menor que|
|\> | Mayor que|
|\== | Igual que|
|\!= | No es igual que|
|\<= | Menor o igual que|
|\>= | Mayor o igual que|


### Menor que (<)

El símbolo de < compara dos valores numéricos y devuelve un resultado booleano de *TRUE*  cuando el valor de la izquierda del símbolo es menor al valor de la derecha del símbolo, si no es cierta la relación, entonce devolverá el resultado booleano de *FALSE*.

```r
308 < 4500
[1] TRUE
```


Es posible relacionar datos tipo *character*, sin embargo el lenguaje de programación R siempre toma como valor de relación la primera letra de la cadena de texto, asumiendo el orden alfabético.

```r
"zorro" < "burro"
[1] FALSE
```

En el anterior ejemplo, R asume que zorro tiene una posición alfabetica mayor a burro, por lo tanto el valor de la relación no sería cierta (FALSE).
### Mayor que (>)

El símbolo de > compara dos valores numéricos y devuelve un resultado booleano de *TRUE*  cuando el valor de la derecha del símbolo es mayor al valor de la izquierda del símbolo, si no es cierta la relación, entonce devolverá el resultado booleano de *FALSE*.

```r
8900 > 23000
[1] FALSE
```


El anterior ejemplo con cadenas de texto tendría el siguiente resultado con el símbolo mayor que.

```r
"zorro" > "burro"
[1] FALSE
```

Es cierta esta relación porque la cadena de texto "zorro" tiene una posición en el orden alfabético mayor que la cadena de texto "burro", ya que se basa en la primera letra de ambas cadenas.

### Igual que (==)

Este símbolo == evalúa si dos valores son exactamente iguales entre si, y estos valores pueden ser numéricos o cadenas de texto, devolviendo un resultado booleano de *TRUE* cuando los valores a ambos lados del símbolo son exactamente iguales o *FALSE* cuando no son exactamente iguales.

```r
636 == 366
[1] FALSE
```


Las cadenas de texto evaluan el número de caracteres.

```r
"zorro" == "burro"
[1] FALSE
```


```r
"zorro" == "zorro"
[1] TRUE
```

### No es igual que (! =)

El símbolo relacional de "no es igual que" combina un símbolo lógico (! negación) y un símbolo relacional (=). 

Este símbolo compara si un valo no es igual al otro y devuelve un valor booleano de *TRUE* cuando el valor de la izquierda no es igual al de la derecha y si son iguales devuelve un valor booleano de *FALSE*.

```r
3!=4
[1] TRUE
```

```r
3!=3
[1] FALSE
```


Para cadenas de texto, el símbolo evalúa si ambos valores tienen el mismo número de caracteres.

```r
"casa" != "caza"
[1] TRUE
```

### Menor o igual que (<=)

El operador menor o igual que, evalúa si el valor de la izquierda es menor o exactamente igual al valor de la derecha del símbolo.

```r
56<=56
[1] TRUE
```

El uso del símbolo menor que, no incluye dentro del intervalo de evaluación el número en cuestión, por lo tanto cuando se evalúa la relación anterior, esta relación es falsa.

```r
56<56
[1] FALSE
```


### Mayor o igual que (>=)

De manera similar al símbolo "menor o igual que", el símbolo "mayor o igual que" evalúa si el valor de la izquierda es mayor o exactamente igual al valor de la derecha del símbolo.

```r
56>=56
[1] TRUE
```

## Reglas de prioridades para las operaciones

En el lenguaje de programación R las operaciones tienen prioridades al igual que en las matemáticas. Cuando se practica una serie de operaciones al mismo tiempo, algunas de ellas tienen prioridad sobre otras.

El orden de prioridades de las operaciones son las siguientes:

| Orden | Operadores |
|:-:|:-:|
|1| ^ |
|2| * / |
|3| + - |
|4| < > <= >= == !=|
|5| !|
|6| & |
|7|  \||
|8| <-|

```r
5+3*6
[1] 23
```


Si se debe dar una prioridad distinta a las operaciones, se deben usar los parentesis así:

```r
(5+3)*6
[1] 48
```

# Ejercicios

## Ejercicio 1

Crear un objeto que se llame m con valor de 850000 y un objeto que se llame c con valor de 450890. Hacerlo con todos los símbolos de asignación posibles.

## Ejercicio 2

Multiplicar los dos objetos anteriores por 10 y dividirlos por 10000 y luego resolver lo siguiente:


```r
$$m^2 + c^2/m+c$$
```

## Ejercicio 3

Cambiar el orden de prioridades de los operadores de la anterior ecuación para que la respuesta sea 711.668.

## Ejercicio 4

¿El valor del resultado del ejercicio 2 es mayor o igual que el del ejercicio 3? Probarlo a través del uso un operador lógico que compare las ecuaciones, no los resultados.

## Ejercicio 5

Representar en código la siguiente afirmación y probar su valor booleano.

**"Es cierto que m es mayor que c y que las priorización de operadores del ejercicio 3 es menor que la priorización de operadores del ejercicio 2**.

## Reto

Resolver la siguiente ecuación y que el resultado final sea: 16.94415

```r
$$m^3 +c^2/85*96+m*c$$
``` 
