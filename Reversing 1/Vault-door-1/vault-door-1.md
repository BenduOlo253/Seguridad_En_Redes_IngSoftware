# Descripción. 
En este reto, el código fuente en Java intenta ofuscar la validación de la contraseña verificando cada carácter de la cadena de forma individual y en un orden completamente aleatorio. Para lograr esto, utiliza el método `password.charAt(índice)`, que comprueba si la letra en esa posición específica (empezando a contar desde el 0) coincide con el carácter esperado.

# Solución.

1. Se descarga el código fuente `VaultDoor1.java`.
    
2. Se extraen todas las líneas de código que contienen la instrucción `charAt()`.
    
3. Se ordenan secuencialmente guiándose por el índice numérico (del 0 al 31).
    
4. Se extrae el carácter correspondiente a cada posición para ensamblar la cadena original. Esto puede hacerse de forma manual leyendo el archivo, o de forma automatizada en la terminal de Linux usando una tubería de comandos: `grep charAt VaultDoor1.java | sort -V | awk '{print $3}' | tr -d "'\n"`.
    
5. Se envuelve la cadena resultante en el formato estándar de la plataforma. 
Flag: `picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_7ffa94}`

# Notas Adicionales. 
Este desafío es un excelente ejercicio introductorio para aprender a usar comandos de manipulación de texto en Linux. Utilizar herramientas como `grep`, `sort`, `awk` y `tr` combinadas para "desofuscar" información desordenada ahorra horas de trabajo manual, lo cual es una habilidad vital en retos de ciberseguridad y análisis de logs.