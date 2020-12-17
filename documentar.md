# EC2
#### Amazon Elastic Compute Cloud (Amazon EC2) es una parte central de la plataforma de cómputo en la nube de la empresa Amazon.com denominada Amazon Web Services (AWS). EC2 permite a los usuarios alquilar computadores virtuales en los cuales pueden ejecutar sus propias aplicaciones. Este tipo de servicio supone un cambio en el modelo informático al proporcionar capacidad informática con tamaño modificable en la nube, pagando por la capacidad utilizada. En lugar de comprar o alquilar un determinado procesador para utilizarlo varios meses o años, en EC2 se alquila la capacidad por horas

## Documentacióm
### Paso 1: Conectarse al servidor
Para crear un aestancia haremos click en "Lanzar entancia"


![Texto alternativo](/img/1.PNG)


Elegiremos en este caso Ubuntu 20 y "Select"


![Texto alternativo](/img/2.PNG)


Comprobaremos que todo este correcto


![Texto alternativo](/img/3.PNG)
![Texto alternativo](/img/4.PNG)


Cambiaremos el “size” a 30GB


![Texto alternativo](/img/5.PNG)

Next y launch


![Texto alternativo](/img/6.PNG)


Aquí crearemos una key para poder acceder después,elegiremos un nombre y lo descargamos


![Texto alternativo](/img/7.PNG)


Le daremos en a Launch Insatances


![Texto alternativo](/img/8.PNG)


Le daremos a View Intances para ver que nuestra instancia se ejecuta


![Texto alternativo](/img/9.PNG)


![Texto alternativo](/img/10.PNG)


Después haremos click sobre la estancia y daremos click en conectar



![Texto alternativo](/img/11.PNG)
![Texto alternativo](/img/12.PNG)
![Texto alternativo](/img/13.PNG)
![Texto alternativo](/img/14.PNG)
![Texto alternativo](/img/15.PNG)
![Texto alternativo](/img/16.PNG)
![Texto alternativo](/img/17.PNG)
![Texto alternativo](/img/18.PNG)



### Paso 2: Instalar Apache


![Texto alternativo](/img/19.PNG)
![Texto alternativo](/img/20.PNG)

#### Control WIZARD


![Texto alternativo](/img/21.PNG)
![Texto alternativo](/img/22.PNG)
![Texto alternativo](/img/23.PNG)
![Texto alternativo](/img/24.PNG)
![Texto alternativo](/img/25.PNG)
![Texto alternativo](/img/26.PNG)


### Paso 3: Instalar MySQL


![Texto alternativo](/img/27.PNG)
![Texto alternativo](/img/28.PNG)
![Texto alternativo](/img/29.PNG)
![Texto alternativo](/img/30.PNG)
![Texto alternativo](/img/31.PNG)
![Texto alternativo](/img/32.PNG)
![Texto alternativo](/img/33.PNG)
![Texto alternativo](/img/34.PNG)
![Texto alternativo](/img/35.PNG)

### Paso 4: Instalar PHP

![Texto alternativo](/img/36php1.PNG)
![Texto alternativo](/img/37.PNG)
![Texto alternativo](/img/38.PNG)
![Texto alternativo](/img/39.PNG)

### Paso 5: Instalar FTP

![Texto alternativo](/img/40.PNG)
![Texto alternativo](/img/41.PNG)
![Texto alternativo](/img/42.PNG)
![Texto alternativo](/img/43.PNG)
![Texto alternativo](/img/44.PNG)
![Texto alternativo](/img/45.PNG)
![Texto alternativo](/img/46.PNG)
![Texto alternativo](/img/47.PNG)



### Paso 6: IP Elastica


![Texto alternativo](/img/48.PNG)
![Texto alternativo](/img/49.PNG)
![Texto alternativo](/img/50.PNG)
![Texto alternativo](/img/51.PNG)


### Paso 7: DNS

-¿Qué es y para qué sirve el DNS?

 - El DNS es un conjunto de protocolos y servicios que permite a los usuarios utilizar nombres en vez de tener que recordar direcciones IP numéricas.

