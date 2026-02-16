# Descripción.
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.The flag is in this.
# Solución.
Primero busque un pequeño tutorial para usar grep, despues aplique lo visto:
$ grep -oE "picoCTF{.*?}" file
picoCTF{grep_is_good_to_find_things_9C6Ef2F7}

# Notas Adicionales.
`grep -oE "picoCTF{.*?}" archivo`

- `-o` (only-matching): Te muestra **solo** el texto que coincide, no toda la línea. Muy útil si la línea mide 10,000 caracteres.
    
- `.*?` : Busca todo lo que haya dentro de los corchetes de forma "perezosa" (se detiene en el primer `}`).
# Referencias.
busque ayuda con gemini.