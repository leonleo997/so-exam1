# PARCIAL 1   
**Nombre:** Yesid Leonardo López  
**Código:** A00056408 
  
# Desarrollo Parcial  

## A. Validación del ISO de Debian 9  

**1.** Descargar la imagen [Debian 9](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-9.4.0-amd64-netinst.iso).  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/Debian9.PNG)  
  
**2.** Descargar e instalar aplicación para comprobar [Checksum](https://download.cnet.com/MD5-SHA-Checksum-Utility/3001-2092_4-10911445.html) que se encarga de comprobar que la imagen se haya bajado correctamente.    
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/checksum.PNG)  
  
**3.** Abrir la aplicación.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/interfazCheck.PNG)  
  
**4.** Damos click en browse y seleccionamos el ISO del Debian descargado.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/interfazCheckIsoCargada.PNG)  
  
**5.** Vamos a [este enlace](https://cdimage.debian.org/debian-cd/9.4.0/amd64/bt-cd/) que contiene los archivos MD5, SHA-1, SHA-256 y SHA-512 que servirán para verificar si la descarga se ha hecho correctamente. 
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/validarChecksum.PNG)  
  
En este caso damos clic en el archivo SHA512SUMS y copiamos el que corresponde a nuestra descarga. Es decir, la primera línea.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/Sha512.PNG) 

**6.** Después pegamos y damos click en la opción de verify y debe salir el mensaje que se muestra en la siguiente imagen. 
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/checksumExitoso.PNG) 
  
Con esta verificación podemos proceder a cargar la imagen en la máquina virtual.  

## B. Instalación de Debian 9 en VirtualBox  
**1.** Abrimos VirtualBox y Creamos una nueva maquina virtual Tipo Linux que tenga una versión de Debian de 64-bits con el tamaño de memoria y el tipo de disco duro que desee.  
**2.** Vamos a las configuraciones de la máquina creada y damos click en `Almacenamiento`.  
**3.** En el panel de `Dispositivos de almacenamiento`, nos ubicamos en `Controlador`. Damos click en el ícono de `Agregar una unidad óptica` y seleccionamos el disco; En este caso cargamos la imagen de Debian que verificamos anteriormente.  
**4.** Seleccionamos nuestra máquina creada y damos click en `Iniciar`.  
**5.** Una vez iniciada la máquina veremos la interfaz para la instalación. Damos click en `Graphical install`.   
**6.** Seleccionamos el idioma, la ubicación y la configuración de teclado deseada. Posteriormente, se procederá a instalar los componentes y a configurar la red.  
**7.** Asignamos un nombre a la Máquina deseado. Por ejemplo, Debian9.  
**8.** En este paso debes indicar un nombre para el equipo e identificar el dominio al que quieres que pertenezca este equipo, si no está claro solo escribe local.  
**9.** Después asignamos una contraseña para el super usuario o root. Esta contraseña es muy importante pues permitirá configurar elementos clave del sistema, así como instalar nuevos paquetes de software entre otras. En este caso será `root`.  
**10.** Escribimos el nombre completo del usuario y el nombre de usuario. Este usuario nuevo es diferente al root debido a que es con el que iniciaremos sesión normalmente. En ambos casos se llamará `VII`.  
**11.** Asignamos una contraseña para el usuario anterior. En este caso será el mismo nombre de usuario, es decir, `vii`.  
**12.** Configuramos el reloj correspondiente a nuestra zona horaria.  
**13.** En la siguiente pantalla seleccionamos entre las opciones `Guiado - utilizar todo el disco`. Esta opción destruirá toda la información del disco en donde se instale.  
**14.** Luego indicamos el disco en el que se va a instalar Debian 9.  
**15.** Indicamos el esquema de particionado mas sencillo y práctico, es decir, `Todos los ficheros en una partición`. 
**16.** Seleccionamos `Finalizar el particionado y escribir los cambios en el disco` damos en continuar y seleccionamos `Sí` al preguntarnos si deseamos escribir los cambios en los discos. En este punto iniciará a instalar el sistema base entre otros.  
**17.** Luego nos preguntará si deseamos analizar otro CD o DVD, aquí seleccionamos no debido a que se hará la instalación por red.  
**18.** Seleccionamos la ubicación geografica para descargar los paquetes de software, trataremos de elegir una ubicación cercana donde haya una transferencia de archivos rápida. En este caso seleccionaremos a Colombia.
**19.** Seleccionamos un servidor. En este caso `de.debian.org`.  
**20.** Seleccionamos la configuración del proxy. En este caso lo dejamos en blanco.  
**21.** En la siguiente pantalla se puede participar en el envío de estadísticas de uso paquetes, esto es una retro alimentación para el equipo de Debian. Se elige lo que se crea conveniente. En este caso seleccionaré `No`.  
**22.** Seleccionamos los paquetes a instalar. En este caso eligiremos: `GNOME`, `Servidor de impresión`, `SSH server` y `Utilidades estándar del sistema`.  
**23.** Esperamos a que se descarguen e instalen los paquetes seleccionados.  
**24.** Seleccionamos `Sí` a la preguntarnos si deseamos instalar el cargador de arranque GRUB en el registro principal de arranque.  
**25.** Seleccionamos `/dev/sda`.  
**26.** Esperamos a que finalice la instalación y deberá salir algo como la siguiente imagen.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/instalacionDebian.PNG)  
### Revisando información del Sistema Operativo
Ahora revisaremos la información del sistema operativo instalado. Para esto digitamos el comando `uname` como se muestra a continuación:  
```console
user@Debian:~$ uname
```
Obteniendo la siguiente información:  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/infoSO.PNG)  

Esta imagen nos dice que el sistema posee lo siguiente:  
| Nombre| valor|
| ----- | ---- |
| Tipo de kernel | linux |

Tipo | Valor  
--- | ---  
Tipo de kernel | Linux  
Arquitectura del procesador | x86_64  
Nombre para el equipo | DebianRoldan  







**1.**  
**2.**  
**3.**  
**4.**  
**5.**  
**6.**  
**7.**  
**8.**  
**9.**  
**10.**  
**11.**  
**12.**  
**13.**  
**14.**  
**15.**  
**16.**  



 
