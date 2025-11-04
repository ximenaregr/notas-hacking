## Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución

Igual que en los anteriores, la contraseña estaba en el script donde nos daban varias opciones, la contraseña correcta era la ultima.

```
ximenare-picoctf@webshell:~$ nano level3.py
ximenare-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 865e
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
```
## Notas

## Referencias
