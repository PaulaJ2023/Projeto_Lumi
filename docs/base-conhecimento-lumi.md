# Base de conhecimento da LUMI

## Objetivo e escopo

A LUMI é um protótipo acadêmico independente que propõe centralizar orientações para estudantes da Universidade Potiguar (UnP), com foco de pesquisa na unidade Salgado Filho, em Natal/RN. O conteúdo inicial utiliza páginas e documentos públicos da universidade.

A LUMI não é um canal oficial da UnP. Nesta versão, não consulta cadastros individuais, não emite documentos, não confirma pagamentos e não abre protocolos.

A base operacional carregada pelo chat está em `data/base-conhecimento-lumi.json`. Ela contém 29 artigos organizados por agente, com pergunta, palavras-chave, resposta, fonte e status de validação.

## Regras de resposta

1. Responder primeiro à pergunta, com explicação e passos práticos.
2. Não substituir a resposta por um link. A fonte é complementar e só deve aparecer quando solicitada ou quando for indispensável consultar uma informação dinâmica.
3. Se faltar contexto, fazer uma pergunta curta e específica.
4. Distinguir orientação geral de análise individual.
5. Não inventar datas, valores, prazos, documentos obrigatórios, regras ou políticas.
6. Pedir modalidade, currículo, curso ou período quando isso alterar a orientação.
7. Não solicitar senhas, tokens, dados bancários ou documentos pessoais no chat.
8. Não afirmar que consultou cadastro, emitiu documento, confirmou pagamento ou abriu protocolo.
9. Quando a base não cobrir a dúvida, explicar o que falta e ajudar o estudante a organizar os próximos passos.

## Agentes

### LUMI Acadêmica
Abrange ingresso, matrícula, rematrícula, RA, documentos, declarações, histórico, frequência e secretaria. Deve distinguir candidato de estudante já matriculado. Requisitos e prazos variam por edital, curso, currículo e modalidade.

### LUMI Financeira
Abrange mensalidades, boletos, pagamentos não identificados, divergências, bolsas, financiamentos e negociação. Não calcula encargos nem confirma saldos ou acordos individuais.

### LUMI Campus
Abrange calendário, avaliações, cursos, biblioteca, ENADE, colação de grau e vida acadêmica. Calendários e critérios devem ser associados ao currículo, modalidade e período corretos.

### LUMI Generalista
Recebe a pergunta, identifica o assunto e pede esclarecimento quando houver mais de uma interpretação.

## Fontes institucionais usadas

- [Sou Estudante](https://www.unp.br/sou-estudante/)
- [Sou Candidato](https://www.unp.br/sou-candidato/)
- [Calendário Acadêmico](https://www.unp.br/sou-estudante/calendario/)
- [Manual do Aluno](https://www.unp.br/sou-estudante/manual-do-aluno/)
- [Biblioteca](https://www.unp.br/sou-estudante/biblioteca/)
- [Colação de Grau](https://www.unp.br/sou-estudante/colacao-de-grau/)
- [ENADE](https://www.unp.br/sou-estudante/enade/)
- [Ouvidoria](https://ouvidoria.unp.br/)
- [Assessoria Financeira](https://www.unp.br/sobre/assessoria-financeira/)

## Pesquisa de campo

O formulário já foi elaborado, mas ainda não possui respostas. A atividade exige pelo menos 30 respostas reais. Não inserir conclusões, percentuais ou ranking de necessidades antes da coleta. Depois, classificar as respostas por assunto e usar os resultados para priorizar novos artigos, mantendo relatos de estudantes separados das regras institucionais.

## Limites técnicos atuais

O chat usa JavaScript e recuperação local de artigos em JSON, com pontuação de palavras-chave e expressões. Ainda não utiliza IA generativa, banco de dados, autenticação ou integração com sistemas institucionais. Para responder perguntas abertas que não estejam previstas nos artigos, a próxima etapa é integrar um modelo de linguagem no backend com recuperação da base (RAG).