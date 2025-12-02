# Circuitos-Logic-Sim

Circuitos criados em aula utilizando o software **Digital Logic Sim (Sebastian Lague)** para estudo de circuitos combinacionais e blocos fundamentais de arquitetura de computadores.

---

## **4-Bit Adder**

**Entradas:**

* **A** – primeiro número de 4 bits (A3, A2, A1, A0)
* **B** – segundo número de 4 bits (B3, B2, B1, B0)

**Saídas:**

* **Soma** – resultado da soma dos 4 bits
* **Carry Out** – vai-um gerado quando o resultado ultrapassa 4 bits

O **4-bit Adder** é um circuito combinacional responsável por somar dois números binários de 4 bits. Seu funcionamento geralmente se baseia em uma cadeia de Full-Adders (ripple-carry adder), onde o carry se propaga de um bit ao seguinte.

---

## **Half-Subtractor**

**Entradas:**

* **A** – minuendo
* **B** – subtraendo

**Saídas:**

* **Diferença (D)**
* **Empréstimo (Borrow)** – ativado quando A < B

O **Half-Subtractor** realiza a subtração de dois bits utilizando portas XOR e AND com inversão. É um circuito base para a construção de subtratores mais completos.

---

## **Full-Subtractor**

**Entradas:**

* **A** – minuendo
* **B** – subtraendo
* **Borrow In (Bi)** – empréstimo de uma operação anterior

**Saídas:**

* **Diferença (Diff)**
* **Borrow Out (Bo)**

O **Full-Subtractor** realiza a subtração de três bits (A − B − Bi). Ele é composto por dois Half-Subtractors e uma porta OR para combinar os sinais de empréstimo. É utilizado para implementar subtratores binários de múltiplos bits.

---

## **Multiplexador 4–1 (4-to-1 MUX)**

O multiplexer 4–1 seleciona **uma entre quatro entradas** e a envia para a saída com base nas linhas de seleção.

**Entradas de Dados:** D0, D1, D2, D3
**Linhas de Seleção:** S1, S0
**Saída:** OUT

| S1 | S0 | Saída |
| -- | -- | ----- |
| 0  | 0  | D0    |
| 0  | 1  | D1    |
| 1  | 0  | D2    |
| 1  | 1  | D3    |

O MUX funciona como um **seletor digital**, permitindo que apenas uma entrada seja conectada à saída. É fundamental em ALUs, sistemas de escolha de dados, e circuitos de controle.

---

## **ALU 4-bit (Arithmetic Logic Unit)**

A **ALU de 4 bits** é o circuito responsável por executar operações aritméticas e lógicas entre dois operandos de 4 bits. Ela representa um dos blocos essenciais da CPU, onde ocorrem cálculos, comparações e operações de manipulação de bits.

### **Entradas**

* **A (A3–A0)** – primeiro operando de 4 bits
* **B (B3–B0)** – segundo operando de 4 bits
* **Linhas de Controle (C0, C1, C2)** – determinam qual operação será executada

### **Saídas**

* **Resultado (R3–R0)** – resultado final de 4 bits
* **Flags opcionais:**

  * **Carry Out** – estouro na soma
  * **Borrow Out** – empréstimo na subtração
  * **Zero** – indica se o resultado é 0
  * **Overflow** – sinaliza estouro aritmético

### **Operações implementadas**

A ALU implementa várias operações por meio de blocos individuais:

* **SOMA (ADD)** – soma de 4 bits usando ripple-carry
* **SUBTRAÇÃO (SUB)** – usando Full-Subtractors ou complemento de dois
* **AND 4-bit** – operação lógica bit a bit
* **OR 4-bit** – operação lógica bit a bit
* **XOR 4-bit** – operação exclusiva bit a bit

### **Arquitetura interna**

* Um **DEMUX** direciona as entradas para o bloco correspondente da operação selecionada.
* Cada operação é processada independentemente.
* Um **MUX** coleta os resultados e, com base nos sinais de controle, envia apenas o resultado desejado para a saída.

Assim, a ALU funciona como um centro de decisões aritméticas e lógicas, semelhante às unidades presentes em processadores reais.

