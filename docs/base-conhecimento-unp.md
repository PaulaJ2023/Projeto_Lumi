# Base de conhecimento da LUMI — UNP Salgado Filho

## Objetivo
Organizar orientações iniciais para os agentes LUMI Acadêmica, LUMI Financeira e LUMI Campus. O conteúdo foi reunido a partir de páginas públicas da UNP consultadas em 27/11/2026.

## Arquivo utilizado pelo site
- Caminho: `data/base-conhecimento-unp.json`
- Carregamento: `fetch('./data/base-conhecimento-unp.json')`
- Funcionamento atual: correspondência de palavras-chave no navegador.
- O chat exibe a resposta e o endereço da fonte consultada.

## Conteúdo incluído
### Acadêmica
- Consulta do RA no Ulife.
- Processo de matrícula inicial e documentos para candidatos.
- Orientação geral para declarações e históricos, sem inventar prazos.
- Canais institucionais de atendimento.
- Rematrícula: orientação para consultar calendário e manual correspondente ao currículo.

### Financeira
- Localização do boleto e extrato financeiro no Ulife.
- Pagamento não identificado: orientação geral para abrir solicitação e anexar comprovante, conforme manual.
- Boleto vencido e necessidade de consultar nova via.
- Divergência de valor e confirmação de bolsas/descontos pelos canais oficiais.

### Campus
- Calendário acadêmico por período, currículo e modalidade.
- Avaliações A1, A2 e A3 conforme página Sou estudante.
- Significado de UC.
- Catálogo geral de cursos, com alerta para confirmar oferta na unidade.
- Atividades complementares.
- Consulta de notas, materiais e avisos no portal.

## Fontes institucionais
- https://www.unp.br/sou-estudante/
- https://www.unp.br/sou-estudante/calendario/
- https://www.unp.br/sou-candidato/
- https://www.unp.br/cursos/
- https://www.unp.br/wp-content/uploads/2025/03/Manual-Aluno_UNP-Novo-Curriculo-atualizado.pdf
- https://www.unp.br/wp-content/uploads/2025/03/Manual-do-Aluno_UNP_Legado_atualizado.pdf

## Limites e validações necessárias
Esta base não confirma todos os procedimentos específicos da Unidade Salgado Filho. Antes de tratar uma informação como definitiva, validar com a instituição:
- horários, salas e fluxos presenciais da secretaria;
- prazo e eventual taxa de cada declaração/histórico;
- rematrícula e regras específicas por curso, currículo e modalidade;
- datas e horários de cada turma;
- oferta de cursos por unidade, turno e modalidade;
- procedimentos financeiros atuais e situações individuais.

## Como atualizar
Edite o JSON mantendo a estrutura existente. Cada artigo deve incluir pergunta, palavras-chave, resposta, fonte e status. Sempre prefira uma resposta segura que direcione ao canal oficial a uma resposta inventada. Não inclua dados pessoais de alunos, credenciais, valores individualizados ou informações financeiras privadas.

## Próxima etapa técnica
Para transformar o protótipo em atendimento com IA real, o passo seguinte é criar uma API/backend (por exemplo, n8n) que receba a pergunta, recupere os artigos relevantes e envie o contexto a um modelo de linguagem. O Supabase poderá guardar os artigos, conversas e avaliações. Chaves de API nunca devem ficar no HTML/JavaScript público.
