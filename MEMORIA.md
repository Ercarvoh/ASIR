# Memoria de servicio de streaming y de audio

<p align="center">
  <img src="imagen/foto-servicios.png" alt="Audio y Video"><br>
  <b>Sergio Martínez Guillem 2ASIR</b>
</p>


# Índice
- [Servicio de audio Icecast2](#Servicio-de-audio)
  - [Introducción al servicio](#Introducción)
- [Servicio de streaming FFmpeg](#Servicio-de-video)
  - [Introducción al servicio](#Introducción)
  - [Instalación del servicio FFmpeg](#Instalación-FFmpeg)
  - [Que metadatos tiene nuestro fichero ](#Metadatos)
  - [Cambio de contenedor de mp4 a mkv](#Contenedores)
  - [Cambio de codecs h264 y h265](#Codecs)
- [Ejercicios](#Simulación-streaming)
  - [Ejercicio1](#Ejercicio1)
  - [Ejercicio2](#Ejercicio2)
- [Anexo (imagenes)](#Anexo)

# Servicio de Audio y de Video

## Servicio-de-video

### Introducción
El servicio de video mediante FFmpeg es una solución de procesamiento multimedia que permite la captura, codificación y transmisión de contenido visual en tiempo real a través de una red. 
Esta herramienta destaca por su capacidad para gestionar diversos formatos y protocolos, garantizando una entrega eficiente de streaming adaptada a diferentes dispositivos y anchos de banda.
Para la tarea lo que tendremos que hacer es descargarnos un video el cual luego vamos a mirar los metadatos haremos cambios en el codec y le cambiaremos el contenedor a otro diferente.

### Instalación-FFmeg

Lo primero que tenemos que hacer para instalar sera abrir una terminal y dentro de esta ejecutar el siguiente comando el cual realizara toda la instalación para posteriormente realizar los siguiente pasos.

```
apt-get install ffmpeg
```

### Metadatos

Cuando este instalado el siguiente paso a realizar sera descargarnos el video el cual esta en aules y una vez lo tengamos descargado y nos encontremos en la ruta donde se encuentra este ejecutaremos el siguiente comando.

```
ffprobe -v error -show_streams big-buck-bunny-1080p-30sec.mp4
```

Cuando se haya ejecutado este comando nos mostrara los metadatos de este video los cuales se pueden observar aqui [Imágen](#Imagen-metadatos) 

### Contenedores 

Ahora lo que tendremos que hacer sera realizar el cambio de contenedor de mp4 el cual es el que tiene el archivo cuando lo descargamos a mkv mediante el siguiente comando.

```
ffmpeg -i big-buck-bunny.mp4 -c:v copy -c:a copy big-buck-bunny.mkv
```
Una vez se ejecute el comando ya tendremos un nuevo archivo el cual tiene el nuevo contenedor en esta imagen se puede observar el funcionamiento del comando [Imágen](#Imagen-contenedor)

Para comprobar el tamaño de los dos archivos he dado click derecho en cada uno he ido a propiedades y he comparado el tamaño y he podido observar que no varia practicamente en nada el peso de cada uno [Imágen](#Imagen-con-tamaño)

Al ejecutar el comando para cambiarle el comando he podido observar que no hace un uso grande de los recursos de nuestro ordenador y tampoco se demora mucho en cambiar el contenedor ya que basicamente este lo que realiza es copiar toda la información que tenia el archivo del mp4 al nuevo archivo que tiene como extension mkv, esto quiere decir que solo tiene que volver a escribir la información en el nuevo archivo por esto no varia el tamaño de estos.

### Codecs
Lo primero que vamos ha realizar es la creación de un archivo en h.264 el cual tendra un bitrate de 2Mbps, para esto utilizaremos el video que hemos descargado previamente de aules, todo se hara mediante el siguiente comando

```
ffmpeg -i big-buck-bunny.mp4 -c:v libx264 -b:v 2M -c:a copy big-buck-bunny-h264-2mbps.mp4
```
Una vez se ejecute el comando se nos creara un archivo con las caracteristicas que hemos especificado en el anterior comando, aqui adjunto una captura para que se pueda observar que se ha realizado correctamente [Imágen](#Imagen-h264)

Ahora cuando tengamos ya hecho el archivo h.264 lo que tendremos que hacer es lo mismo pero cambiando el h.264 por h265 como se muestra en el siguiente comando

```
ffmpeg -i big-buck-bunny.mp4 -c:v libx265 -b:v 2M -c:a copy big-buck-bunny-h265-2mbps.mp4
```
Ahora mostrare igual que con el h.264 que ha funcionado correctamente mediante la siguiente imagen [Imágen](#Imagen-h265)

Cuando realizamos la comprobación del funcionamiento de ambos archivos que hemos creado nos podemos dar cuenta que en ambos funcionan muy parecido pero la diferencia no se encuentra en la imagen sino en el rendimiento ya que el h265 suele pesar menos pero hace un uso mayor de la CPU asi que es recomendable si quieres reducir el uso de espacio en la maquina o el ancho de banda

Voy a adjuntar ahora una imagen para mostrar la diferencia de tamaño de los dos archivos uno con el h264 y el h265 ambos tienen el tamaño parecido [Imágen](#Imagen-cod-tamaño)


### Simulación-streaming

Low (móvil):
Resolución 240p
Bitrate: 400k
2. High (fibra):
Resolución: 1080p
Bitrate: 2Mbps

#### Pregunta 1:


**Almacenamiento: Si tu servidor tiene un disco de 500 GB, ¿cuántas horas de vídeo del perfil "HD" (2 Mbps) podrías alojar?**

-Como primero tenemos que pasar de 2Mbps a MB/s, tenemos que dividirlo entre 8, por lo tanto se nos quedaría en 0,25MB/s

**2Mbps / 8 = 0,25MB/s**

-1 hora es equivalente a 3600 segundos entonces, tenemos que hacer 0,25 MB/s x 3600 segundos y nos daria 900MB, como hay dos veces segundos, se elimina la s y equivale a 0.9GB

**0,25 MB/s × 3600 s = 900 MB, 900 MB ≈ 0,9 GB**

-Entonces, como el disco tiene de capacidad 500GB y cada hora ocupa 0,9GB del disco, habrá que dividir 500GB entre 0,9GB y nos daría aproxiamdamente 555 horas

**500 ÷ 0,9 ≈ 555 horas**

-Se podrán alojar 555 horas de vídeo en el disco de 500GB


#### Pregunta 2:


**Red: Tienes una línea de 100 Mbps simétricos. ¿Cuántos usuarios podrían ver el perfil "Móvil" (400 kbps) simultáneamente antes de saturar el 80% de la línea?**

-Como la línea tiene 100Mbps y para no saturarlo tenemos que usar el 80% de la línea, tenemos que multiplicar 100 x 0.8 que nos da 80 Mbps útiles

**100 × 0,8 = 80 Mbps útiles**

-Como cada usuario consume 400kbps, tenemos que pasarlo a Mbps porque la capacidad de línea también está en Mbps, por lo tanto, tenemos que hacer 400 kbps entre 1000 y nos da aproximadamente 0,4 Mbps por usuario

**400 kbps ÷ 1000 ≈ 0,4 Mbps por usuario**

-Ahora, como tenemos 80Mbps útiles y cada usuario consume 0,4 Mbps, tan solo tendremos que dividir 80 entre 0,4 y eso nos dará 200

**80 ÷ 0,4 = 200 usuarios**

-Entonces, 200 usuarios podrán ver el perfil móvil sin saturar la red




