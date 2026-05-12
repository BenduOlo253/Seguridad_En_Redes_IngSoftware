# Descripción. 
Nos enfrentamos a un script de Python interactivo que toma la entrada del usuario, le añade paréntesis y la ejecuta usando la peligrosa función `eval()`. Dentro del código existe una función oculta llamada `win()` que abre el archivo de la bandera, lee su contenido y lo imprime carácter por carácter en formato hexadecimal. La vulnerabilidad reside en la posibilidad de ejecutar código arbitrario.

# Solución.

1. Se establece conexión con el servicio mediante `nc saturn.picoctf.net 49820`.
    
2. En el prompt de entrada `==>` , se ignora la sugerencia inicial y se introduce directamente la palabra `win`.
    
3. El programa evalúa la entrada como `win()` y ejecuta la función oculta.
    
4. Se obtiene una secuencia de valores hexadecimales en la salida estándar.
    
5. Se decodifican los valores hexadecimales a texto plano (ASCII) para revelar la bandera. 
**Flag: picoCTF{4_d14m0nd_1n_7h3_r0ugh_b523b2a1}** 

# Notas Adicionales. 
Este reto demuestra por qué la función `eval()` es extremadamente peligrosa en Python cuando procesa información proveniente del usuario sin sanitizar. Permite a un atacante tomar control del flujo del programa con un mínimo esfuerzo.