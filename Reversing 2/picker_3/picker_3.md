# Descripción.
El código intenta mitigar las vulnerabilidades previas limitando la ejecución a una tabla de funciones predefinidas (`func_table`). No obstante, habilita una opción (`write_variable`) que utiliza `exec()` para sobrescribir variables globales. La validación exige que la variable mida exactamente 128 caracteres y no contenga paréntesis ni punto y coma, pero esto no impide inyectar cadenas de texto manipuladas mediante operaciones matemáticas de Python.

# Solución.

1. Se establece conexión con el servicio mediante `nc saturn.picoctf.net 49338`.
    
2. Se selecciona la opción `3` del menú para invocar `write_variable`.
    
3. Se indica `func_table` como la variable global objetivo a modificar.
    
4. Se inyecta el valor `'win' + ' ' * 125` para cumplir con el requisito de longitud exacta (128 caracteres) esquivando los caracteres prohibidos.
    
5. Se regresa al menú principal y se elige la opción `1` para ejecutar la primera entrada de la tabla manipulada, la cual ahora ejecuta `win()`.
    
6. Se decodifican los valores hexadecimales obtenidos a ASCII. Flag:
**picoCTF{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_c20f5222}**
    

# Notas Adicionales. 
Resalta los graves riesgos de permitir a los usuarios modificar variables de estado globales en tiempo de ejecución. Los controles basados en longitud y las listas negras de caracteres pueden ser burlados fácilmente utilizando la sintaxis matemática de strings propia del lenguaje.