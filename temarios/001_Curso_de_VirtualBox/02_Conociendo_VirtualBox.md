# Sección 2: Conociendo VirtualBox 26 min

   * 02 VirtualBox y las máquinas virtuales 04:50 min
   * 03 Ventajas e inconvenientes de las máquinas virtuales 04:24 min
   * 04 Instalación de VirtualBox 06:16
   * 05 Nuestra primera máquina virtual 09:07
   * Preguntas sobre máquinas virtuales y VirtualBox 8 preguntas
   * Resumen 1 páginas



## 02 VirtualBox y las máquinas virtuales

<img src="images/02-02.png">

<img src="images/02-03.png">

Vamos a aprender lo que son las máquinas virtuales y sus características más importantes.


<img src="images/02-04.png">

Así como una aplicación para gestionarlas de la que es objeto este curso VirtualBox que será nuestro software de virtualización para llevar toda esta teoría a la práctica, tanto esta clase como la siguiente son puramente teóricas pero fundamentales, te ruego que pongas mucha atención porque los conceptos que vamos a tratar ahora son fundamentales para adentrarnos con buen pie y empezar a comprender el mundo de la virtualización.

<img src="images/02-05.png">

Lo primero y más básico sería preguntarnos qué es una máquina virtual.

<img src="images/02-06.png">

Según la Wikipedia una máquina virtual se define como un software que simula una computadora y puede ejecutar programas como si fuese una computadora real o dicho de otra forma se trata de una aplicación que simula por software una computadora y que en la práctica tiene las mismas capacidades que una computadora real.

<img src="images/02-07.png">

En adelante para referirnos a la máquina real y a la máquina virtual utilizaremos la nomenclatura **Anfitrión** y **Huésped** la máquina real o física toma el nombre de anfitrión, mientras que la máquina virtual toma el nombre de huésped, como ves los nombres les vienen al pelo.

<img src="images/02-08.png">

Cuando ejecutamos una máquina virtual como es evidente esta máquina virtual o huésped tomará prestado sus recursos del anfitrión o máquina real.

<img src="images/02-09.png">

Veámoslo con un ejemplo, pongamos que tenemos una máquina real con 4 gigas de memoria RAM, si ejecutamos en ella una máquina virtual y le asignamos un giga de ram esta última lo tomará prestado te los 4 gigas con los que cuenta la máquina real, la cual ya solo dispondrá de 3 GB para ejecutarse.

<img src="images/02-10.png">

Pongamnos otro ejemplo, imaginemos que un usuario tiene un PC con Windows y este PC tiene un procesador de cuatro núcleos, 8 GB de memoria RAM y un giga de memoria gráfica, podemos definir una máquina virtual con Linux para que se ejecute dentro de Windows asignándole un núcleo del procesador, 2 gigas de ram 128MB de memoria de vídeo, como antes los recursos que toma el huésped ya no estarán disponibles para la máquina anfitrión. 

<img src="images/02-11.png">

Evidentemente podemos ser más generosos con los recursos asignados a la máquina virtual pero siempre hay que tener en cuenta que los recursos que prestemos al huésped o máquina virtual quedarán a disposición de esta y no del sistema anfitrión es decir, en el ejemplo anterior Windows tendrá menos recursos del PC a su disposición, justo los que ha prestado a su huésped la máquina virtual con Linux.

Por otra parte el huésped máquina virtual no podrá nunca exceder la capacidad o recursos que le sean prestados por el anfitrión, en nuestro ejemplo anterior la máquina virtual con Linux tendrá unos límites de un núcleo del procesador, 2 gigas de memoria RAM y 128 MB de memoria de vídeo y nunca podrá por muchos recursos que le sobren anfitrión superar los que le han sido asignados en su configuración.

Otro punto a tener en cuenta es que si otorgamos un porcentaje elevado de recursos al huésped, corremos el riesgo de que la máquina Real o anfitrión quedé conlapzada ya que le será imposible correr holgadamente su propio sistema operativo qué es la base de todo sistema en ejecución.

<img src="images/02-12.png">

Ya es hora de conocer al protagonista VirtualBox, VirtualBox es una aplicación desarrollada por la compañía Oracle para crear y gestionar máquinas virtuales. 

<img src="images/02-13.png">

Disponible para sistemas operativos Windows, OSx, Linux y Solaris y es capaz de hospedar con seguridad múltitud de sistemas operativos diferentes. VirtualBox se distribuye de forma gratuita con una licencia OpenSource pero por otra parte el Extensión Pack que dota la aplicación de características adicionales como el soporte para USB, RDP, IPX aunque también se distribuye de forma gratuita no tienen licencia Open Source.

