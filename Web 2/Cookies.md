# Descripción.
Who doesn't love cookies? Try to figure out the best one.http://wily-courier.picoctf.net:49520/
# Solución.
1. Ingrese al sitio web indicado.
2. Abri el modo desarrollador y cheque las cookies.
3. solo habia una con el nombre y el valor.
4. comence a editar las cookies, encontrando diferentes valores, sin embargo, no lanzaba la bandera, habria que probar varios valores, por lo que habria que hacerlo iterativamente.
5. En la terminal use un for, cambiando los valores hasta encontrar la bandera, filtrando los resultados con un grep.
**Flag: picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}**
# Notas Adicionales.
Este reto incita a buscar maneras de variar valores de manera iterativa desde terminal.
# Referencias.
https://www.youtube.com/watch?v=LseQ-XWCXVo&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=12

