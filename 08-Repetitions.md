## Descripción

Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/476/enc_flag).
## Solución

usamos wget para descargar el archivo que nos dan en el reto, y cat para ver su contenido, nos regresa una serie de letras que estan codificadas en base 64, yo use cyber chef para decodificarla con la formula de from base64, me regreso otra cadena a la que tuve que decodificar con la misma formula , esto lo hice un por de veces, hasta que me dio la llave.

```
ximenare-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/476/enc_flag
--2025-09-07 19:11:06--  https://artifacts.picoctf.net/c/476/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.33, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag                                                   100%[========================================================================================================================================>]     349  --.-KB/s    in 0s      

2025-09-07 19:11:06 (24.5 MB/s) - 'enc_flag' saved [349/349]

ximenare-picoctf@webshell:~$ cat enc_flag
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKVVZXMTRWMDVHV2toalJYUlhDazFyV25sVVZXaHpWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
```
## Notas

## Referencias