## Descripción

What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/290/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
## Solución

Para resolver este reto, descargué el archivo Java con `wget` y analicé el código fuente con `cat SafeOpener.java`. En esta versión, la contraseña estaba ofuscada mediante operaciones matemáticas, XOR, o almacenada como un array de valores numéricos que representan caracteres ASCII. Identifiqué la sección del código donde se construye o verifica la contraseña, y utilicé Python o una calculadora para decodificar los valores. Por ejemplo, si había un array como `{112, 105, 99, 111}`, lo convertí a caracteres ASCII. También pude modificar el código Java para imprimir directamente la contraseña agregando `System.out.println(password);` antes de la comparación, recompilar con `javac` y ejecutar para obtener la flag.
## Notas

## Referencias