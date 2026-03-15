# Descripción.

There is some interesting information hidden around this site. Can you find it?http://wily-courier.picoctf.net:63956/
**Pistas:**
1. You should have enough hints to find the files, don't run a brute forcer.

# Solución.

1. **Analizar la página**: Al abrir el sitio web del reto, se observan dos pestañas y una introducción al uso de HTML, CSS y JavaScript para la creación del sitio.
2. **Inspeccionar código fuente**: Al revisar el código fuente HTML, se encuentra el primer comentario con **la primera parte de la bandera:** picoCTF{t.
3. **Revisar hojas de estilo**: Se examina el enlace a la hoja de estilos CSS, donde se encuentra en un comentario **la segunda parte de la bandera:** h4ts_4_l0.
4. **Buscar robots.txt**: Se prueba acceder a `/robots.txt` para buscar pistas de indexación, encontrando **la tercera parte de la bandera**: t_0f_pl4c y una indicación sobre servidores Apache.
5. **Revisar archivos de configuración**: Se intenta acceder al archivo de configuración `.htaccess`. Debido a una mala configuración de permisos del servidor, el archivo es accesible y revela **la cuarta parte de la bandera**: 3s_2_lO0k y una pista sobre archivos de Mac.
6. **Buscar archivos ocultos de Mac**: Finalmente, se accede al archivo `.DS_Store` (típico de sistemas macOS) para obtener **la quinta y última parte de la bandera**: _9588550}

**Flag: picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_9588550}**

# Notas Adicionales.

- El reto enseña a buscar información crítica en archivos que **teóricamente deberían estar ocultos** o ser inaccesibles al público.
-  `.htaccess` es un archivo de configuración para servidores Apache.
- `.DS_Store` es un archivo de sistema de Apple que almacena información de configuración de carpetas.

# Referencias.

https://youtu.be/E2gN3AGHirc?si=UfVtqhqwoGNny7e0