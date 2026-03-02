# Descripcion.
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.`ssh -p 59050 ctf-player@saturn.picoctf.net`The password is `8a707622`

**Pistas:**
1. Experiment with different shell syntax

# Solución.
1. Me conecte mediente ssh al reto.
2. intente los comandos basicos.
3. Investigue una manera de ingresar los comandos en una pagina.
4. use la forma ${parameter='comando'} para ejecutar comandos.
5. Use un ls para ver los archivos.
6. Buscando en la carpeta que habia, logre dar con la bandera.
7. hice un cat a la bandera y obuve la bandera.

**Flag: picoCTF{5p311ch3ck_15_7h3_w0r57_a60bdf40}**
# Notas Adicionales.
usar ${parameter='comando'} puede llegar a ser muy util cuando la sintaxis de la terminal es restringida o cambiada.
# Referencias.
https://josephkimiri.github.io/posts/Special/
