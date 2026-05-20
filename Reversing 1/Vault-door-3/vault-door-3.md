# Descripción.
La bóveda toma la contraseña del usuario (de 32 caracteres) y la desordena guardando sus letras en un búfer temporal (arreglo) mediante cuatro bucles `for` que reordenan los índices (directos, invertidos y saltando posiciones). Finalmente, compara el búfer modificado con la cadena fija `"jU5t_a_sna_3lpm13gf49_u_4_m9r540"`.

# Solución.

1. Se realiza ingeniería inversa revirtiendo matemáticamente la lógica de los cuatro bucles para mapear los caracteres ofuscados de vuelta a sus posiciones originales.
    
2. Bucle 1 (Índices 0-7): Se leen directamente.
    
3. Bucle 2 (Índices 8-15): Se invierte el orden del bloque.
    
4. Bucle 3 y 4 (Índices 16-31): Se reordenan alternando los caracteres en las posiciones pares e impares.
    
5. Se concatenan los bloques reconstruidos. 
Flag: `picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_99f530}`

# Notas Adicionales. 
Gran ejercicio de seguimiento de algoritmos de ofuscación basados en índices (básicamente un anagrama matemático). La aparición de palabras con sentido (como _anagram_) confirma que la reversión algorítmica fue exitosa.