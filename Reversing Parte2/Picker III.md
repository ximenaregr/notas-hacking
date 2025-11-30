## Descripción

Can you figure out how this program works to get the flag?

Additional details will be available after launching your challenge instance.
## Solución

Para resolver este reto, después de conectarme con `nc`, analicé cuidadosamente las restricciones implementadas. El programa bloqueaba nombres de funciones comunes y caracteres especiales. Utilicé técnicas avanzadas como acceder a `__builtins__.__dict__` para obtener funciones del sistema, o concatenar strings para construir nombres de funciones que evadieran los filtros (por ejemplo, `'wi' + 'n'`). 
## Notas

## Referencias