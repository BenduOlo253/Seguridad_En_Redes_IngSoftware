# Descripción.
Se nos proporcionan dos archivos de texto extraídos de una filtración: una lista de nombres de usuario (`usernames.txt`) y una lista de contraseñas (`passwords.txt`). Las líneas de ambos archivos están emparejadas (la línea 10 de usuarios corresponde a la línea 10 de contraseñas). El objetivo es localizar la contraseña del usuario `cultiris` y descifrarla para obtener la bandera.

# Solución.

1. En lugar de contar manualmente cientos de líneas para emparejar los archivos, utilizamos la función de búsqueda de nuestro editor de texto o terminal.
    
2. Al buscar el nombre de usuario `cultiris` en el archivo de usuarios, notamos que está en una línea específica. Si buscamos esa misma línea en el archivo de contraseñas, encontramos la cadena: `cvpbPGS{P7e1S_54I35_71Z3}`.
    
3. Sabiendo que la plataforma siempre usa el formato `picoCTF{...}` y que la contraseña está cifrada con ROT13, podíamos simplemente buscar la cadena `cvpbPGS{` (que es `picoCTF{` desplazado 13 posiciones) directamente en el archivo `passwords.txt`, encontrando la bandera instantáneamente sin siquiera mirar los nombres de usuario.
    
4. Tomamos la cadena `cvpbPGS{P7e1S_54I35_71Z3}` y le aplicamos una decodificación ROT13 (desplazar cada letra 13 posiciones en el alfabeto).
    
5. El proceso transforma la `c` en `p`, la `v` en `i`, etc., revelando el texto en claro.
    

**Flag:** `picoCTF{C7r1F_54V35_71M3}`

**Notas Adicionales.**

La genialidad de este reto está en su mensaje final. Si leemos la bandera en _leet speak_ (`C7r1F_54V35_71M3`), nos está diciendo claramente: **"Ctrl F saves time"** (Ctrl+F ahorra tiempo). El creador del reto nos está recordando de forma muy cómica que el atajo de teclado para "Buscar" (`Ctrl+F`) era la herramienta de "hackeo" más eficiente para este problema.