# Descripción. 
Se proporciona un archivo compilado de Java (`.class`) que simula una caja fuerte virtual. El objetivo es recuperar la clave de acceso codificada. Al estar en formato _bytecode_ de la máquina virtual de Java, el archivo no es directamente un texto legible, pero preserva sus cadenas estáticas sin ningún tipo de cifrado, lo que expone credenciales directamente incrustadas en el código (hardcoding).

# Solución.

1. Se descarga el archivo `.class` a la máquina local.
    
2. Se utiliza el comando de terminal `strings archivo.class | grep picoCTF` para extraer todas las secuencias de caracteres legibles y localizar la bandera inmediatamente.

**Flag: picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_de45efd6}**

# Notas Adicionales.
Ilustra de forma práctica la vulnerabilidad de _Hardcoding_. Escribir contraseñas o datos sensibles directamente en el código fuente es una de las peores prácticas de seguridad, puesto que la compilación a ejecutables o a _bytecode_ no cifra los datos ni protege los strings de herramientas básicas de análisis.