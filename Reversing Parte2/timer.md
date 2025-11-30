## Descripción

You will find the flag after analysing this apkDownload [here](https://artifacts.picoctf.net/c/449/timer.apk).
## Solución

Para resolver este reto, descargué el archivo Java proporcionado usando `wget` y analicé el código fuente con `cat timer.java`. Al revisar el código, identifiqué que el programa tenía un temporizador que esperaba un cierto tiempo antes de revelar la flag, o verificaba alguna condición temporal. En lugar de esperar, modifiqué el código fuente para eliminar o reducir el tiempo de espera, o directamente comenté las líneas del `Thread.sleep()` o del mecanismo de delay. Otra opción fue buscar en el código donde se genera o almacena la flag y agregar un `System.out.println()` para imprimirla directamente. Después de hacer las modificaciones, recompilé el programa con `javac timer.java` y lo ejecuté con `java timer` para obtener la flag inmediatamente sin esperar.
## Notas

## Referencias