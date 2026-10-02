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

1. Importe `workflow.template.json` no n8n.
2. Configure suas próprias credenciais para planilha, modelo de IA, PostgreSQL e canal de mensagem.
3. Substitua os campos `REPLACE_WITH_*` e URLs `example.invalid`.
4. Teste com uma planilha e contatos fictícios.
5. Inicie com um fluxo manual; habilite agendamentos apenas após a validação.

## Uso responsável

Use este template exclusivamente com contatos que tenham autorizado a comunicação e respeite regras de consentimento, limites de frequência e políticas do canal utilizado. Dados, mensagens, credenciais e configurações da implementação original foram removidos.

