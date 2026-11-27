# LUMI — Sua jornada universitária, mais leve

A LUMI é um protótipo acadêmico independente de assistente virtual universitária, em português brasileiro, com foco de pesquisa nos estudantes da UnP — unidade Salgado Filho, Natal/RN. A proposta é centralizar orientações acadêmicas, financeiras e de campus em uma conversa.

> A LUMI é um protótipo acadêmico, não um canal oficial da UnP. A versão atual não consulta cadastros pessoais nem executa operações institucionais.

## Agentes
1. **LUMI Generalista:** acolhe e identifica a intenção.
2. **LUMI Acadêmica:** ingresso, matrícula, documentos, declarações, frequência e secretaria.
3. **LUMI Financeira:** mensalidades, boletos, pagamentos, cobranças, bolsas e negociação.
4. **LUMI Campus:** calendário, avaliações, cursos, biblioteca, ENADE e vida acadêmica.

## Base de conhecimento
O chat consulta `data/base-conhecimento-lumi.json`, com artigos organizados por agente, palavras-chave, respostas explicativas, fontes institucionais e status de validação. A base foi ampliada para responder dúvidas frequentes com passos práticos. Links são complementares: a LUMI deve explicar primeiro e mostrar a fonte quando solicitada ou necessária para consultar informação dinâmica.

A pesquisa Forms ainda não possui respostas. A atividade exige pelo menos 30 respostas reais; nenhum resultado foi presumido ou inventado.

## Funcionamento técnico atual
- Interface: HTML, CSS e JavaScript.
- Conteúdo: JSON versionado no GitHub.
- Motor: busca local por expressões e palavras-chave com pontuação de compatibilidade.
- Não há ainda IA generativa, Supabase, n8n, autenticação ou integração com dados pessoais.
- A LUMI orienta e organiza solicitações, mas não consulta matrícula, saldo, notas ou pagamentos, não emite documentos e não abre protocolos.

## Próxima evolução
Integrar um modelo de linguagem no backend com recuperação da base de conhecimento (RAG), registro seguro das conversas e persistência dos indicadores. Segredos de API nunca devem ficar no frontend.

## Fontes institucionais consultadas
- [Sou Estudante](https://www.unp.br/sou-estudante/)
- [Sou Candidato](https://www.unp.br/sou-candidato/)
- [Calendário Acadêmico](https://www.unp.br/sou-estudante/calendario/)
- [Manual do Aluno](https://www.unp.br/sou-estudante/manual-do-aluno/)
- [Biblioteca](https://www.unp.br/sou-estudante/biblioteca/)
- [Colação de Grau](https://www.unp.br/sou-estudante/colacao-de-grau/)
- [ENADE](https://www.unp.br/sou-estudante/enade/)
- [Ouvidoria](https://ouvidoria.unp.br/)
- [Assessoria Financeira](https://www.unp.br/sobre/assessoria-financeira/)
