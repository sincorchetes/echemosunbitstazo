---
title: 'Primeros pasos con Python'
published: false
---

Primeros pasos con Python

# Historia
Python es un lenguaje de programación interpretado, de alto nivel y de interés general. Este lenguaje tiene una filosofía de programación que se centra en la legibilidad del código, para ello implementa una serie de declaraciones y estándares que ha de respetarse para que el código funcione como es la indentación. Python es un lenguaje orientado a objetos que facilitan a los desarrolladores escribir un código limpio, eficaz, lógico y pequeño que sirve tanto para pequeños, como medianos y grandes proyectos.

La primera versión de Python se publicó en el año 1991 por Guido van Rossum un programador holandés graduado en matemáticas y ciencias computacionales en la universidad de Amsterdam en 1982. Posteriormente se publicó la versión 2.0 el día 16 de octubre del año 2000 y la versión 3.0 que se liberó el 3 de diciembre de 2008. Actualmente las versiones 1.0 y 2.0 ya no están soportadas, esta última dejó de tener soporte el día 31 de diciembre de 2019.

# Instalación
Python por norma general está instalado por defecto en el 99% de distribuciones de Linux por lo que no te hará falta tener que instalar nada. Sin embargo, hay distribuciones que a pesar de que Python 2.* se encuentre obsoleto, la mayor parte de librerías y programas que contienen en su sistema operativo hacen uso de la versión 2.7.* que fue la última en mantenerse. Por lo que, quizás necesites realizar unos pasos adicionales para tener Python 3.* instalado en tu Linux.

Algunas distribuciones pueden ser:
* CentOS 6/7, hay que hacer uso de Software Collections puedes hacer uso de esta guía que <a href="" target="blank">  elaboré.</a>
* Debian Stable
* RHEL 6/7
* Gentoo

En FreeBSD y OpenBSD hay que instalarlo con su respectiva paquería, puedes utilizar estas guía oficial de Python para <a href="https://docs.python.org/3/using/unix.html#on-freebsd-and-openbsd" target="blank">hacerlo.</a>

En Windows y en Mac, tendrán que utilizar otras formas para instalarlo.
<Completar></Completar>

# Conceptos

Como en todos los lenguajes de programación, nos encontraremos casi siempre con los mismos conceptos:
* ¿Qué es una variable?
* ¿Qué es un tipo de dato?
* ¿Qué es una función?

# Palabras clave
Python como otros lenguajes, tienen una serie de palabras que no se deben utilizar bajo ningún concepto para utilizarlos como identificadores, como:

# Identificadores
Los identificadores son el nombre que se utilizan para identificar una variable, función, clases o un objeto.
Las reglas que se utilizan son las siguientes:
* No se utilizan caracteres especiales o numéricos menos ( _ ) que se puede utilizar como un identificador
* Las palabras clave no se utilizan
* Python discrimina de mayúsculas y minúsculas por lo que no es lo mismo llamar a una función o variable `var` si está definida como `Var`.

# Tipos de datos en Python (Literals)
* Cadenas o strings
* Númericos
* Especiales
##  Cadenas o _strings_ 
Se forman encerrando un texto utilizando ( _ " _ ) ó (  _''_ ). 

Por ejemplo: 
```
helloWorld = "Hello world"
helloWorld = 'Hello world'
```

Se puede definir cadenas con múltiples líneas:
```
helloWorldMessage = '''
Este es un mensaje para toda la civilización.
Todos(as) aquellos(as) que no se interesen por la historia,
estarán condenados(as) a repetir los mismos errores que se
cometieron en el pasado. '''
```

## Números
Tenemos varios tipos de dato en Python como puede ser:
* int 
* long (_no se usa más en Python 3_)
* float
* complex

### int ó números enteros
Este tipo de dato solo almacena números enteros (_positivos y negativos, nada de comas, ni decimales, ni fracciones_.
* Este tipo de dato no contiene ninguna restricción por parte del número de bits en Python y puede expandirse el límite de la memoria disponible.
* No se necesita ningún tipo de declaración especial para almacenar números muy largos.
```
a = 1
b = -2
print(a - b)

>>> 3
```


### Float o número de coma flotante
Si necesitas utilizar decimales, este es el tipo de dato que buscar.
```
x = 20.30
y = -33.99
z = 100.12
print(x - y - z)

>>> -45.83
```

### Complex o números complejos 
Se utilizan para diferentes tipos de cálculos aplicados a la geometría, física... La definición en Python es `a+bj`, dónde `a` es el número que se encuentra representado en los números reales; `bj` es el número imaginario.
```
a = 2+3j
print(a)

>>> 2+3j
```

### Tipos de datos especiales
Tenemos el valor `None` que viene a ser el valor `null` en otros lenguajes como SQL, se suele utilizar para declarar un campo con este valor _¡ojo, esto no quiere decir que esté vacío!_

# Tipos de operadores
En Python tenemos varios tipos de oepradores para hacer comparaciones, cálculos, valorar expresiones lógicas....
* Aritmético
* Asignación
* Comparación
* Lógico
* Bit a bit (_bitwise_)
* Identidad
* Membresía

## Aritméticos
Se utiliza para realizar operaciones matemáticas y se utilizando dos operandos para llevarlas a cabo.
|-----|-----|
| Operador | Descripción |
|+| Se utiliza para realizar operaciones de adicción (suma)
|-| Operaciones de sustracción (resta)
|*| Multiplicación
|/| División (resto)
|%| División (cociente), Módulo 
