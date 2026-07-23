> Status: Canônico
> Owner: Luccas — até delegação formal
> Revisor: Luccas
> Versão: v1.0
> Atualizado em: 2026-07-23
> Próxima revisão: após mudanças relevantes nas integrações GHL
> Fonte: manifesto autoral da ZOI sobre APIs GHL efetivamente usadas

# APIs GHL usadas pela ZOI

Este arquivo é a exceção autoral da ZOI dentro de `ghl-docs/`: é um manifesto mantido no mirror para registrar as APIs efetivamente usadas pela ZOI. O restante de `ghl-docs/` continua sendo documentação externa importada e não fonte de verdade da operação ZOI.

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
