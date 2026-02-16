# Descripción.
"Can you convert the number 42 (base 10) to binary (base 2)?"
**Pista**
"Submit your answer in our competition's flag format. For example, if your answer was '11111', you would submit 'picoCTF{11111}' as the flag."
# Solución.
Primero investigue la forma en que se pueden convertir numeros decimales a binario en linux, encontre una pagina donde explican la forma de hacer esta convercion con comandos.

El comando es el siguiente:
*echo "obase=2; 42" | bc*
como resultado me dio: 
101010

Por lo tanto la bandera es:
picoCTF{101010}

# Notas Adicionales.
echo "obase=n; x" | bc
n= la base a la que se desea convertir el numero decimal.
x= es el numero decimal que se desea convertir.
# Referencias
https://www.networkworld.com/article/971677/converting-numbers-on-linux-among-decimal-hexadecimal-octal-and-binary.html#:~:text=Convertir%20n%C3%BAmeros%20a%20decimales%20con,en%20los%20ejemplos%20a%20continuaci%C3%B3n.&text=Al%20igual%20que%20en%20el,s%C3%B3lo%20requiere%20un%20peque%C3%B1o%20esfuerzo.