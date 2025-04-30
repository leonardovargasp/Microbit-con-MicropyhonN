# Microbit-con-MicropyhonN

## Utilización innovadora y precisa de los sensores básicos, con integración efectiva en el proyecto.

from microbit import *
lightsOn = False

while True:
    if microphone.was_event(SoundEvent.LOUD):
        lightsOn = not lightsOn
        if lightsOn:
            display.show(Image.HEART)
        else:
            display.clear()
    sleep(100)

## Implementación creativa y eficiente del uso de la matriz LED con animaciones avanzadas o patrones complejos.

from microbit import *

while True:
    display.show(Image(
        "00000:"
        "00900:"
        "09990:"
        "00900:"
        "00000"))
    sleep(500)
    display.show(Image(
        "00000:"
        "09990:"
        "09990:"
        "09990:"
        "00000"))
    sleep(500)
    display.show(Image(
        "90909:"
        "09990:"
        "99999:"
        "09990:"
        "90909"))
    sleep(500)

##	Integración y uso superior de otros elementos o sensores no especificados, potenciando el proyecto.

    from microbit import *
import music


for x in range(2):
    music.play(['C4:4', 'D4', 'E4', 'C4'])

for x in range(2):
    music.play(['E4:4', 'F4', 'G4:8'])

##	Implementación avanzada y optimizada de la comunicación por radio, con manejo de errores y confirmaciones.

    from microbit import *
import radio


radio.config(group=1)
radio.on()

while True:
    message = radio.receive()
    if message:
        display.show(Image.HAPPY)
    if button_a.was_pressed():
        display.clear()
        radio.send('smile')
