# prg04sgcrweb

**SGCR - Sistema de Gestão de Contas a Receber**

O SGCR é um sistema financeiro e ERP de vendas voltado para o varejo. Originalmente construído como uma aplicação desktop em Java com Swing, o projeto está em processo de migração para uma arquitetura Web (cliente-servidor).

O principal diferencial do sistema é o seu módulo de contas a receber com foco em vendas a prazo (crédito direto em loja). Ele resolve o problema do controle informal de crédito, fornecendo à gerência ferramentas para monitorar clientes devedores, histórico de compras pendentes e conciliação de pagamentos, além de operar com as funções transacionais padrão de um ERP.

## Funcionalidades Principais
- **Gestão de Vendas a Prazo:** Controle de transações baseadas em crédito da loja, com atribuição de dívidas diretamente ao perfil do cliente.
- **Monitoramento de Inadimplência:** Painel gerencial para visualização de clientes em atraso, montantes em aberto e relatórios de vencimento.
- **Operações de ERP Padrão:** Registro de vendas, fluxo de caixa e controle de saída de produtos.
- **Gestão de Clientes:** Cadastro e rastreamento completo do histórico de compras, limites de crédito e liquidações.

## Arquitetura e Estrutura do Projeto

O projeto adota uma **Arquitetura Modular** (também conhecida como *Feature-Based* ou *Orientada a Domínio/Funcionalidades*). Essa separação organiza os arquivos por contexto ou módulo. Isso evita o acoplamento excessivo e impede que a base de código se desorganize conforme novas funcionalidades forem incorporadas.

### Árvore de Diretórios (Base Primária)
O foco atual é estabelecer a base estrutural primária, sem a necessidade de criar antecipadamente todas as pastas de módulos de negócio. A estrutura inicial está definida da seguinte forma:

```plaintext
prg04sgcrweb/
├── .gitattributes
├── .gitignore
├── README.md
├── admin/                 # Módulo de Administração: Dashboard e gerenciamento
├── auth/                  # Módulo de Autenticação: Centraliza login e controle de acesso
├── infrastructure/       # Módulo Global: Centraliza páginas e assets gerais e transversais do site
│   ├── assets/
│   │   ├── css/
│   │   ├── images/
│   │   │   ├── favicon.ico
│   │   │   ├── icon-atvd03.ico
│   │   │   ├── foto-p.png
│   │   │   ├── foto-m.png
│   │   │   └── foto-g.png
│   │   └── js/
│   └── pages/
│       ├── index.html
│       └── atividade-3.html