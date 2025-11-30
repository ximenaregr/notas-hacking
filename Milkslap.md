## Descripción

## Solución

Copiar la dirección de el video que aparece en la pagina, lo descargamos, y con zsteg en el archivo  y nos regresa la bandera.

```
kali㉿kali)-[~]
└─$ wget http://mercury.picoctf.net:58537/concat_v.png
--2025-11-29 14:47:56--  http://mercury.picoctf.net:58537/concat_v.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:58537... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18095920 (17M) [image/png]
Saving to: ‘concat_v.png’

concat_v.png       100%[================>]  17.26M  12.6MB/s    in 1.4s    

2025-11-29 14:47:58 (12.6 MB/s) - ‘concat_v.png’ saved [18095920/18095920]

                                                                            
┌──(kali㉿kali)-[~]
└─$ zsteg             

┌──(kali㉿kali)-[~]
└─$ zsteg concat_v.png

```
## Notas

## Referencias
