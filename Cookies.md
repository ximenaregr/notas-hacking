## Descripción
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:64944/](http://mercury.picoctf.net:64944/)
## Solución

En el sitio web entamos a ve las cookies,  vemos que ha una llamada auth'name con el valo "guest"`

El sitio también nos permite cambiar el valor de la cookie a través de una página que genera una nueva cookie en base al nombre que introduzcamos. Al probar con `"admin"`, notamos que el sitio devuelve una cookie diferente, pero aún no muestra la bandera.

Descargamos la cookie generada y observamos que está codificada. Si analizamos el valor, podemos notar que está en Base64. Al decodificarla, vemos que representa información sobre el usuario. Lo que tenemso que hacer es modificar la cookie para que el campo de usuario sea admin.

Ingresamos `"admin"` en el formulario para generar la cookie y la establecemos manualmente. Una vez cambiada correctamente la cookie y refrescamos la página, el sitio muestra la bandera.
## Notas

## Referencias
