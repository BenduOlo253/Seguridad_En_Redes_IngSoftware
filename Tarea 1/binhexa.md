# Descripción.
How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 51010`
# Solución.
1. Me conecte al enlace.
2. comence a resolver las operaciones.
$ nc titan.picoctf.net 51010

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 11110011
Binary Number 2: 01101101


Question 1/6:
Operation 1: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01100001
Correct!

Question 2/6:
Operation 2: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 11100110
Incorrect. Try again
Enter the binary result: 11100110
Incorrect. Try again
Enter the binary result: 01111001
Incorrect. Try again
Enter the binary result: 00110110
Incorrect. Try again
Enter the binary result: 111100110
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0110011101110111
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 101100000
Correct!

Question 5/6:
Operation 5: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11111111
Correct!

Question 6/6:
Operation 6: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01111001
Incorrect. Try again
Enter the binary result: 01111001^[[D

Incorrect input. Provide the right input
Enter the binary result: 011110010
Incorrect. Try again
Enter the binary result: 001111001
Incorrect. Try again
Enter the binary result: 0 1 1 1 1 0 0 1

Incorrect input. Provide the right input
Enter the binary result: 01111001
Incorrect. Try again
Enter the binary result: 00110110
Correct!

Enter the results of the last operation in hexadecimal: 0x36

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_1367e2c6}

**Flag: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_1367e2c6}**

# Notas Adicionales.
# Referencias.