# Taller: Más allá de la nube de palabras: exploración y visualización de textos usando R

> Indicaciones previas para el taller a realizar en conjunto con [Data Campfire](https://www.datacampfire.com/2018/04/04/mas-alla-de-la-nube-de-palabras-exploracion-y-visualizacion-de-textos-usando-r/) el sábado 9 de junio de 2018.


## Antes del taller

### Instalación de R y RStudio

En este taller utilizaremos R a través del IDE RStudio. ¿Qué es un IDE? IDE es el acrónimo de *Integrated Development Environment* (*Entorno de Desarrollo Integrado*). Esto quiere decir que RStudio es una aplicación que nos entrega herramientas para hacer más fácil el desarrollo de proyectos usando R.

Para poder instalar R y RStudio, sigue los siguientes pasos:

- Descarga R desde https://cran.r-project.org/. Debes elegir la opción que corresponda, según tu sistema operativo.
- Instala R en tu computador, tal como lo haces con cualquier programa. 
- Una vez que R ha quedado correctamente instalado, descarga RStudio desde https://www.rstudio.com/products/rstudio/download/. Elige la primera opción, es decir, "RStudio Desktop Open Source License" (gratuita). 
- Instala RStudio en tu computador, tal como lo haces con cualquier programa. 

Si quedó todo bien instalado, cuando abras RStudio deberías ver algo así:

![](https://github.com/rivaquiroga/RLadies-Santiago/blob/master/images/rstudio.png)

En este taller usaremos la última versión de R y RStudio, así que si tienes instalada una versión previa, puede que algunas cosas se vean un poco distintas.

IMPORTANTE: Si te aparece algún error durante este proceso, lo más probabable es que sea por alguna configuración de tu sistema operativo. En ese caso, la mejor manera de buscar una solución es copiar el error que arroja R, pegarlo en tu motor de búsqueda favorito y ver cómo alguien que se enfrentó a eso antes lo resolvió. De todos modos, el día sábado antes del taller habrá un espacio destinado a la resolución de problemas. 

### Instalación de los paquetes de R que utilizaremos

Cuando instalamos R por primera vez en nuestro computador, lo que estamos instalando es lo que se conoce como "R Base", es decir, los elementos centrales del lenguaje de programación. Una de las ventajas de R es que se trata de un lenguaje extensible: la propia comunidad de usuarios puede desarrollar nuevas posibilidades para utilizarlo. La manera de compartir estos nuevos desarrollos es a través de "paquetes", que incluyen, entre otras cosas, código y datos. Una analogía que se suele utilizar para explicar esto es que R Base es un teléfono celular tal como viene de fábrica y los paquetes las _apps_ que descargamos para que tenga más funcionalidades. 

En este tutorial usaremos varios paquetes; algunos especialmente destinados al análisis de textos (como `quanteda`, `tidytext` o `udpipe`) y otros que entregan herramientas para el manejo de datos (como `tidyverse`).

Para instalarlos, 

1. copia el siguiente código:

```r
install.packages("tidytext")
install.packages("quanteda")
install.packages("udpipe")
install.packages("cleanNLP")
install.packages("tm")
install.packages("syuzhet")
install.packages("pdftools")
install.packages("readtext")
install.packages("readxl")
install.packages("tidyverse")
```

2. pégalo en la consola (_Console_) de RStudio:

![](https://github.com/rivaquiroga/taller_datacampfire_mayo/blob/master/images/install.packages.png)

3. presiona 'enter'. 

Dependiendo de tu sistema operativo o versión de R, es posible que en el caso del paquete `quanteda` R te haga una pregunta. La respuesta esa pregunta es __no__. Para seguir, entonces, debes tipear una `n` en la consola y luego presionar `enter`:

![](https://github.com/rivaquiroga/taller_datacampfire_mayo/blob/master/images/pregunta_quanteda.png)

Si todo sale bien, deberías ver algo así al final del proceso:

![](https://github.com/rivaquiroga/taller_datacampfire_mayo/blob/master/images/paquetes_instalados.png)

### Otras aplicaciones

Durante el taller usaremos otras aplicaciones que nos servirán para ver y editar tanto archivos de textos, como los resultados de los análisis. En todos los casos de trata de aplicaciones libres. 
- __Editor de textos__. Si bien tanto Windows como Mac traen uno por defecto, se sugiere descargar [Sublime Text](https://www.sublimetext.com/).
- __Hoja de cálculo__. Se sugiere [LibreOffice](https://es.libreoffice.org/descarga/libreoffice/). Para el propósito que la utilizaremos funciona mejor que Excel. 

### ¿Quieres avanzar más?

Este workshop no supone ningún conocimiento previo de R, pero si te interesa llegar un poco más familiarizada/o, te sugiero darle una mirada [al siguiente tutorial introductorio](https://github.com/rivaquiroga/RLadies-Santiago/blob/master/2018-04_taller_primeros_pasos_en_R.Rmd). La primera parte (instalación de R, RStudio y paquetes) es similar; el resto está enfocado al trabajo con datos "rectangulares", es decir, ordenados en filas y columnas (_dataframes_).