En una clase posterior descargaremos la aplicación y le instalaremos en nuestro equipo para poder trabajar con ella es importante tener claros los conceptos que hemos visto en esta clase, por ello en caso de ser necesario si no te ha quedado claro algo de lo que hemos visto aquí, no dudes en tomar de nuevo esta clase, cuántas veces sean necesarias y así afianzar esos conceptos clave que nos servirán para el resto del curso.

<img src="images/02-14.png">

## 03 Ventajas e inconvenientes de las máquinas virtuales 04:24 min

<img src="images/03-01.png">

<img src="images/03-02.png">

Aunque el uso de máquinas virtuales puede parecer un escenario idílico.

<img src="images/03-03.png">

En realidad tiene sus puntos a favor y sus puntos en contra conocer tanto unos como otros es lo que vamos a hacer en esta clase, como la anterior se trata de una clase de corte teórico pero fundamental, así que te pido un pequeño esfuerzo para comprender los conceptos que vamos a tratar en esta clase, que sean aplicables y habrá que tener en cuenta para el resto del curso.

Primero de todo que veamos cuáles son las características ventajosas del uso de máquinas virtuales.

<img src="images/03-04.png">

Crear una máquina virtual es un proceso muy sencillo puede llevarnos tan solo unos pocos segundos, una reducción de tiempo que es abismal si la comparamos por ejemplo con el tiempo que nos llevaría montar un equipo real con hardware real.

<img src="images/03-05.png">

El aislamiento implica que un fallo en una máquina virtual en ejecución no afecta para nada a otra u otras máquinas virtuales que podían estar ejecutándose en ese mismo momento.

<img src="images/03-06.png">

Es decir si no máquina virtual se nos queda colgada, el resto de máquinas virtuales que podíamos tener en marcha en ese mismo momento seguirá funcionando como si no hubiera pasado nada.

<img src="images/03-07.png">

Las máquinas virtuales tienen la capacidad de modificar sus propiedades y su configuración de forma muy sencilla, esta flexibilidad nos permite por ejemplo aumentar la memoria RAM asignada a una máquina virtual cuando tengamos necesidad de ello con la facilidad de solo cambiar un parámetro en su configuración.

<img src="images/03-08.png">

Al tratarse de máquinas virtuales independientes cada una de ellas tiene sus propios usuarios, claves y métodos de acceso que igualmente son independientes.

<img src="images/03-09.png">

Las máquinas virtuales suelen definirse en muy pocos ficheros, unos que visualizan los sistemas de almacenamiento como los discos duros y otros que contienen la configuración de esas máquinas, aseguran los datos o transportar los de un anfitrión a otro es tan sencillo como hacer copias de estos ficheros.

<img src="images/03-10.png">

En nuestro caso que estamos dedicando este curso a VirtualBox en particular también existen un par de ventajas destacables de esta aplicación, la primera de ellas es que VirtualBox es un software que se distribuye de forma gratuita, es tan sencillo y barato cómo ir al sitio web oficial de VirtualBox, descargarnos la versión que corresponda a nuestro sistema operativo e instalarla y por cierto esto es lo que haremos en la siguiente clase. L aplicación VirtualBox está disponible para un buen número de sistemas operativos diferentes desde Windows, pasando por Mac OS X o Linux entre otros, ejemplos prácticos tanto podríamos ejecutar limos dentro de Windows como debes ejecutar Windows dentro de Linux y este es solo un ejemplo de los múltiples escenarios que podemos plantearnos.

<img src="images/03-11.png">

Hasta aquí todo han sido ventajas, ahora veamos los inconvenientes que conlleva el uso de máquinas virtuales, la lista de desventajas que conlleva el uso de máquinas virtuales se reduce básicamente a un punto y no poco importante las máquinas virtuales consumen muchos recursos del anfitrión.

<img src="images/03-12.png">

Un ejemplo si tenemos un PC con 4 gigas de memoria RAM y creamos una máquina virtual con 1,5 gb de ram. 

<img src="images/03-13.png">

El sistema operativo anfitrión pasará a disponer de solo 2,5 GB de memoria RAM para sí mismo, con la bajada que eso supone en el rendimiento general del sistema, por eso debemos ser siempre cuidadosos con este punto y asignar recursos a nuestras máquinas virtuales en su justa medida, según las necesidades y según lo que nos permite el propio anfitrión.

<img src="images/03-14.png">

Como hemos visto no todo es perfecto en el mundo de las máquinas virtuales tenemos puntos a favor pero también tenemos puntos en contra, lo importante de todo esto es conocer estos puntos y saber cuándo y en qué condiciones nos interesa utilizar una máquina virtual y de qué forma hacerlo, es decir saber configurar nuestra máquina virtual para que conmigo en armonía con su anfitrión y sobre todo no te asustes por tanta teoría la siguiente clase ya será de corte práctico empezando por la instalación de VirtualBox










