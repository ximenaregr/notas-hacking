## Descripción

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Solución

Para resolverlo use el webshell de pico, para guardar el archivo que nos daba en la descripción de el reto, lo guardamos con wget, y usamos strings, con el comando de strings strings | grep pico. Para filtrar los resultados, así nos dio la llave del reto.

## Notas

String. Para ver cadenas de texto especiales que no se pueden imprimir 
## Referencias