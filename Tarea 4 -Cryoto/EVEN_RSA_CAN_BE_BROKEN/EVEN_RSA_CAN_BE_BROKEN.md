# Descripción.

El reto proporciona un servicio interactivo escrito en Python que genera llaves RSA y cifra la bandera. Analizando el código fuente, se descubre que la generación de números primos (`get_primes()`) es defectuosa y carece de suficiente entropía. Esto provoca que, al conectarse múltiples veces, el servidor tenga una alta probabilidad de generar exactamente el mismo número primo ($p$) para construir diferentes módulos públicos ($N$). Esta reutilización destruye la seguridad fundamental del algoritmo RSA.

# Solución.

1. Se diseña un script automatizado para conectarse al servidor mediante sockets en dos instancias consecutivas.
    
2. Se capturan dos módulos públicos generados por el servidor: $N_1$ y $N_2$, junto con al menos un texto cifrado $c_1$.
    
3. Se aplica el algoritmo de Euclides para calcular el Máximo Común Divisor (GCD) entre ambos módulos gigantes: $p = \text{gcd}(N_1, N_2)$.
    
4. Al compartir un factor debido a la vulnerabilidad del generador aleatorio, el resultado de la operación nos entrega el primo secreto $p$.
    
5. Se despeja el segundo factor primo dividiendo el módulo original: $q_1 = N_1 / p$.
    
6. Teniendo $p$ y $q_1$, se calcula la función totiente de Euler: $\phi = (p-1) \times (q_1-1)$.
    
7. Se deriva la llave privada $d$ calculando el inverso multiplicativo modular del exponente público $e$ respecto a $\phi$.
    
8. Se descifra matemáticamente el mensaje aplicando la fórmula original $m = c_1^d \pmod{N_1}$ y se decodifican los bytes resultantes a texto plano.
    
    Flag: `picoCTF{tw0_1$_pr!m37dbe6984}`
    

# Notas Adicionales.

Este es un ejemplo clásico de un ataque _Batch GCD_. Nos enseña una lección vital en la criptografía aplicada: la fortaleza de un sistema de cifrado no recae únicamente en lo inquebrantable de su algoritmo, sino en la calidad de su Generador de Números Pseudoaleatorios (PRNG).