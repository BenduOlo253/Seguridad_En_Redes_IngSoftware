# Descripción. 
El sistema de seguridad utiliza dos capas de codificación. Transforma la entrada del usuario aplicando URL encoding (caracteres en hexadecimal precedidos por `%`) y posteriormente la codifica en Base64. Para validar el acceso, compara el texto resultante con una cadena fija de caracteres pre-codificada en el código fuente.

# Solución.

1. Se toma la cadena de texto fija almacenada en el archivo.
    
2. Se le aplica ingeniería inversa ejecutando el proceso contrario: primero se decodifica desde Base64 para revelar la representación en formato URL.
    
3. Se aplica un _URL Decode_ a la cadena obtenida para traducir cada valor hexadecimal (ej. `%63`) a su correspondiente carácter en texto plano.
    
4. El texto resultante revela la contraseña original. 

Flag: `picoCTF{c0nv3rt1ng_fr0m_ba5e_64_7f855fc5}`

# Notas Adicionales.
Resalta una lección fundamental de la industria: **codificación no es cifrado**. Algoritmos como Base64 o URL Encoding están diseñados para el transporte estandarizado de datos en la red, no para ocultarlos, por lo que pueden revertirse de inmediato sin llaves ni contraseñas.