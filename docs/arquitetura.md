# Arquitetura proposta — LUMI

## Objetivo
Oferecer atendimento universitário simples para estudantes e uma área administrativa para configurar, testar e acompanhar a assistente.

## Fluxo lógico
1. O estudante envia uma pergunta pela interface web.
2. O agente generalista identifica a intenção.
3. A solicitação é encaminhada ao agente especialista (Acadêmica, Financeira ou Campus).
4. O agente consulta a base de conhecimento pertinente.
5. A resposta retorna ao chat.
6. Conversa, assunto, resultado e eventual encaminhamento são registrados para análise.
7. Se a informação não existir ou não for confiável, a LUMI informa a limitação e orienta atendimento humano.

## Componentes planejados
- **Frontend web:** interface do estudante e LUMI Studio administrativo.
- **n8n:** orquestra classificação, roteamento e chamadas de IA.
- **Modelo de linguagem:** gera respostas a partir de instruções e conteúdo recuperado.
- **Supabase:** autenticação, conversas, agentes, prompts, documentos e eventos analíticos.
- **Base de conhecimento:** conteúdos por domínio, com fonte, responsável e data de revisão.
- **Docker:** opção para empacotar serviços próprios.

## Agentes
| Agente | Responsabilidade |
|---|---|
| Generalista | Boas-vindas, intenção, triagem e roteamento |
| Acadêmica | Matrícula, documentos, declarações e secretaria |
| Financeira | Mensalidades, pagamentos e orientações financeiras |
| Campus | Calendário, avaliações, cursos e vida acadêmica |

Atendimento humano é um mecanismo de escalonamento.

## Segurança e governança
- Exigir autenticação e autorização para o painel administrativo.
- Nunca expor chaves de API no navegador ou no repositório.
- Não solicitar nem armazenar senhas de estudantes.
- Minimizar dados pessoais e definir retenção de conversas.
- Registrar fontes e datas de atualização da base.
- Não inventar datas, valores, prazos ou políticas.
- Oferecer encaminhamento humano quando não houver resposta confiável.

## Limite do protótipo
O `index.html` simula roteamento por palavras-chave. Não há conexão com n8n, Supabase ou provedor de IA.
