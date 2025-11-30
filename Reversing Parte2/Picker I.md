## Descripción

This service can provide you with a random number, but can it do anything else?

Additional details will be available after launching your challenge instance.
## Solución

Para resolver este reto, primero me conecté al servidor usando `nc` con la dirección y puerto proporcionados. Al analizar el código fuente, descubrí que permite ejecutar funciones por su nombre. El programa tiene una función oculta que contiene la flag, generalmente llamada `win`, `print_flag` o similar. Simplemente ingresé el nombre de esta función cuando el programa me lo solicitó, y el programa ejecutó la función revelando la flag directamente en la terminal.
## Notas

## Referencias