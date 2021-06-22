# Viendo el tiempo en tu terminal

¿Te gustaría ver el tiempo en tu terminal? No te gustan los plugins de los entornos de escritorio o usas un gestor de ventanas tipo _i3wm_ que no tiene ningún icono en la bandeja de notificación de _i3status_.

Bueno pues no pasa nada, puedes ver el tiempo que hará en tu ciudad con tan solo ejecutar un `curl` al dominio [wttr.in](http://wttr.in?target=_blank) y por GeoIP te dará la climatología de tu lugar.

# ¿Qué puedes hacer?

 * Información de vuelta traducida a un idioma en concreto
 * Definir los días que queramos que nos devuelva (0 si es solo el día de hoy)
 * Definir la métrica, sistema internacional de unidades o sistema anglosajon
 * Calendario lunar
 * Buscar una ubicación
 * Convertir el resultado en un .png
 * Añadir transparencia a la imagen
 * Añadir un marco a la imagen que has generado

# Visualizando en un sitio específico
```
curl wttr.in/Palma?1q
```
Devolverá algo tal que así:
```
Palma, Spain

    \  /       Partly cloudy
  _ /"".-.     6-7 °C         
    \_(   ).   ↘ 6 km/h       
    /(___(__)  10 km          
               0.2 mm         
```
En mi caso como es Palma, porque vivo en ella. ¿Qué pasa si quiero otra ciudad?

Pues puedes apoyarte de la ayuda:
```
[sincorchetes@keys0 ~]$ curl wttr.in/:help
Usage:

    $ curl wttr.in          # current location
    $ curl wttr.in/muc      # weather in the Munich airport

Supported location types:

    /paris                  # city name
    /~Eiffel+tower          # any location
    /Москва                 # Unicode name of any location in any language
    /muc                    # airport code (3 letters)
    /@stackoverflow.com     # domain name
    /94107                  # area codes
    /-78.46,106.79          # GPS coordinates

Special locations:

    /moon                   # Moon phase (add ,+US or ,+France for these cities)
    /moon@2016-10-25        # Moon phase for the date (@2016-10-25)

Units:

    m                       # metric (SI) (used by default everywhere except US)
    u                       # USCS (used by default in US)
    M                       # show wind speed in m/s

View options:

    0                       # only current weather
    1                       # current weather + 1 day
    2                       # current weather + 2 days
    F                       # do not show the "Follow" line
    n                       # narrow version (only day and night)
    q                       # quiet version (no "Weather report" text)
    Q                       # superquiet version (no "Weather report", no city name)
    T                       # switch terminal sequences off (no colors)

PNG options:

    /paris.png              # generate a PNG file
    p                       # add frame around the output
    t                       # transparency 150
    transparency=...        # transparency from 0 to 255 (255 = not transparent)

Options can be combined:

    /Paris?0pq
    /Paris?0pq&lang=fr
    /Paris_0pq.png          # in PNG the file mode are specified after _
    /Rome_0pq_lang=it.png   # long options are separated with underscore

Localization:

    $ curl fr.wttr.in/Paris
    $ curl wttr.in/paris?lang=fr
    $ curl -H "Accept-Language: fr" wttr.in/paris

Supported languages:

    da de fr fa id it nb nl pl ru (supported)
    az be bg bs ca cy cs el eo es et fi hi hr hu hy is ja jv ka kk ko ky lt lv mk ml nl nn pt ro sk sl sr sr-lat sv sw th tr te uk uz vi zh zu he (in progress)

Special URLs:

    /:help                  # show this page
    /:bash.function         # show recommended bash function wttr()
    /:translation           # show the information about the translators
```
# Mostrando la fase lunar
```
[sincorchetes@keys0 ~]$ curl wttr.in/moon
                  ------------.  
              --'  o     . .   `--.  
            '   .    O   .       . `-.   
          @   @@@@@@@   .  @@@@@      `-.  
         @  @@@@@@@@@@@   @@@@@@@   .    \   
          o @@@@@@@@@@@   @@@@@@@       . \.   
        o   @@@@@@@@@@@.   @@@@@@@   O      \  
      @   .   @@@@@@@o    @@@@@@@@@@     @@@ \   
     @@@               . @@@@@@@@@@@@@ o @@@@|   
     @@  O  `.-./  .      @@@@@@@@@@@@    @@  \  First Quarter +
     @@    --`-'       o     @@@@@@@@ @@@@    |  4 14:22:41
     @@        `    o      .  @@   . @@@@@@@  |  Full Moon -
         @@  @         .-.     @@@   @@@@@@@  |  2  8:08:13
      @        @@@     `-'   . @@@@   @@@@  o /  
         @@   @@@@@ .           @@   .       |   
        @@@@  @\@@    /  .  O    .     o   . /   
         @@     \ \  /         .    .       /  
           .    .\.-.___   .      .   .-. /'   
                  `-'                `-' /   
             o   / |     o    O   .   .-'  
            .   /     .       .    .-'   
              --.       .      .--'  
                  ------------'  


Follow @igor_chubin for wttr.in updates

```

# Referencias
* wtrr.info - [repositorio GitHub](https://github.com/chubin/wttr.in?target=_blank)

