# Descripción

Este reto de **criptografía RSA** aborda la vulnerabilidad que surge cuando se utilizan **exponentes públicos (e) muy pequeños**, específicamente en casos donde e=3. El desafío consiste en recuperar un mensaje original que ha sido cifrado de tal manera que el valor de M elevado a la potencia de e es apenas superior al módulo n, lo cual permite realizar un ataque de raíz cúbica en lugar de una factorización tradicional.

# Solución

1. **Análisis del problema**: Identificar los valores proporcionados: el texto cifrado (C), el módulo (n) y el exponente público (e=3). Al ser un exponente tan pequeño, el sistema es vulnerable a un ataque de raíz cúbica.
2. **Fundamentación matemática**: Dado que C = M^3 mod n, y considerando la congruencia modular A = KN + B, se establece que el valor buscado es la raíz cúbica de C + (k * n), donde k es un valor desconocido que debe ser hallado mediante fuerza bruta.
3. **Implementación del script**: Se utiliza el lenguaje Python junto con la librería **gmpy2** para realizar cálculos de alta precisión. Se crea un bucle que prueba diferentes valores de "i" (correspondientes a k) hasta encontrar aquel para el cual la raíz cúbica es un número entero exacto.
4. **Descifrado y conversión**: Una vez encontrada la raíz exacta, se convierte el valor entero obtenido (M) primero a bytes y posteriormente a texto (ASCII) para recuperar la flag original.

**Flag: PicoCTF{...}** (El valor exacto varía según la ejecución del script).

# Notas adicionales

- Cuando el exponente "e" es muy pequeño, el ataque de raíz cúbica es más efectivo que intentar factorizar "n".
- La librería **gmpy2** es fundamental para manejar aritmética de precisión arbitraria en este tipo de retos criptográficos.
- La búsqueda del valor "k" puede requerir probar un rango amplio de números antes de hallar el que satisface la condición de ser una raíz cúbica perfecta.