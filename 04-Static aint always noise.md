## Descripción

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!
## Solución

Cargamos los dos archivos con wget, vemos que tipo de archivo son, usamos strings en el archivo static, buscando la palabra pico.

```
ximenare-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
--2025-09-07 16:30:32--  
2025-09-07 16:30:32 (213 MB/s) - 'static' saved [8376/8376]

ximenare-picoctf@webshell:~$ wget 

2025-09-07 16:30:47 (353 MB/s) - 'ltdis.sh' saved [785/785]

ximenare-picoctf@webshell:~$ file ltdis.sh
ltdis.sh: Bourne-Again shell script, ASCII text executable
ximenare-picoctf@webshell:~$ file static
static: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=277d07901cf99a335a8107fbdd6642d9c6140bb5, not stripped

ximenare-picoctf@webshell:~$ ls
Addadshashanammu  ltdis.sh  static
ximenare-picoctf@webshell:~$ strings static | grep pico 
picoCTF{d15a5m_t34s3r_f5aeda17}

```
## Notas

## Referencias
