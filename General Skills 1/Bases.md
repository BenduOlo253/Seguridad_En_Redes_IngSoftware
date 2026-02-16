# Descripción.
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.
***Pista***:
Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

# Solución.
Primero identifique en que base esta codificado el texto y despues de investigar un poco, llego a la conclusión de que es base 64 y decido utilizar los comandos de la terminal de linux para decodificarlo.
$ echo "bDNhcm5fdGgzX3IwcDM1" | base64 -d
***Resultado***
l3arn_th3_r0p35
***Flag***: picoCTF{l3arn_th3_r0p35}
# Notas Adicionales.
Tambien existe un comando para la base 32:
echo "..." | base32 -d
# Referencias.