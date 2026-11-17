# Sistema Bancário em Python (POO)

Sistema bancário de terminal desenvolvido em Python, aplicando Programação Orientada a Objetos. Permite cadastrar clientes, criar contas correntes e realizar depósitos, saques e consulta de extrato.

## Funcionalidades
- Cadastro de novo usuário (pessoa física), com verificação de CPF duplicado
- Criação de conta corrente vinculada a um cliente (agência 0001, número sequencial)
- Depósito (apenas valores positivos)
- Saque com limite de R$ 500,00 por operação e máximo de 3 saques por conta
- Extrato com data e hora de cada movimentação e saldo atual
- Listagem de todas as contas cadastradas
- Tratamento de valores inválidos digitados no terminal

## Conceitos aplicados
- Classes e objetos
- Herança (`PessoaFisica` herda de `Cliente`; `ContaCorrente` herda de `Conta`)
- Classes abstratas e métodos abstratos (`Transacao`, com `Deposito` e `Saque`)
- Encapsulamento com atributos privados e `@property`
- Polimorfismo (`ContaCorrente` sobrescreve o método `sacar`)
- Métodos de classe (`nova_conta`)
- Organização do código em funções

## Estrutura das classes
- `Transacao` (abstrata) → `Deposito`, `Saque`
- `Historico`: guarda as transações com tipo, valor e data
- `Cliente` → `PessoaFisica`
- `Conta` → `ContaCorrente`

## Tecnologias
- Python 3 (apenas bibliotecas padrão: `abc` e `datetime`)

## Como executar
1. Instale o Python 3
2. Baixe os arquivos deste repositório
3. No terminal, dentro da pasta do projeto, execute:
   python sistema_bancario_poo_projeto.py

## Menu
| Opção | Ação |
|-------|------|
| d  | Depositar |
| s  | Sacar |
| e  | Extrato |
| nu | Novo usuário |
| nc | Nova conta |
| lc | Listar contas |
| q  | Sair |

## Autor
Gabriel Chaves Pereira
