---
title: Distrochooser, descarga fácilmente distros de Linux desde CLI
date: 22:55 10/01/2018
taxonomy: 
	category: sysadmin
	tag: [linux, ubuntu, debian, archlinux, centos, fedora, centos, wget, script, bash, download, cli]
published: true
---
Distrochooser es un pequeño script que he elaborado para descargar cualquier distribución popular pulsando un par de teclas evitando ir a los mirrors o páginas oficiales para descargarlos. 
Se puede obtener desde GitHub
```
git clone https://github.com/sincorchetes/distrochooser
chmod +x distrochooser/run.sh
./distrochooser/run.sh
```
Este script crea un directorio `iso` en la ruta de trabajo actual dónde descargar la imagen, para su descarga hace uso del comando `wget` utilizando el modificador `-c` que permite renaudar la descarga en caso de fallo, por lo que deberemos tenerlo instalado en nuestro sistema.

En la próxima versión soportará verificación de firma, más distribuciones. Espero que os guste.

<script src="https://asciinema.org/a/YALdTZZWMUPFOjPVgpbbA6cIt.js" id="asciicast-YALdTZZWMUPFOjPVgpbbA6cIt" async></script>

Un saludo.
