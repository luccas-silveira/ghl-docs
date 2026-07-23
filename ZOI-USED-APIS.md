# APIs GHL usadas pela ZOI

`ghl-docs/` é um espelho externo com centenas de páginas. Não é fonte de verdade da operação ZOI.

## Projetos consumidores conhecidos

- `zoi-lead-qualification`: oportunidades, contatos, usuários, conversas, OAuth, webhooks;
- `sitezoi`: contacts/upsert e tags/custom fields;
- `meta-sync`: oportunidades, agendamentos, qualificação e motivos de perda.

## Para cada endpoint usado, registrar

- projeto consumidor;
- método/rota;
- versão/header;
- scopes;
- payload;
- resposta;
- rate limit;
- comportamento de erro;
- data da última verificação;
- link para a página externa.

## Atualização do espelho

Método, remote e frequência de sincronização ainda precisam ser definidos. Alterações locais no espelho devem ser marcadas como patch da ZOI ou não realizadas.
