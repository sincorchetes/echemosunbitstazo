---
title: Instalar Telnet en nuestro sistema
date: 14:15 03/05/2018
taxonomy: 
	category: Network
	tag: [observa,telecom,switch,router, cli,linux, windows,network, ccna, cisco, alcatel, telnet]
body_classes: single single-post
published: false
routable: false
---

1. Arrancar con un pendrive con imagen Windows 10
2. Entrar en Opciones avanzadas de recuperación
3. Símbolo del sistema
4. diskpart
	sel disk 0
	list vol
		Por lo general, si hemos instalado Windows en primer lugar, tendremos la partición EFI en la tercera posición
5. sel vol 2
6. assign letter=G:
7. exit
8. cd /d G:\EFI\Microsoft\Boot
9. bootrec /fixboot
10. copy X:\EFI\Microsoft\bootx86.cfg (Creo)
11. copy X:\EFI\Boot\en-us\*
12. exit
13. Reiniciar
14. Voilá!