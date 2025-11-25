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


*Full-Subtractor*

Entrada A – representa o minuendo, o bit do qual será feita a subtração.  
Entrada B – representa o subtraendo, o bit que será subtraído de A.  
Entrada Bi – (Borrow In) indica o empréstimo proveniente de uma subtração anterior (bit menos significativo).  
Diferença (Diff) – resultado final da operação A − B − Bi.  
Empréstimo (Bo) – (Borrow Out) indica se foi necessário “emprestar” 1 da próxima posição binária.  

O Full-Subtractor é um circuito combinacional que realiza a subtração de três bits (A, B e Bi). Ele é composto por dois Half-Subtractors e uma porta OR.
O primeiro Half-Subtractor calcula a diferença entre A e B, e o segundo subtrai o resultado do Borrow In. As saídas de empréstimo dos dois Half-Subtractors são combinadas pela porta OR, gerando o Borrow Out. Esse circuito é utilizado em subtratores binários de múltiplos bits.


*Multiplexador 4-1 (4-to-1 MUX)*

O Multiplexador 4-1 é um circuito combinacional responsável por selecionar uma entre quatro entradas de dados e enviá-la para a saída, de acordo com o valor das linhas de seleção.

Entradas de Dados (D0, D1, D2, D3) – representam os 4 valores possíveis que podem ser encaminhados à saída.
Entradas de Seleção (S0, S1) – determinam qual das entradas de dados será enviada para a saída.
Saída (OUT) – representa o valor selecionado dentre as entradas D0–D3.

O Multiplexador 4-1 funciona como um "seletor digital". Dependendo da combinação das linhas de seleção (S1 S0), apenas uma das entradas é conectada à saída:

| S1 | S0 | Saída |
| -- | -- | ----- |
| 0  | 0  | D0    |
| 0  | 1  | D1    |
| 1  | 0  | D2    |
| 1  | 1  | D3    |

Internamente, o circuito utiliza portas AND, OR e NOT para ativar apenas a entrada correspondente à combinação das linhas de seleção. Esse dispositivo é muito utilizado em arquitetura de computadores, unidades lógicas e sistemas que precisam escolher qual dado será processado.
