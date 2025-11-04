## Descripción

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.
## Solución

Use el webshell de picoCTF y se puso el comando que venia en la instrucción para conectarse a lo que se nos pide, cuando damos enter nos sale una secuencia de números, el cual nos pide que regresemos como una palabra, para convertirla usamos cyberchef con la herramienta mágica, al ingresar la palabra que se nos dio nos valida que sea correcta para darnos una nueva secuencia y  pedirnos una nueva palabra en la que usamos cyberchef para descifrarla, esto ocurre una vez mas al descifrar la tercer palabra e ingresarla nos da la flag del reto.

La respuesta fue: picoCTF{learning_about_converting_values_b375bb16}

```ximenare-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29956
Let us see how data is stored
colorado
Please give the 01100011 01101111 01101100 01101111 01110010 01100001 01100100 01101111 as a word.
...
you have 45 seconds.....

Input:
colorado
Please give me the  157 166 145 156 as a word.
Input:
oven
Please give me the 616e696d6174696f6e as a word.
Input:
animation
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_b375bb16}
```
## Notas

La herramienta mágica de Cyber Chef nos ayuda a saber la formula que necesitaremos para decodificar la palabra.
## Referencias
