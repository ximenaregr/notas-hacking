## Descripción

Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility.The source code for the training vault is here: [VaultDoorTraining.java](https://challenge-files.picoctf.net/c_fickle_tempest/894d84f5b5e66228fa8e422d898a42adf4fd8298aa8d322decaf9b172ba276ea/VaultDoorTraining.java)
## Solución
abrimos el archivo Java proporcionado y se busca el método `checkPassword`, donde aparece un arreglo `char[]` que contiene la contraseña dividida carácter por carácter. Luego, simplemente se copian esos caracteres tal como están y se unen en una sola cadena, ya que el programa no realiza ninguna transformación ni cifrado la contraseña está explícitamente escrita en el arreglo. Al unirlos en orden, se obtiene la bandera.
## Notas

## Referencias
