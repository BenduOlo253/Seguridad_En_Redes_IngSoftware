# Descripción. 
Secuela del reto anterior donde el desarrollador introdujo un parche de seguridad: la función `filter()`. Esta función verifica si la palabra 'win' está presente en la entrada del usuario y, de ser así, bloquea la ejecución. Sin embargo, el programa sigue utilizando `eval()`, lo que permite evadir el filtro mediante técnicas de ofuscación o inyección de código nativo.

# Solución.

1. Se establece conexión con el servicio mediante `nc saturn.picoctf.net 58024`. 
2. En el prompt `==>` , se introduce código Python para leer el archivo directamente sin llamar a la función bloqueada: `print(open('flag.txt','r').read())`.
    
3. Alternativamente, se evade el filtro construyendo la palabra bloqueada en tiempo de ejecución: `globals()['w'+'in']`.
    
4. El programa ejecuta el código inyectado, saltándose con éxito la validación de la lista negra.
    
5. Se decodifican los valores hexadecimales resultantes a texto plano. 
**Flag: picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_0b5f113}**


# Notas Adicionales. 
Enseña que los filtros basados en listas negras (blocklists) casi siempre son ineficientes. Los atacantes pueden ofuscar cadenas de texto mediante concatenación o utilizar funciones alternativas para lograr exactamente el mismo objetivo sin activar las alertas.