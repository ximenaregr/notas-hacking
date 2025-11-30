## Descripción
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/60786/` ([link](https://jupiter.challenges.picoctf.org/problem/60786/)) or http://jupiter.challenges.picoctf.org:60786
## Solución
Revisamos el codigo fuente de la pagina, y podemos ver, la variable checkpass contiene nuestra entrada, y en este caso, el método `each` de subcadena nos proporciona un número de caracteres divididos (establecidos en 4) a partir del primer argumento del método. La primera parte es de 0-8 y siguiendo en donde se quedo el ultimo numero.
picoCTF{no_clients_plz_ee2f24}
## Notas

## Referencias
