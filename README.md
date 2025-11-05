# Circuitos-Logic-Sim
Circuitos criados em aula.


*4-Bit adder*
Entrada A - recebe os 4 bits do primeiro número (A3, A2, A1, A0).
Entrada B - recebe os 4 bits do segundo número (B3, B2, B1, B0).
Soma - representa o resultado da soma dos 4 bits.
Carry out - representa o vai-um final da soma, usado quando o resultado ultrapassa 4 bits.

O 4-bit Adder é um circuito combinacional responsável por somar dois números binários de 4 bits.


*Half-Subtractor*

Entrada A – representa o minuendo, ou seja, o bit do qual será subtraído outro.
Entrada B – representa o subtraendo, o bit que será subtraído de A.
Diferença (D) – indica o resultado da subtração entre A e B.
Empréstimo (Borrow) – sinaliza quando é necessário “emprestar” 1 da próxima casa, ou seja, quando A < B.

O Half-Subtractor é um circuito combinacional responsável por realizar a subtração de dois bits. Ele gera como saída a diferença e o empréstimo, utilizando portas lógicas XOR e AND (com inversão). É a base para circuitos mais complexos, como o Full-Subtractor.