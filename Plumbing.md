## Descripción

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 7480`.
## Solución

Use el webshell de picoCTF para poder resolver este problema con el comando; nc jupiter.challenges.picoctf.org 7480 | grep picoCTF. Donde en nc nos yaudo a conectra con el servidor y a resivir la informacion, y el grep lo usamos par afiltar la salida para mostrar solo la linea de la bandera.

La respuesta es: picoCTF{digital_plumb3r_06e9d954}
## Notas

## Referencias
