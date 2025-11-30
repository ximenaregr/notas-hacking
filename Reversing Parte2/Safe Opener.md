## Descripción

Can you open this safe?I forgot the key to my safe but this [program](https://artifacts.picoctf.net/c/83/SafeOpener.java) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?Put the password you recover into the picoCTF flag format like:`picoCTF{password}`
## Solución

Para resolver este reto, descargué el archivo Java proporcionado usando `wget`. Al abrir el código fuente con `cat SafeOpener.java` o cualquier editor de texto, pude observar directamente la contraseña codificada en el código. El programa compara la entrada del usuario con una cadena que está hardcodeada en el código fuente. Simplemente extraje esa cadena del código, la decodifiqué, y la usé como input al ejecutar el programa con `java SafeOpener`, lo que me dio acceso a la flag del reto.
## Notas

## Referencias