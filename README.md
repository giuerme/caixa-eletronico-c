# Sistema de Caixa Eletrônico em C

# Sobre o Projeto

O **Sistema de Caixa Eletrônico** é um projeto acadêmico desenvolvido em linguagem C durante a graduação em Ciência da Computação, como parte de uma atividade prática universitária.

O objetivo é simular o funcionamento de um caixa eletrônico, permitindo realizar operações de saque, verificar o saldo disponível e calcular automaticamente a distribuição das cédulas necessárias.

O desenvolvimento do projeto teve como foco a aplicação de conceitos fundamentais de programação estruturada, raciocínio lógico, estruturas condicionais e operações aritméticas.

---

## Funcionalidades

O sistema apresenta as seguintes funcionalidades:

- **Consulta de saldo:** exibição do saldo disponível para saque.
- **Solicitação de saque:** entrada de valores inteiros pelo usuário.
- **Validação de entrada:** verificação de valores inválidos.
- **Verificação de saldo:** bloqueio de operações superiores ao saldo disponível.
- **Distribuição de cédulas e moedas:** cálculo automático das denominações necessárias para o saque.
- **Composição do valor solicitado:** distribuição de qualquer valor inteiro positivo dentro do saldo, utilizando também a moeda de R$ 1.
- **Atualização de saldo:** desconto do valor sacado após uma operação válida.
- **Tratamento de erros:** apresentação de mensagens para operações não permitidas.

### Cédulas disponíveis

| Cédula | Valor |
|---|---|
| 100 | R$ 100 |
| 50 | R$ 50 |
| 20 | R$ 20 |
| 10 | R$ 10 |
| 5 | R$ 5 |
| 2 | R$ 2 |
| Moeda de 1 | R$ 1 |

O sistema utiliza as cédulas acima e a moeda de R$ 1, permitindo compor qualquer valor inteiro positivo dentro do saldo disponível.

---

## Tecnologias Utilizadas

| Tecnologia | Aplicação |
|---|---|
| Linguagem C | Desenvolvimento do algoritmo |
| Biblioteca `stdio.h` | Entrada e saída de dados |
| `scanf()` | Leitura de informações |
| `printf()` | Exibição dos resultados |
| Estruturas condicionais | Validação das operações |
| Operadores aritméticos | Cálculo das cédulas |

### Conceitos aplicados

- Programação estruturada
- Variáveis e tipos primitivos
- Estruturas condicionais
- Operadores aritméticos
- Divisão inteira e operador módulo
- Validação de dados
- Algoritmos e lógica de programação

---

## Funcionamento do Sistema

O algoritmo segue uma sequência de etapas para processar as solicitações de saque.

**1. Inicialização**

O sistema inicia com um saldo disponível de R$ 1.000,00.

**2. Entrada de dados**

O usuário informa o valor que deseja sacar.

**3. Validação**

O programa verifica se o valor informado é válido, se existe saldo suficiente e se o saque pode ser realizado utilizando as cédulas disponíveis.

**4. Distribuição das cédulas**

Após a validação, o algoritmo calcula uma combinação de cédulas e, quando necessário, moedas de R$ 1 que corresponde ao valor solicitado.

**5. Atualização do saldo**

Após uma operação bem-sucedida, o valor sacado é descontado do saldo disponível.

### Exemplo de distribuição

Para um saque de **R$ 95,00**, o sistema pode realizar a seguinte distribuição:

```text
1 nota(s) de R$ 50
2 nota(s) de R$ 20
1 nota(s) de R$ 5
```

Total distribuído: R$ 95,00.

Saldo restante: R$ 905,00.

---

## Exemplo de Execução

### Saque válido

```text
=== CAIXA ELETRONICO ===

Saldo disponivel: R$ 1000
Digite o valor do saque: R$ 95

Saque realizado com sucesso!
Valor sacado: R$ 95

Distribuicao das cedulas:
1 nota(s) de R$ 50
2 nota(s) de R$ 20
1 nota(s) de R$ 5

Saldo restante: R$ 905
```

### Saldo insuficiente

```text
=== CAIXA ELETRONICO ===

Saldo disponivel: R$ 1000
Digite o valor do saque: R$ 1005

Erro: saldo insuficiente.
```

---

## Testes e Validação

Os testes têm como objetivo verificar o comportamento do programa em diferentes situações.

| Cenário | Valor | Resultado esperado |
|---|---|---|
| Saque simples | R$ 50 | Operação realizada |
| Saque com múltiplas cédulas | R$ 95 | Distribuição correta |
| Saque com combinação alternativa | R$ 123 | Operação realizada com combinação válida |
| Saldo insuficiente | R$ 1.005 | Operação recusada |
| Valor inválido | R$ 0 | Operação recusada |
| Valor negativo | R$ -10 | Operação recusada |

No cenário de R$ 123, o programa distribui 1 nota de R$ 100, 1 nota de R$ 20, 1 nota de R$ 2 e 1 moeda de R$ 1.

---

## Como Executar

### Pré-requisitos

- Compilador C (GCC ou equivalente).
- Terminal ou ambiente de desenvolvimento compatível com C.

### 1. Obtenha o projeto

Clone o repositório ou baixe o código-fonte disponibilizado no GitHub.

### 2. Compile o código

No terminal, execute:

```bash
gcc caixa_eletronico_em_c.c -o caixa_eletronico
```

### 3. Execute o programa

**Windows:**

```bash
.\caixa_eletronico.exe
```

**Linux/macOS:**

```bash
./caixa_eletronico
```

### 4. Utilize o sistema

Informe um valor inteiro para saque e acompanhe o resultado apresentado no terminal.

---

## Limitações

O sistema foi desenvolvido com finalidade educacional e possui algumas limitações:

- Saldo inicial fixo de R$ 1.000,00.
- Uma operação de saque por execução.
- Ausência de autenticação de usuários.
- Sem integração com banco de dados.
- Sem armazenamento permanente de transações.
- Sem controle físico do estoque de cédulas.

---

## Contexto Acadêmico

Este projeto foi desenvolvido no ambiente universitário, durante o curso de **Ciência da Computação da Universidade Cidade de São Paulo (UNICID)**, como parte de uma atividade prática voltada ao desenvolvimento de algoritmos em linguagem C.

A proposta teve como finalidade aplicar conhecimentos adquiridos em sala de aula, especialmente relacionados à lógica de programação, estruturas condicionais, manipulação de variáveis e resolução de problemas computacionais.

Além da implementação do sistema, a atividade envolveu a análise do funcionamento do algoritmo e a realização de testes para verificar seu comportamento em diferentes cenários.

---

## Conclusão

O desenvolvimento do **Sistema de Caixa Eletrônico em C** proporcionou a aplicação prática de conceitos fundamentais da programação estruturada.

A implementação permitiu explorar a construção de algoritmos, a validação de dados e o uso de operações matemáticas para solucionar um problema inspirado em situações reais.

O projeto contribuiu para o desenvolvimento do raciocínio lógico e para a consolidação dos conhecimentos adquiridos durante a graduação, além de representar uma experiência prática para o portfólio acadêmico e profissional.

---

**Projeto acadêmico desenvolvido durante a graduação em Ciência da Computação — UNICID.**
