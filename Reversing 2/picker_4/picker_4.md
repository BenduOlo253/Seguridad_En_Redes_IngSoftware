# Descripción.
Se proporciona un programa compilado en C que solicita al usuario una dirección de memoria en formato hexadecimal. El programa toma este valor numérico, lo convierte en un puntero a función y redirige el flujo de ejecución hacia esa dirección exacta. Dentro del binario existe una función `win()` que lee e imprime el archivo `flag.txt`, pero la cual no es llamada de forma natural por el programa.

# Solución.

1. Se descarga el archivo binario ejecutable asociado al reto.
    
2. Se analizan los símbolos del binario en la terminal local utilizando herramientas de inspección (`nm archivo_binario | grep win`).
    
3. Se extrae la dirección de memoria estática de la función `win` (0x40129e).
    
4. Se establece conexión con el servidor mediante `nc saturn.picoctf.net 54677`.
    
5. Se ingresa la dirección de memoria encontrada, sin el prefijo '0x': `40129e`.
    
6. El programa convierte la entrada, ejecuta el salto en memoria hacia la función objetivo y devuelve el contenido del archivo en pantalla.  
**Flag: picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}**

**Notas Adicionales.** Introduce la explotación de binarios (Pwn) y el concepto de manipulación del flujo mediante punteros. Este ataque directo es posible debido a la falta de mitigaciones modernas en la compilación como PIE (Position Independent Executable), lo que provoca que las direcciones de memoria permanezcan estáticas y predecibles.