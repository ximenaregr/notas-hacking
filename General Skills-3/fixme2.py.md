## Descripción

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
## Solución

Corremos el script  vemos que tiene un error en la linea 22, usamos nano para poder  modificarlo, faltaba un = en el if, al volver a correrlo, nos regresa la bandera
```
python fixme2.py
  File "/home/ximenare-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
ximenare-picoctf@webshell:~$ nano fixme2.py
ximenare-picoctf@webshell:~$ python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```
## Notas

## Referencias
