# Descripción.
El código fuente en Java implementa una bóveda de entrenamiento cuya validación compara directamente la contraseña ingresada con una cadena de texto estática utilizando el método `.equals()`.

# Solución.

1. Se inspecciona el archivo `VaultDoorTraining.java` utilizando cualquier editor de texto o comando de lectura en terminal (`cat`).
    
2. Se localiza la función `checkPassword()`.
    
3. Se extrae la cadena de texto fija incrustada entre comillas dentro del método de comparación, la cual es la contraseña en texto plano. 
Flag: `picoCTF{w4rm1ng_Up_w1tH_jAv4_000wYdiGTvt}`

# Notas Adicionales. 
Demuestra el concepto más básico de ingeniería inversa y análisis estático: buscar cadenas (strings) en texto plano (hardcoding) que los desarrolladores dejan expuestas directamente en el código fuente.