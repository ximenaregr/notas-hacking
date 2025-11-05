## Descripción
There is some interesting information hidden around this site [http://mercury.picoctf.net:39491/](http://mercury.picoctf.net:39491/). Can you find it?
## Solución
La bandera esta dividida en 5 partes, lo priemeor que hicer fue ver el codigo de la pagina, y ahi esta la primera parte, para la segunda parte se encuentra en el css que esta en el codigo.
Para la terecer parte intentamos buscar en el script de java donde mps da uan pista que dice "Como puedo evitar que Google indexe mi sitio web" es una referncia a robots.txt, que al ponerlo nos da la tercera parte de la bandera, y una pista a la siguiente parte "Creo que este es un servidor Apache... ¿Puedes acceder a la siguiente bandera?".

La palabra calve es access, para la cuarta parte ponemos un .htaccess y nos da la bandera, con la pista de la siguiente parte "Me encanta crear sitios web en mi Mac, puedo almacenar mucha información allí." Lo que usamos es un .DS_Store.

## Notas

## Referencias
