---
title: "Introducción al Lenguaje Python: Tipos de Datos"
output:
  md_document:
    variant: gfm+footnotes
    preserve_yaml: TRUE
knit: (function(inputFile, encoding) {
  rmarkdown::render(inputFile, encoding = encoding, output_dir = "../_posts") })
date: 2023-10-21
permalink: /posts/2023/10/python
excerpt_separator: <!--more-->
toc: true
tags:
- Programación en Python
- Operadores de programación
- Python
---
<svg xmlns="http://www.w3.org/2000/svg" height="5em" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M439.8 200.5c-7.7-30.9-22.3-54.2-53.4-54.2h-40.1v47.4c0 36.8-31.2 67.8-66.8 67.8H172.7c-29.2 0-53.4 25-53.4 54.3v101.8c0 29 25.2 46 53.4 54.3 33.8 9.9 66.3 11.7 106.8 0 26.9-7.8 53.4-23.5 53.4-54.3v-40.7H226.2v-13.6h160.2c31.1 0 42.6-21.7 53.4-54.2 11.2-33.5 10.7-65.7 0-108.6zM286.2 404c11.1 0 20.1 9.1 20.1 20.3 0 11.3-9 20.4-20.1 20.4-11 0-20.1-9.2-20.1-20.4.1-11.3 9.1-20.3 20.1-20.3zM167.8 248.1h106.8c29.7 0 53.4-24.5 53.4-54.3V91.9c0-29-24.4-50.7-53.4-55.6-35.8-5.9-74.7-5.6-106.8.1-45.2 8-53.4 24.7-53.4 55.6v40.7h106.9v13.6h-147c-31.1 0-58.3 18.7-66.8 54.2-9.8 40.7-10.2 66.1 0 108.6 7.6 31.6 25.7 54.2 56.8 54.2H101v-48.8c0-35.3 30.5-66.4 66.8-66.4zm-6.7-142.6c-11.1 0-20.1-9.1-20.1-20.3.1-11.3 9-20.4 20.1-20.4 11 0 20.1 9.2 20.1 20.4s-9 20.3-20.1 20.3z"/></svg>
En este *post* explicaré cuales son los tipos de datos que existen en la programación con el lenguaje Python, cómo se utilizan y para que sirven. Al final se pondrán en practica algunos de los conocimientos adquiridos por medio de ejercicios.
<!--more-->

Temario
- [Tipos de datos en Python](#tipos-de-datos-en-snake)
  - [Numéricos: Enteros y reales](#numéricos-enteros-y-reales)
  - [Enteros](#enteros)
  - [Reales](#reales)
  - [Booleanos](#booleanos)
  - [Caracteres y cadenas de caracteres](#caracteres-y-cadenas-de-caracteres)


## Tipos de datos en Python
Existen varios tipos de datos que se pueden manejar en Python y estos son:
### Numéricos: Enteros y reales

#### Enteros
Se codifican con una palabra ```int``` y se declara mediante la expresión ```x:int```

Ejemplo:
aquí se asignan valores a los objetos ```i, j, p``` y se declaran que son enteros con los valores asignados

```python
i: int = 0
j : int = 1
p : int = -10
```
#### Reales
Se codifican con una palabra ```float``` y se declara mediante la expresión ```x:float```

Ejemplo:
aquí se asignan valores a los objetos ```i, j, p``` y se declaran que son reales con los valores asignados

```python
i: float = 2.0
j : float = 1.6
p : float = -1.960
```
### Booleanos
Se codifican con una palabra ```bool``` y se declara mediante la expresión ```x:bool```, lo que sirve para declarar si dicha variable es ```True``` (Verdadero) ó ```False``` (Falso).

Ejemplo:
aquí se asignan valores a los objetos ```i, j, p``` y se declaran que son reales con los valores asignados

```python
i: bool = True
j : bool = False
p : bool = True
```
### Caracteres y cadenas de caracteres
Un carácter es el elemento mínimo de información usado para representar,  controlar, transmitir y visualizar datos. 

Se codifican con una palabra ```str``` y se declara mediante la expresión ```x:str```.

```python
i: str = "r"
j : str = "tonto"
p : str = "Verdadero"
```

## Operadores
Existen diversos tipos de operadores en Python para llevar a cabo procedimientos tanto matemáticos como de lógica.
### Operadores ariméticos
Los operadores aritméticos en Python son:

|Operador|Operación|
|:-:|:-:|
|+|suma|
|-|resta|
|*|multiplicación|
|/|división|
|//|división entera|
|%|residuo de división|
|**|potencia|
### Operadores de asignación
Para asignar valores a variables se pueden utilizar los siguientes
operadores  infijos.

Estos valores realizan la operación sobre el mismo objeto de la izquierda, por ejemplo:

```python
x += 2 #esto es igual que...
x = x + 2 #esto!
```

|Operador|Operación|
|:-:|:-:|
|=|asignación|
|+=|asignación suma|
|-=|asignación resta|
|*=|asignación multiplicación|
|/=|asignación división|
|//=|asignación división entera|
|%=|asignación residuo de división|

### Operadores lógicos
Los operadores lógicos permiten realizar secuencias de operaciones que tengan una lógica.

|Operador|Operación|
|:-:|:-:|
|¬|not|
|and|y|
|or|ó|

### Operadores de igualdad y relacionales

Los operadores igualdad y relacionales permiten realizar evaluar diferentes valores devolviendo datos booleanos.

|Operador|Operación|
|:-:|:-:|
|==|igualdad|
|!=|diferencia|
|>|mayor que|
|<|menor que|
|>=|mayor o igual que|
|<=|menor o igual que|

### Precedencia de los operadores
 En Python como en otros lenguajes de programación, existe precedencia o gerarquía entre loss signos. por lo general la palabra pnemotécnica de **PEMDAS** nos ayudará a recordar esta precedencia. Esta parabra significa, Paréntesis, Exponencia, Multiplicación, División, Adición y Sustreacción. Sin embargo, hay jerarquía tambien con operadores de igualdad, booleanos y de asignación.

|Operador|Prioridad|
|:-:|:-:|
|()|1|
|¬ -(signo) +(signo) **|2|
|* / // %|3|
|+ - |4|
|< > <= >=|5|
|== !=|6|
|and|7|
|or|8|
|= += -= *= /= //= %=|9|

