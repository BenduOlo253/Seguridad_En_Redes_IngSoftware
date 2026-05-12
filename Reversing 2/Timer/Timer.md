# Descripción. 
El desafío requiere analizar un paquete de aplicación de Android (`.apk`) para extraer una bandera oculta. Un APK es funcionalmente un archivo comprimido que empaqueta _bytecode_ Dalvik (`classes.dex`), recursos multimedia y archivos de configuración (Manifest). La solución exige aplicar técnicas de ingeniería inversa y análisis estático para inspeccionar las entrañas de la aplicación sin llegar a instalarla ni ejecutarla.

# Solución.
1. Se descarga el paquete de la aplicación `.apk`.
2. Se descomprime manualmente el archivo `.apk` usando herramientas como `unzip` o `apktool` y se usa `grep -Ra "picoCTF{" .` sobre los archivos en crudo.
**Flag: picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}**
    

# Notas Adicionales.
Demuestra cómo el ecosistema de Android retiene la gran mayoría de la estructura lógica, nombres de variables y texto en el _bytecode_ compilado. Esto facilita la reconstrucción de aplicaciones vulnerables casi a su estado original, recalcando la necesidad crítica de ofuscar el código móvil y evitar almacenar secretos incrustados en los binarios de producción.