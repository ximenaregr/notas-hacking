## Descripción

Can you figure out how this program works to get the flag?

Additional details will be available after launching your challenge instance.
## Solución

Para resolver este reto, me conecté al servidor con `nc` y analicé las restricciones del programa. A diferencia de Picker I, este programa filtra ciertos nombres de funciones. Sin embargo, pude bypassear esta restricción utilizando funciones built-in de Python como `__builtins__`, `globals()`, o `dir()` para listar todas las funciones disponibles y luego acceder a la función que contiene la flag mediante técnicas como `getattr()` con el diccionario de funciones globales. 
## Notas

## Referencias