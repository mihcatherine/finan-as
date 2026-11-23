# Organização Financeira

Base funcional de um aplicativo mobile/PWA de organização financeira.

## Stack
- HTML, CSS e JavaScript
- Appwrite para autenticação e banco
- PWA com `manifest.webmanifest` e `sw.js`

## Estrutura
- Início
- Lançamentos
- Investimentos
- Análises
- Configurações

## Regras já previstas
- Receitas, despesas e investimentos ficam em `transactions`.
- Pix representa saída imediata.
- Cartão de crédito representa gasto comprometido na fatura.
- Cartões possuem limite, fechamento e vencimento.
- Categorias possuem limite mensal.
- Meta de investimento é persistida em `goals`.
- Configurações de salário/adiantamento são persistidas em `settings`.

## Appwrite
O arquivo `app.js` já aponta para o projeto Appwrite informado no projeto:
endpoint, project ID e database ID.

As tabelas utilizadas são:
profiles, settings, transactions, goals, accounts, categories, bills e cards.

## Próxima etapa recomendada
Criar o fluxo completo de autenticação, adicionar `card_id` e `account_id` em `transactions`, implementar recorrências, parcelas por fatura e o cálculo de saldo por conta. Isso evita duplicidade e permite que o cartão e o Pix sejam calculados de forma realmente integrada.
