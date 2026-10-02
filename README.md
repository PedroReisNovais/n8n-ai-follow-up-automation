# Follow-up Automatizado com IA no n8n

Template de automação para organizar follow-ups de contatos autorizados, combinando agenda, planilhas, IA, memória de conversa e registro de status.

## Problema resolvido

Equipes comerciais perdem contexto quando o acompanhamento é manual ou ocorre em várias ferramentas. Este fluxo organiza uma cadência de follow-up, usa contexto armazenado para personalização e registra o resultado de cada interação.

## Fluxo

```text
Agendamento
  -> Google Sheets: leitura de contatos e regras
  -> Loop por contato elegível
  -> IA: preparação da mensagem
  -> PostgreSQL: memória de conversa
  -> Canal de mensagem configurado
  -> Espera / próxima etapa da cadência
  -> Google Sheets: atualização de status
```

## Tecnologias e integrações

- n8n
- Google Sheets
- Modelo de linguagem da OpenAI
- PostgreSQL para memória de conversa
- Evolution API como conector de canal de mensagem
- Loops, waits e agendamentos do n8n

## Como importar

1. Importe `workflow.template.json` no n8n para visualizar a arquitetura e as conexões entre nós.
2. Configure novamente os parâmetros de cada nó com suas próprias credenciais, fontes e regras de negócio.
3. Teste com uma planilha e contatos fictícios.
4. Inicie com um fluxo manual; habilite agendamentos apenas após a validação.

## Uso responsável

Use este template exclusivamente com contatos que tenham autorizado a comunicação e respeite regras de consentimento, limites de frequência e políticas do canal utilizado. Esta versão preserva apenas a arquitetura: dados, mensagens, credenciais, parâmetros e configurações da implementação original foram removidos.