-Indica cuales son y para qué se usan los diferentes tipos de registros DNS.
- A = Dirección (address). Este registro se usa para traducir nombres de servidores de alojamiento a direcciones IPv4.

- AAAA = Dirección (address). Este registro se usa en IPv6 para traducir nombres de hosts a direcciones IPv6.

- CNAME = Nombre canónico (canonical Name). Se usa para crear nombres de servidores de alojamiento adicionales, o alias, para los servidores de alojamiento de un dominio. Es usado cuando se están corriendo múltiples servicios (como FTP y servidor web) en un servidor con una sola dirección IP. Cada servicio tiene su propia entrada de DNS (como ftp.ejemplo.com. y www.ejemplo.com.). Esto también es usado cuando corres múltiples servidores HTTP, con diferentes nombres, sobre el mismo host. Se escribe primero el alias y luego el nombre real. Ej. Ejemplo1 IN CNAME ejemplo2

- SRV = Service record (SRV record).

- TXT = Un registro TXT es un tipo de registro DNS que proporciona información de texto a fuentes externas a tu dominio.El texto puede ser lenguaje legible por máquina o por el ser humano, y se puede utilizar para diversos fines.

-Imagen de los registros DNS de tu sitio en Guebs y explicación de los registros de tu dominio grupoX.zerbitzaria.net.
- ![Texto alternativo](/img/52.PNG)

### Paso 7: DNS 2

-¿Cuántos servidores DNS existen?
- En la actualidad existen un total de 13 servidores raíz DNS, y están nombrados por letras de la “A” a la “M”. Estos servidores, tienen una dirección IPv4 y una dirección IPv6.

-¿Cuántas redirecciones DNS son posibles?
- TLD y Root Server

-¿Qué son los servidores DNS Raíz?
- El directorio raíz de un dominio es la carpeta a la que apunta el dominio, que contiene los ficheros y carpetas de la web que carga dicho dominio. En cpanel, el dominio principal apunta a la carpeta public_html de tu cuenta. Si quieres puedes apuntar el dominio principal a otra carpeta



-¿Para qué montar un servidor si simplemente escribiendo en un fichero la relación IP/Nombre el sistema ya funcionaría?

- Cada equipo conectado directamente a Internet tiene al menos una dirección IP específica. Sin embargo, los usuarios no desean trabajar con direcciones numéricas

-Según lo expuesto, y si en tu configuración de red del sistema operativo solamente posees un servidor DNS, entonces: ¿cuál sería el proceso para encontrar la IP de la dirección web: http://www.debian.org/distrib/netinst?
- Nuestro equipo verá que no conoce la IP a la que debe conectarse, así que preguntará a un servidor DNS que tenga configurado.
- A este servidor DNS le llegará una petición: “Oye, ¿a qué IP resuelve el dominio miweb.es?”.  Pero tampoco conoce la respuesta, así que pregunta a uno de sus propios servidores DNS.
- Esto puede ocurrir varias veces hasta que al final la pregunta llega a un Root Server.
- El Root Server contestará “Yo no sé a qué IP resuelve miweb.es, pero puedo decirte qué servidor DNS lo sabe.” Entonces dirigirá la consulta a un servidor DNS del dominio padre, o TLD.
- El servidor del dominio padre de nuevo contestará la consulta, indicando cuáles son los servidores DNS autoritativos para el dominio.
- La petición llega a estos dos servidores DNS, es contestada.
- Por último, tu ordenador ya tiene su respuesta y ya sabe a qué IP resuelve el dominio. Hace una conexión a ella, pide la página web y te la enseña.




-¿Es posible si dispones de una conexión a Internet con IP dinámica ofrecer servicios en Internet? Es decir, si quieres ofrecer los servicios SND, no dispones de IP estática, esto es, cada vez que te conectas a Internet tu IP, aunque a veces sea la misma, no siempre es la misma. 



-¿Qué es ICANN?
- La comunidad mundial de Internet se empeña en la promoción de la estabilidad e integridad de Internet.