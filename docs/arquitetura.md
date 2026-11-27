# Arquitetura proposta — LUMI

## Contexto e escopo
A LUMI é uma proposta acadêmica criada por estudantes da **UNP — Unidade Salgado Filho**, a partir de uma pesquisa de campo com alunos reais dessa unidade. A pesquisa deve reunir no mínimo 30 respostas e identificar necessidades de autoatendimento, conforme o enunciado do professor.

O enunciado também estabelece um **case fictício**, “Instituto Horizonte — Central de Atendimento ao Aluno”. Para manter aderência à atividade, esse cenário pode ser usado na demonstração técnica, nos exemplos e nos dados simulados. A UNP Salgado Filho é o contexto real da pesquisa e inspiração; o Instituto Horizonte é o cenário fictício do case. A LUMI não é um serviço oficial da UNP.

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

## Pesquisa de campo e uso dos dados
- Aplicar o formulário a pelo menos 30 estudantes reais da UNP — Salgado Filho.
- A pergunta central deve investigar o que gostariam de encontrar no autoatendimento via WhatsApp da UNP, conforme o professor.
- Apresentar resultados agregados, sem expor nomes, matrículas, telefones ou outras informações pessoais.
- Usar os achados para priorizar temas e funcionalidades; não inventar respostas nem percentuais.
- Separar claramente resultados reais da pesquisa e dados simulados do protótipo.

## Segurança e governança
- Exigir autenticação e autorização para o painel administrativo.
- Nunca expor chaves de API no navegador ou no repositório.
- Não solicitar nem armazenar senhas de estudantes.
- Minimizar dados pessoais e definir retenção de conversas.
- Registrar fontes e datas de atualização da base.
- Não inventar datas, valores, prazos ou políticas da UNP.
- Só incluir conteúdo institucional real após validação em fonte oficial ou por responsável autorizado.
- Oferecer encaminhamento humano quando não houver resposta confiável.

## Limite do protótipo
O `index.html` simula roteamento por palavras-chave. Não há conexão com n8n, Supabase ou provedor de IA.
