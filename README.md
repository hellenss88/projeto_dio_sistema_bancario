# 🚀 DIO – Back-end com Python  
## Desafio de Projeto: **Otimizando o Sistema Bancário com Funções Python**

> **Instrutor:** Guilherme Carvalho  
> **Objetivo:** Refatorar e otimizar o sistema bancário previamente desenvolvido, encapsulando as operações de **depósito**, **saque** e **extrato** em **funções específicas**, favorecendo **reutilização**, **organização** e **manutenibilidade** do código.

---

## ✨ Visão Geral

Neste desafio, você aprimora a arquitetura de um sistema bancário em console utilizando **funções puras**, parâmetros **posicionais** e **nomeados**, além de uma separação clara de responsabilidades.  
A proposta é demonstrar domínio de conceitos fundamentais de Python aplicados a um mini-projeto de regras de negócio.

---

## 🧩 Funcionalidades

- **[d] Depositar** — adiciona valor ao saldo e registra no extrato  
- **[s] Sacar** — respeita limite por transação e número máximo de saques diários  
- **[e] Extrato** — imprime todas as movimentações e o saldo atual  
- **[nu] Novo usuário** — cadastro com **CPF**, nome, data de nascimento e endereço  
- **[nc] Nova conta** — cria conta associada a um usuário existente (agência padrão)  
- **[lc] Listar contas** — exibe as contas cadastradas  
- **[q] Sair** — encerra o programa

> **Regras de negócio (principais):**  
> • Limite de saques diários: **2**  
> • Limite por saque: **R$ 1.000,00**  
> • Agência padrão: **0001**

---

## 🏗️ Arquitetura de Funções (resumo)

- `menu()` → Interface textual do menu  
- `depositar(saldo, valor, extrato, /)` → Exemplo de uso de **parâmetros posicionais-apenas**  
- `sacar(*, saldo, valor, extrato, limite, numero_saques, limite_saques)` → Exemplo de **parâmetros nomeados-apenas**  
- `exibir_extrato(saldo, /, *, extrato)` → Combinações de parâmetros com semântica explícita  
- `criar_usuario(usuarios)` / `filtrar_usuario(cpf, usuarios)`  
- `criar_conta(agencia, numero_conta, usuarios)` / `listar_contas(contas)`  
- `main()` → Laço principal de interação

---

## 🗺️ Fluxo (Mermaid)

```mermaid
flowchart TD
    A[Início] --> B[Exibir MENU]
    B -->|d| C[Depositar]
    B -->|s| D[Sacar]
    B -->|e| E[Extrato]
    B -->|nu| F[Novo Usuário]
    B -->|nc| G[Nova Conta]
    B -->|lc| H[Listar Contas]
    B -->|q| Z[Fim]
    C --> B
    D --> B
    E --> B
    F --> B
    G --> B
    H --> B
