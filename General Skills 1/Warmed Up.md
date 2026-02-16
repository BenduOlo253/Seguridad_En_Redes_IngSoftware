# Descripción.
What is 0x3D (base 16) in decimal (base 10)?
***pista***
Submit your answer in our flag format. For example, if your answer was '22', you would submit 'picoCTF{22}' as the flag.

# Solución.
Para la solucion del reto, usare "bc", de la siguiente forma:
echo "obase=10; ibase=16; 3D" | bc
***Resultado***
61
***Flag***: picoCTF{61}
# Notas Adicionales.
- Al momento de usar bc, hay que tener en cuenta que el comando ya espera recibir el dato en la base especificada. Por ejemplo si hubieramos puesto 0x3D eso saldria error porque x no es parte del formato hexadecimal, el prefijo *0x....* solo son una forma de aclarar que lo siguiente esta en formato hexadecimal.
# Referencias.
https://www.networkworld.com/article/971677/converting-numbers-on-linux-among-decimal-hexadecimal-octal-and-binary.html#:~:text=Convertir%20n%C3%BAmeros%20a%20decimales%20con,en%20los%20ejemplos%20a%20continuaci%C3%B3n.&text=Al%20igual%20que%20en%20el,s%C3%B3lo%20requiere%20un%20peque%C3%B1o%20esfuerzo.