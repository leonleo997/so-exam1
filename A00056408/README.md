# Primer Parcial  
**Nombre:** Yesid Leonardo López  
**Código:** A00056408  
**URL repositorio:** https://github.com/leonleo997/so-exam1.git  

**Tabla de Contenido**

- [PARCIAL 1](#parcial-1)
- [Desarrollo Parcial](#desarrollo-parcial)
  - [A. Validación del ISO de Debian 9](#a-validaci%C3%B3n-del-iso-de-debian-9)
  - [B. Instalación de Debian 9 en VirtualBox](#b-instalaci%C3%B3n-de-debian-9-en-virtualbox)
    - [Revisando información del Sistema Operativo](#revisando-informaci%C3%B3n-del-sistema-operativo)
  - [C. Accediendo a través de Putty](#c-accediendo-a-trav%C3%A9s-de-putty)
  - [D. Instalando git y tig](#d-instalando-git-y-tig)
  - [E. Exportando Máquina Virtual](#e-exportando-m%C3%A1quina-virtual)
  - [F. Importando Máquina Virtual](#f-importando-m%C3%A1quina-virtual)
  - [G. Comparación entre Debian 9 y CentOS7](#g-comparaci%C3%B3n-entre-debian-9-y-centos7)

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
Ahora revisaremos la información del sistema operativo instalado. Para esto digitamos el comando `uname -a` como se muestra a continuación:  
```console
user@Debian:~$ uname -a
```
Obteniendo la siguiente información:  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/infoSO.PNG)  

Esta imagen nos dice que el sistema posee lo siguiente:  

Tipo | Valor  
--- | ---  
Tipo de kernel | Linux  
Arquitectura del procesador | x86_64  
Nombre para el equipo | DebianRoldan  
Sistema operativo | GNU/LINUX  
Info kernel | 4.9.0-6-amd64  
Fecha publicación kernel | SMP Debian 4.9.82-1+deb9u3 (2018-03-02)  

## C. Accediendo a través de Putty  

Usamos el siguiente comando  
```console
user@Debian:~$ ip a
```
Obteniendo como resultado la siguiente imagen, en ésta observamos que tiene dos interfaces, `lo` y `enp0s3`.   
 ![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/ipa.PNG)  
Sin embarbo, para poder conectar a Putty primero debemos adicionar un adaptador red más. Para esto:  
**1.** Apagamos la mána virtual y abrimos sus configuraciones. Vamos a la opción de `Red`>`Adaptador 2` y habilitamos el adaptador de Red.  
**2.** En la opción de `conectado a` seleccionamos `Adaptador puente` eligiendo como `Nombre` el que nos corresponda. En este caso será el Wireless.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/adaptadorPuente.PNG)  
**3.** Iniciamos de nuevo la máquina y volvemos a usar el comando  
```console
user@Debian:~$ ip a
```
Obteniendo una interfaz adicional llamada `enp0s8` que será la que usaremos para acceder mediante putty.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/ipa2.PNG)  
**4.** Abrimos Putty.
**5.** Ingresamos como `host name` la dirección ip que muestra la interfaz `enp0s8` que es `192.168.0.12`, el `puerto` será el `22` y el `connection type` será tipo `ssh`. Después damos click en `Open`.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/configputty.PNG)  
**6.** Al iniciar nos pedirá el nombre del login y la contraseña. El nombre será el usuario que configuramos al intalar Debian y la contraseña es la que se le asignó. En este caso vii y vii.  
```console
login as: vii
vii@192.168.0.12´s password: vii
```
Desplegandose lo que se muestra a continuación:  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/inicioPutty.PNG)  

## D. Instalando git y tig  
Ahora intentaremos instalar git y tig.  
Primero instalaremos `git`. Para esto:  
**1.** Ingresamos como root  
```console
user@Debian:~$ su
```
**2.** Ingresamos la contraseña que asignamos al instalar debian, es decir `root`.
Escribimos el siguiente comando para instalarlo  
```console
root@Debian:~$ apt-get install git -y
``` 
**3.** Verificamos que esté instalado con el siguiente comando:  
```console
root@Debian:~$ git -version
``` 
veremos el siguiente resultado:  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/gitVersion.PNG)  

Ahora instalaremos tig  
Estando como root, escribimos el siguiente comando para instalarlo:  
```console
root@Debian:~$ apt-get install tig -y
``` 
**3.** Verificamos que esté instalado con el siguiente comando:  
```console
root@Debian:~$ tig -version
``` 
veremos el siguiente resultado:  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/tigVersion.PNG)  
 
Ahora usaremos git para bajar este repositorio, y usaremos tig para ver el historial de commits hechos en el repositorio. para esto hacemos:  
```console
root@Debian:~$ git clone https://github.com/leonleo997/so-exam1.git
``` 
Después nos movemos a la carpeta `so-exam1` usando el siguiente comando  
```console
root@Debian:~$ cd so-exam1/
``` 
Estando dentro de la carpeta del repositorio ejecutamos el siguiente comando para ver el historial de commits hecho  
```console
root@Debian:~$ tig
``` 
y obtendremos algo como se ve a continuación:  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/tig.PNG)  
 
## E. Exportando Máquina Virtual  
Para exportar la máquina virtual haremos lo siguiente, teniendo la máquina virtual apagada:  
**1.** Damos click en la viñeta de `Archivo` y seleccionamos `Exportar servicio virtualizado`.   
**2.** Seleccionamos la máquina Dedian como se ve a continuación:  
 ![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/exportarDebian.PNG)  
**3.** Elegimos la ubicación en donde quedará el archivo y damos siguiente.   
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/exportarDebian2.PNG)  
**4.** Damos click en `exportar` y experamos a que se exporte la máquina.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/exportarFinal.PNG)  

## F. Importando Máquina Virtual  
Para importar la máquina virtual haremos lo siguiente:  
**1.** Damos click en la viñeta de `Archivo` y seleccionamos `Importar servicio virtualizado`.   
**2.** Seleccionamos la máquina Dedian exportada como se ve a continuación:  
 ![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/importarDebian.PNG)    
**3.** Damos click en `Importar` y experamos a que se importe la máquina.  
![alt text](https://github.com/leonleo997/so-exam1/blob/master/A00056408/Images/importarFinal.PNG)  

## G. Comparación entre Debian 9 y CentOS7  
A continuación se presenta un cuadro comparativo entre estos dos sistemas operativos:  

Característica | Debian 9 | CentOS7  
--- | --- | ---  
Permite instalar interfaz gráfica | Sí | No  
Forma en que hace las modificaciones | Backports | EPEL  
Package Manager | 'apt-get' y 'aptitude' | yum  
Paquetes | Posee más respecto a CentOS | Posee menos respecto a Debian  
Fácil de instalar | No | Sí  
Tamaño de ISO | 297 MB | 4.2 GB  
Tipo distribución | Debian | RedHat  
Rapidez | Menor | Mayor  
Actualizaciones | Mayores | Menores  
Confiabilidad | Mayor | Menor  
