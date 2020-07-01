# Sección 2: Conociendo VirtualBox 26 min

   * 02 VirtualBox y las máquinas virtuales 04:50 min
   * 03 Ventajas e inconvenientes de las máquinas virtuales 04:24 min
   * 04 Instalación de VirtualBox 06:16
   * 05 Nuestra primera máquina virtual 09:07
   * Preguntas sobre máquinas virtuales y VirtualBox 8 preguntas
   * Resumen 1 páginas



## 02 VirtualBox y las máquinas virtuales

Vamos a aprender lo que son las máquinas virtuales y sus características más importantes así como una aplicación para gestionar las de la que es objeto este curso VirtualBox que será nuestro software de virtualización para llevar toda esta teoría a la práctica la siguiente son puramente teóricas pero fundamentales que no lo que pongas mucha atención porque los conceptos que vamos a tratar ahora son fundamentales para adentrarnos con buen pie y empezar a comprender el mundo de la virtualización lo primero y más básico sería preguntarnos qué es una máquina virtual según la Wikipedia una máquina virtual se define como un software que simula una computadora y puede ejecutar programas como si fuese una computadora real o dicho de otra forma sentada una aplicación que simula por software una computadora y que en la práctica tiene las mismas capacidades que una computadora real en adelante para referirnos a la máquina real y a la máquina virtual utilizaremos la nomenclatura anfitrión y huésped la máquina real o física toma el nombre de anfitrión mientras que la máquina virtual toma el nombre de huésped como ves los nombres les vienen al pelo virtual como es evidente esta máquina virtual o huésped tomará prestado sus recursos del anfitrión o máquina real veámoslo con un ejemplo pongamos que tenemos una máquina real con 4 gigas de memoria RAM se ejecutamos en ella una máquina virtual y le asignamos un giga de ram esta última lo tomará prestado te los 4 gigas con los que cuenta la máquina real de Aqualia son dispondrá de 3 GB para ejecutarse en Windows y huésped la máquina real o física toma el nombre de anfitrión mientras que la máquina virtual toma el nombre de huésped como ves los nombres les vienen al pelo cómo es evidente esta máquina virtual o huésped tomará prestado sus recursos del anfitrión o máquina real un ejemplo pongamos que tenemos una máquina real con 4 gigas de memoria RAM ejecutamos en ella una máquina virtual y le asignamos un giga de ram y esta última lo tomará prestado te los 4 gigas con los que cuenta la máquina real la cual ya solo dispondrá de 3 GB para ejecutarse ejemplo imaginemos que un usuario tiene un PC con Windows y este PC tiene un procesador de cuatro núcleos 8 GB de memoria RAM y un giga de memoria gráfica podemos definir una máquina virtual con Linux para que se ejecute dentro de Windows asignándole un núcleo del procesador 2 gigas de ram 128MB de memoria de vídeo como antes los recursos que toma el huésped ya no estarán disponibles para la afición evidentemente podemos ser más generosos con los recursos asignados a la máquina virtual pero siempre hay que tener en cuenta que los recursos que prestemos al huésped o máquina virtual quedarán a disposición de esta Inma del sistema ficción he decidido un ejemplo anterior Windows tendrán menos recursos del PC a su disposición justo los que ha prestado a su huésped la máquina virtual con Linux por otra parte el huésped máquina virtual no podrá nunca exceder la capacidad o recursos que le sean prestados por el anfitrión ejemplo anterior la máquina virtual con Linux tendrá unos límites de un núcleo del procesador 2 gigas de memoria RAM y 128 MB de memoria de vídeo y nunca podrá por muchos recursos que le sobren anfitrión superar los que le han sido asignados en su configuración 50 es que tengamos un porcentaje elevado de recursos a huésped corremos el riesgo de que la Marina Real o anfitrión quedé con lazada ya que le será imposible correr holgadamente su propio sistema operativo qué es la base de todo sistema en ejecución VirtualBox es una aplicación desarrollada por la compañía Oracle para crear y gestionar máquinas virtuales disponible para sistemas operativos Windows Linux y Solaris y es capaz de quedar con seguridad múltiples sistemas operativos diferentes VirtualBox se distribuye de forma gratuita con una licencia openshop pero por otra parte el extensión pack que no está la aplicación de características adicionales como el soporte para USB RDP IPX aunque también se distribuye de forma gratuita no tienen licencia Open Source y una clase posterior descargaremos la aplicación y le instalaremos en nuestro equipo para poder trabajar con ella es importante tener claros los conceptos que hemos visto en esta clase por ello en caso de ser necesario si no te ha quedado claro algo de lo que hemos visto aquí donde siempre tomar de nuevo esta clase cuántas veces sean necesarias y así hace alzar esos conceptos clave que nos servirán para el resto del curso


<img src="images/02-02.png">
<img src="images/02-03.png">
<img src="images/02-04.png">
<img src="images/02-05.png">
<img src="images/02-06.png">
<img src="images/02-07.png">
<img src="images/02-08.png">
<img src="images/02-09.png">
<img src="images/02-10.png">
<img src="images/02-11.png">
<img src="images/02-12.png">
<img src="images/02-13.png">
<img src="images/02-14.png">
