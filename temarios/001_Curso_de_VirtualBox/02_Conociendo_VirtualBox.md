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

# 04 Instalación de VirtualBox 06:16

[VirtualBox](https://www.virtualbox.org/)

[Installing Oracle VM VirtualBox and Extension Packs](https://www.virtualbox.org/manual/ch01.html#intro-installing)

, hasta ahora hemos estado viendo conceptos teóricos básicos en torno a las máquinas virtuales que son y qué ventajas e inconvenientes presentan también hemos conocido de pasada al protagonista de este curso VirtualBox pero es ahora en esta clase cuando vamos a conocerlo de primera mano vamos a dedicar la por completo a la instalación de VirtualBox en nuestro equipo para así poder empezar a trabajar con esta aplicación en casas posteriores descargar VirtualBox abrimos una ventana del navegador y vamos a la dirección web virtualbox.org qué es la el sitio web oficial de VirtualBox una vez allí vamos a session download descargas y descargamos la última versión estable que en este caso en las 5.02 en mi casa o fiesta doble no máquina con Windows entonces el hijo está haciendo aquí como hemos es la misma versión tanto para 32 como para 64bits y que pinchamos aquí y guardamos el archivo una vez descargado el instalador lo ejecutamos y nos saldrá un wither como este vamos a siguiente y bueno aquí elegimos qué módulos queremos instalar por defecto vienen todos y así lo voy a dejar porque cuando esté en la aplicación de Virtual Box soporte para USB soporte para redes etcétera luego aquí el destino te envía dejaré que viene por defecto siguiente siguiente y bueno aquí nos avisa que al instalar el soporte para redes podemos ser desconectados temporalmente de la red creemos que hacer con esta oración le decimos que sí instalar y una vez instalada la aplicación la abrimos para echarle un primer vistazo y aquí tenemos la pantalla principal y VirtualBox aquí a la izquierda en este recuadro en blanco y aparecerá en cada una de las máquinas que vayamos creando y a la derecha aparecerán las propiedades de esas máquinas tenemos aquí un botón para crear una nueva máquina y diferentes opciones ayuda opciones relacionadas con las máquinas y aquí tenemos esta opción de preferencias qué es lo que vamos ahora potencial de la aplicación en general bien vamos a ampliarlo un poco para verlo mejor me arrime la pestaña General podemos cambiar lo que es la carpeta predeterminada para las máquinas virtuales si tenemos por ejemplo un segundo disco duro con más espacio pues podemos indicar aquí una carpeta en ese segundo disco duro y dejar libre por ejemplo no me hace aquí vemos los dirigentes atasco en el teclado tanto en la aplicación como en la máquina virtual la opción de comprobar actualizaciones cada X tiempo para que la aplicación comprueba a través de Internet si hay versiones nuevas y actualice o no el idioma me me apuesto a español porque es el idioma que tiene sistema operativo por defecto entonces lo ha cogido también por defecto aunque posteriormente ya ves que se puede cambiar desde aquí indicar un tamaño de pantalla máximo para lo que es el huésped si queremos que no sobrepase esa dimensiones en mi caso yo lo he dejado automático y tal y como viene porque me puede interesar cambiar ese tamaño en cualquier momento opciones de red extensiones son diferentes extensiones que podemos instalar a VirtualBox para darle mayor capacidad y opciones de proxy si estamos conectados a Internet a través de un proxy pues lo haríamos aquí una vez que hemos instalado VirtualBox una de las cosas necesarias que debemos instalar es el extensión pack extensión pack se distribuye de forma gratuita a través de la página web oficial de Virtual Box y bueno no va a dar soporte para dispositivos USB 2.0 RDP IPX entre otras cosas también que podéis ver dentro de la documentación oficial de la página web son varias las cosas que nos proporciona y es muy muy recomendable instalarlo este extensión pack sea instalar dentro de las extensiones hemos visto anteriormente que había una opción de la aplicación en VirtualBox para instalar extensiones puestas tensión para que es precisamente eso una extensión que se instala en la aplicación y qué bueno por los da una serie de características adicionales y como veis C&A la versión del extensión pack tengo incidir con la pensión de la aplicación este caso vamos a descargar la extensión para VirtualBox 502 ahora hemos estado viendo conceptos teóricos básicos en la máquina virtual es que soy y qué ventajas e inconvenientes presenta también hemos conocido de pasada al que está bonita de este curso Virtual Box pero esa hora en esta clase cuando vamos a conocer los de primera mano le damos aquí ya nos dice que está extensión pack sirven para todas las plataformas es independiente del sistema operativo del anfitrión vamos aquí y le vamos a dejar que lo abra directamente con VirtualBox manager decir que lo haga la propia aplicación 9 descargado una vez descargado no se lanza la pregunta se abre directamente VirtualBox y nos lanza la pregunta queremos instalar extensión pack tenemos a instalar y bueno nos viene aquí una licencia que debemos de leer y de aceptar para VirtualBox vamos a comprobarlo nos vamos aquí archivo preferencias extensiones y hemos que aquí está instalado Oracle VM VirtualBox extensión pack para versión 502 y con esto ya tenemos instalado VirtualBox en nuestro equipo estamos preparados para la siguiente clase la cual dedicaremos a crear nuestra primera máquina virtual

<img src="images/04-01.png">
<img src="images/04-02.png">
<img src="images/04-03.png">
<img src="images/04-04.png">
<img src="images/04-05.png">
<img src="images/04-06.png">
<img src="images/04-07.png">
<img src="images/04-08.png">
<img src="images/04-09.png">
###10
<img src="images/04-10.png">
<img src="images/04-11.png">
<img src="images/04-12.png">
<img src="images/04-13.png">
<img src="images/04-14.png">
<img src="images/04-15.png">
<img src="images/04-16.png">
<img src="images/04-17.png">
<img src="images/04-18.png">
<img src="images/04-19.png">
###20
<img src="images/04-20.png">
<img src="images/04-21.png">
<img src="images/04-22.png">
<img src="images/04-23.png">
<img src="images/04-24.png">
<img src="images/04-25.png">
<img src="images/04-26.png">
<img src="images/04-27.png">
<img src="images/04-28.png">
<img src="images/04-29.png">
###30
<img src="images/04-30.png">
<img src="images/04-31.png">
<img src="images/04-32.png">
<img src="images/04-33.png">
<img src="images/04-34.png">
<img src="images/04-35.png">
<img src="images/04-36.png">
<img src="images/04-37.png">
<img src="images/04-38.png">
<img src="images/04-39.png">
<img src="images/04-40.png">
<img src="images/04-41.png">








