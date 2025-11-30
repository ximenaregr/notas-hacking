## Descripción

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Solución

Para resolverlo use el webshell de picoCTF, primero copie la dirección de enlace de el archivo de file, para poder descargar el archivo en el webshell use wget y la dirección de enlace. Después use: strings file | grep -i picoCTF.  Con eso me regreso una cadena que es la bandera.

La respuesta es picoCTF{grep_is_good_to_find_things_dba08a45}
## Notas

El comando grep nos sirve para buscar patrones de texto, secuencias de caracteres dentro de archivos o en la salida de otros comandos.
## Referencias

