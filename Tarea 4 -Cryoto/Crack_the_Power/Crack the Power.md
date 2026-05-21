**Descripción.**

El reto nos proporciona parámetros de un cifrado RSA: un módulo `n` de gran tamaño, un texto cifrado `c` y un exponente público `e` inusualmente bajo (`e = 20`). La complejidad radica en que el módulo `n` es demasiado grande para ser factorizado con métodos convencionales, pero las pistas sugieren que existe un atajo matemático ("shortcut") para invertir la operación sin necesidad de conocer la clave privada.

**Solución.**

1. Se analiza la fórmula estándar de RSA: $c = m^e \pmod n$.
    
2. Se identifica la vulnerabilidad: dado que el exponente `e = 20` es muy pequeño y el mensaje original `m` (la bandera) es relativamente corto, la operación de elevar el mensaje a la potencia de 20 produce un número que sigue siendo menor que el módulo `n` ($m^{20} < n$).
    
3. Al cumplirse que $m^e < n$, la operación módulo de la fórmula matemática no tiene ningún efecto. El cifrado se reduce a una simple exponenciación: $c = m^{20}$.
    
4. Para revertir esto y recuperar el mensaje original, no se necesita factorizar `n`. Simplemente se debe calcular la raíz 20 exacta del texto cifrado `c`.
    
5. Se implementa un script en Python utilizando un algoritmo de búsqueda binaria matemática para calcular la raíz exacta sin perder precisión decimal por el tamaño de los números.
    
6. El número entero resultante se decodifica de bytes a texto plano (ASCII), revelando el mensaje original.
    
    Flag: `picoCTF{t1ny_e_381870dd}`
    

**Notas Adicionales.**

Este desafío ilustra una vulnerabilidad clásica y fundamental en implementaciones ingenuas de RSA. Demuestra por qué en la criptografía del mundo real es obligatorio utilizar algoritmos de relleno (como _Padding OAEP_) antes de encriptar. El relleno añade datos aleatorios al mensaje para asegurar que $m$ sea siempre un número gigantesco, forzando así que $m^e$ supere ampliamente a `n` y garantizando que la operación módulo proteja la reversibilidad del cifrado.