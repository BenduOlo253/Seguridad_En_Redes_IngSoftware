# Descripción.

Encuentra la bandera escondida en el servidor cambiando los métodos de solicitud HTTP para **adelantarte en la competencia.**

# Solución.

1. **Analizar la página**: Al entrar, se observan botones para cambiar el color de fondo a rojo o azul.
2. **Inspeccionar código fuente**: Al revisar el HTML, se nota que el botón rojo usa el método **GET**, mientras que el botón azul usa **POST**.
3. **Identificar la pista**: El nombre del reto "GET aHEAD" sugiere usar el método **HEAD**.
4. **Modificar la solicitud**: Usando las herramientas de desarrollador en la pestaña de red, se puede reenviar una solicitud cambiando el método a **HEAD**.
5. **Obtener la bandera**: La bandera se encuentra en los encabezados de respuesta de la solicitud **HEAD**.

**Flag: picoCTF{r3j3ct_m3th0d_9528020d}**

# Notas Adicionales.

# Referencias.

https://www.youtube.com/watch?v=LseQ-XWCXVo