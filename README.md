# Taller: Más allá de la nube de palabras: exploración y visualización de textos usando R
[Taller realizado en conjunto con DataCampfire el 12 de mayo de 2018]

## Instalación de R y RStudio

En este taller utilizaremos R a través del IDE RStudio. ¿Qué es un IDE? IDE es el acrónimo de Integrated Development Environment, es decir, de un Entorno de Desarrollo Integrado. En palabras simples, se trata de un entorno que nos entrega herramientas para trabajar de manera más fácil con un determinado lenguaje de programación (en este caso, R). 

Para poder instalar R y RStudio, sigue los siguientes pasos:

- Descarga R desde https://cran.r-project.org/. Debes elegir la opción que corresponda según tu sistema operativo.
- Instala R en tu computador, tal como lo haces con cualquier programa. 
- Chequea que el programa haya quedado adecuadamente instalado (por ejemplo, abriéndolo).
- Descarga RStudio desde https://www.rstudio.com/products/rstudio/download/. Elige la primera opción, es decir, "RStudio Desktop
Open Source License" (gratuita). 
- Instala RStudio en tu computador, tal como lo haces con cualquier programa. 
- Chequea que el programa haya quedado adecuadamente instalado.

## Instalación de los paquetes de R que usaremos

En este taller usaremos con una serie de paquetes de R que nos permitirán analizar textos y hacer más simple nuestro proceso de trabajo. Es importante que los tengas instalados antes del comienzo del workshop.

```r
install.packages("tidyverse")
install.packages("tidytext")
install.pacckages("quanteda")
```
