## Descripción
Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:21939/
## Solución

Accedemos al enlace proporcionado por el reto. Vemos una página con un botón que alterna entre dos imágenes (“red” y “blue”).  
Abrimos la pestaña Red y observamos las solicitudes que se hacen cuando pulsamos el botón. Todas las peticiones son de tipo GET.

El título del reto sugiere probar el método **HEAD**, que solicita solo los encabezados de la respuesta sin el cuerpo del contenido.  
Para probarlo, podemos usar **cURL** o **Burp Suite**, pero la manera más simple es hacerlo desde la terminal:

`curl -I http://satellite.picoctf.net:xxxxx/`

(Sustituye la URL y puerto con los del reto.)

El parámetro `-I` envía una solicitud **HEAD**.  
La respuesta devuelve los encabezados HTTP, y entre ellos encontramos la bandera:

`HTTP/1.1 200 OK Content-Type: text/html Flag: picoCTF{r3j3ct_th3_du4l1ty_6f8f2fbd}`

También se puede intentar manualmente con Burp Suite o cambiando el método de la solicitud desde una extensión del navegador (como **ModHeader** o **RESTED**).
## Notas

## Referencias
