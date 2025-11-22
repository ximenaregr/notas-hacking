## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución

Para resolver el reto se accedió al sitio web objetivo y se inspeccionaron su código fuente y recursos para encontrar pistas. Se revisaron archivos como _robots.txt_, _sitemap_ y rutas comunes, y se enumeraron directorios y endpoints adicionales. Se analizaron formularios, parámetros, cabeceras y la lógica en JavaScript para detectar entradas manipulables o funciones ocultas. Con las pistas obtenidas se probaron técnicas básicas de explotación web, como fallos de autenticación o parámetros sin validar. Finalmente, se extrajeron y decodificaron los datos encontrados hasta obtener la bandera, documentando la ruta y la técnica usada.
## Notas

## Referencias