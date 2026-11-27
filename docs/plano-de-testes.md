# Plano de testes — LUMI

## Objetivo

Verificar se o protótipo identifica corretamente o assunto, seleciona o agente especialista adequado, responde com orientação geral apoiada na base e trata limites sem inventar informações.

## Casos de roteamento

| Pergunta de teste | Agente esperado | Verificação principal |
|---|---|---|
| Como faço para renovar minha matrícula? | LUMI Acadêmica | Diferenciar matrícula inicial de rematrícula e não inventar prazo |
| Preciso de uma declaração de matrícula | LUMI Acadêmica | Explicar o tipo de documento e os limites de emissão |
| Onde encontro meu RA? | LUMI Acadêmica | Não solicitar CPF nem afirmar que consultou cadastro |
| Meu boleto venceu. Como resolvo? | LUMI Financeira | Não calcular juros ou prometer segunda via |
| Meu pagamento não apareceu | LUMI Financeira | Orientar a guardar comprovante e pedir conferência financeira |
| Como consulto o calendário acadêmico? | LUMI Campus | Solicitar modalidade/currículo quando necessário |
| Como funcionam as provas A1, A2 e A3? | LUMI Campus | Não inventar pesos ou fórmula de média |
| Quais serviços a biblioteca oferece? | LUMI Campus | Explicar serviços e indicar fonte complementar |
| Quero reclamar de um atendimento | LUMI Campus | Explicar quando a Ouvidoria pode ser adequada |
| Pergunta fora da base | LUMI Generalista | Pedir esclarecimento e não inventar resposta |

## Testes de interação

1. Enviar uma pergunta pelo campo de texto e pelo botão Enviar.
2. Usar os atalhos rápidos de matrícula, financeiro e calendário.
3. Selecionar Menu e confirmar que a conversa volta à saudação inicial.
4. Pedir atendimento humano pelo botão e por uma frase digitada.
5. Solicitar a fonte de uma resposta e verificar que o link é complementar à explicação.
6. Abrir a área administrativa e confirmar que o histórico mostra apenas perguntas enviadas pelo aluno na sessão atual.
7. Executar perguntas no laboratório de testes e confirmar que elas não entram nas estatísticas das mensagens dos alunos.
8. Adicionar um rascunho na tela da base e confirmar que a interface informa que ele não altera o JSON.

## Testes de sentimento

Usar somente como verificação funcional da estimativa lexical, não como avaliação psicológica ou conclusão sobre estudantes:

- Exemplo negativo: “Estou insatisfeito com esse erro e quero uma solução.”
- Exemplo positivo: “Muito obrigado, a orientação ajudou.”
- Exemplo neutro: “Onde encontro o calendário acadêmico?”

A classificação é simplificada e pode errar em frases com ironia, negação, ambiguidade ou palavras positivas e negativas na mesma mensagem. O painel deve continuar identificando o resultado como estimativa.

## Critérios de aprovação

- A pergunta é direcionada ao agente esperado nos casos previstos.
- Respostas não inventam datas, valores, taxas, regras, prazos ou status individuais.
- O texto explica os próximos passos e não substitui a resposta por um link.
- Pedidos fora do escopo recebem esclarecimento ou orientação segura.
- O pedido de atendimento humano não afirma que ocorreu transferência real.
- Indicadores são identificados como dados da sessão, sem serem confundidos com resultados do Forms.
- Nenhuma estatística da pesquisa é apresentada antes da coleta mínima de 30 respostas reais.

## Limitações conhecidas

O motor atual é baseado em regras e palavras-chave. O roteiro deve ser executado manualmente no navegador após cada atualização. A integração com IA generativa, banco de dados, WhatsApp, n8n, Supabase e atendimento humano real ainda não está implementada.
