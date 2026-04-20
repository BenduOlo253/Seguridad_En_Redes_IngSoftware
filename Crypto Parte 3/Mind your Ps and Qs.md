# Descripción

Este reto de **criptografía RSA** explora cómo la seguridad del algoritmo depende de la dificultad de **factorizar el número n** en sus componentes primos p y q. El desafío consiste en recuperar una flag cuando los factores de n no son lo suficientemente grandes, lo que permite romper la seguridad del sistema mediante factorización.

# Solución

1. **Obtención de datos**: Descargar el archivo proporcionado que contiene el texto cifrado, el valor n y el exponente público e (65537).
2. **Factorización**: Utilizar una herramienta de factorización (como un script en JavaScript) para descomponer n en sus factores primos p y q. Este proceso puede tomar varios minutos dependiendo de la potencia de cómputo.
3. **Cálculo de la clave privada**:
    - Calcular la función totient de Euler (phi) como (p-1) * (q-1).
    - Determinar el **inverso multiplicativo modular** de e respecto a phi.
4. **Descifrado**: Elevar el texto cifrado a la potencia de la clave privada (mod n) para obtener el mensaje original.
5. **Conversión**: Convertir el resultado obtenido en formato hexadecimal a texto ASCII para revelar la flag final.

**Flag: picoCTF{sma11_N_n0_g0od_1dc7ae91}**
# Notas adicionales

- La robustez de RSA depende de que n sea un número extremadamente grande; si los factores son pequeños, el sistema es vulnerable a ataques de factorización.
- Se recomienda el uso de scripts automatizados o herramientas de línea de comandos para manejar las operaciones matemáticas complejas.
- La flag recuperada en este ejercicio es: `picoCTF{small_n_no_good}`.

# Referencias.
https://www.youtube.com/watch?v=-ixz-2gi9r0