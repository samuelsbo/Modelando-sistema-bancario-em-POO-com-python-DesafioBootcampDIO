# Sistema Bancário em Python

Bem-vindo ao **Sistema Bancário em Python**, um projeto robusto desenvolvido para simular operações bancárias completas utilizando a linguagem de programação Python.

## Sumário

- [Descrição](#descrição)
- [Funcionalidades](#funcionalidades)
  - [Menu Principal](#menu-principal)
  - [Gestão de Usuários](#gestão-de-usuários)
    - [Novo Usuário](#novo-usuário)
  - [Gestão de Contas](#gestão-de-contas)
    - [Nova Conta](#nova-conta)
    - [Listar Contas](#listar-contas)
  - [Operações Financeiras](#operações-financeiras)
    - [Depósito](#depósito)
    - [Saque](#saque)
    - [Extrato](#extrato)
- [Bibliotecas Utilizadas](#bibliotecas-utilizadas)
- [Autor](#autor)

## Descrição

O **Sistema Bancário em Python** é uma aplicação de console que permite aos usuários realizar operações bancárias completas, incluindo:

- **Gestão de Usuários**: Criação e gerenciamento de perfis de usuários.
- **Gestão de Contas**: Criação e listagem de contas bancárias associadas aos usuários.
- **Operações Financeiras**: Depósitos, saques e visualização de extratos.
- **Histórico de Transações**: Registro detalhado de todas as transações realizadas.

O sistema é estruturado utilizando princípios de programação orientada a objetos, garantindo uma organização clara e facilitando futuras expansões ou manutenções.

## Funcionalidades

### Menu Principal

O **Menu Principal** é a interface principal do sistema, onde o usuário pode selecionar a operação desejada. As opções disponíveis são:

- **[d] Depositar**: Permite ao usuário adicionar fundos à sua conta.
- **[s] Sacar**: Permite ao usuário retirar fundos da sua conta, com restrições aplicáveis.
- **[e] Extrato**: Exibe o histórico de transações realizadas na conta.
- **[nc] Nova Conta**: Permite a criação de uma nova conta bancária associada a um usuário existente.
- **[lc] Listar Contas**: Lista todas as contas bancárias existentes no sistema.
- **[nu] Novo Usuário**: Permite a criação de um novo perfil de usuário.
- **[q] Sair**: Encerra o sistema.

### Gestão de Usuários

#### Novo Usuário

A funcionalidade de **Novo Usuário** permite a criação de um novo perfil de usuário no sistema. O usuário deve fornecer:

- **CPF**: Cadastro de Pessoa Física (somente números).
- **Nome Completo**: Nome completo do usuário.
- **Data de Nascimento**: Formato `dd-mm-aaaa`.
- **Endereço**: Endereço completo (logradouro, número, bairro, cidade/estado).

O sistema verifica se já existe um usuário com o CPF informado. Caso exista, a criação do usuário é cancelada para evitar duplicidades.

### Gestão de Contas

#### Nova Conta

A funcionalidade de **Nova Conta** permite a criação de uma nova conta bancária associada a um usuário existente. O usuário deve fornecer o CPF do titular da conta. Se o usuário existir, a conta é criada com sucesso; caso contrário, a operação é cancelada.

#### Listar Contas

A funcionalidade de **Listar Contas** exibe uma lista de todas as contas bancárias existentes no sistema, mostrando detalhes como:

- **Agência**: Número da agência bancária.
- **C/C**: Número da conta corrente.
- **Titular**: Nome do usuário associado à conta.

### Operações Financeiras

#### Depósito

A funcionalidade de **Depósito** permite que o usuário adicione um valor positivo ao saldo da conta. O sistema valida se o valor informado é positivo antes de realizar a operação. Caso o valor seja inválido (não positivo), a operação é cancelada e uma mensagem de erro é exibida.

#### Saque

A funcionalidade de **Saque** permite que o usuário retire fundos da sua conta, obedecendo às seguintes restrições:

- **Saldo Insuficiente**: O valor do saque não pode exceder o saldo disponível.
- **Limite de Saque**: Há um limite máximo por saque (R$ 500,00).
- **Número de Saques**: O usuário pode realizar no máximo 3 saques por dia.

Se alguma dessas condições não for atendida, o sistema informa o motivo da falha na operação.

#### Extrato

A funcionalidade de **Extrato** exibe o histórico de todas as transações realizadas pelo usuário, incluindo depósitos e saques. Além disso, mostra o saldo atual da conta. Se nenhuma movimentação tiver sido realizada, o sistema informa que não há movimentações para exibir.

## Bibliotecas Utilizadas

- **textwrap**: Utilizado para formatar o menu e a listagem de contas de forma limpa e organizada.
- **abc (Abstract Base Classes)**: Utilizado para criar classes abstratas, garantindo que as classes derivadas implementem métodos específicos.
- **datetime**: Utilizado para registrar a data e hora das transações.

## Autor

Este projeto foi desenvolvido por Samuel Batista, baseado nas orientações do tutor Guilherme Arthur de Carvalho (@decarvalhogui). Sinta-se à vontade para entrar em contato ou contribuir com melhorias!
