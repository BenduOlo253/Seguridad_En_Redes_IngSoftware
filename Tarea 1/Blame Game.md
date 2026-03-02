# Descripción.
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

**Pistas:**
1. In collaborative projects, many users can make many changes. How can you see the changes within one file?
2. Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3. You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.
# Solución.
1. Descargue el archivo.
2. Descomprmi el archivo.
3. inicie el repositorio de git dentro de la carpeta.
4. use git blame para encontrar el commit que hizo que no funcionara el programa.
**Flag: picoCTF{@sk_th3_1nt3rn_d2d29f22}**
# Notas Adicionales.
git blame "archivo" sirve para encontrar el comit que provoco algún error en algún archivo.
# Referencias.
https://www.geeksforgeeks.org/git/how-to-use-git-blame/
