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
**1.** Abrimos VirtualBox y Creamos una nueva maquina virtual Tipo Linux que tenga una versión de Debian de 64-bits con el tamaño de memorio y el tipo de disco duro que desee.  
**2.** Vamos a las configuraciones de la máquina creada, damos click en `Almacenamiento`.  
**3.** En el panel de `Dispositivos de almacenamiento`, nos ubicamos en `Controlador`. Damos click en el ícono de `Agregar una unidad óptica` y seleccionamos el disco. En este caso la imagen de Debian que verificamos anteriormente.  
**4.** Seleccionamos nuestra máquina creada y damos click en `Iniciar`.  
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



 
