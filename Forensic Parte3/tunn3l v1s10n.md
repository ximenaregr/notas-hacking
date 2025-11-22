## Descripción

We found this [file](https://mercury.picoctf.net/static/d0129ad98ba9258ab59e7700a1b18c14/tunn3l_v1s10n). Recover the flag.
## Solución

1. Descargar el archivo del reto.
    
2. Comprobar el tipo de archivo para confirmar que es una imagen.
    
3. Visualizar la imagen por si la bandera es visible a simple vista.
    
4. Buscar texto oculto dentro del archivo (búsqueda de cadenas).
    
5. Analizar los canales de la imagen en busca de datos en los bits menos significativos (LSB).
    
6. Extraer cualquier texto o bloque encontrado y comprobar si está codificado.
    
7. Decodificar el contenido si es necesario (por ejemplo Base64) para revelar la bandera.
    
8. Registrar la bandera y añadir notas breves sobre la herramienta/método usado.
## Notas

## Referencias