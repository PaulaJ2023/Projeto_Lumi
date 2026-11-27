# Guia administrativo — LUMI Studio

## Objetivo
A LUMI propõe uma experiência centralizada de autoatendimento para estudantes da UnP, com orientação acadêmica, financeira e de campus. É um protótipo acadêmico independente, não um canal oficial.

## Agentes
- **Generalista:** acolhe, identifica intenção e esclarece ambiguidades.
- **Acadêmica:** ingresso, matrícula, documentos, declarações, histórico e frequência.
- **Financeira:** mensalidades, boletos, pagamentos, divergências e bolsas.
- **Campus:** calendário, avaliações, cursos, biblioteca, ENADE e colação.

## Padrão de resposta
1. Responder à dúvida com explicação e passos práticos.
2. Não usar links como substitutos da resposta.
3. Exibir referências apenas quando solicitadas ou necessárias.
4. Pedir contexto quando curso, modalidade, currículo ou período alterarem a resposta.
5. Não inventar datas, valores, prazos ou requisitos.
6. Não solicitar senhas, dados bancários ou documentos pessoais.
7. Não afirmar que consultou dados individuais ou concluiu operações.

## Gestão da base
- Base operacional: `data/base-conhecimento-lumi.json`.
- Documentação: `docs/base-conhecimento-lumi.md` e `base-conhecimento/`.
- Cada artigo deve ter pergunta, palavras-chave, resposta, fonte e status.
- Conferir fontes institucionais e testar perguntas com sinônimos e variações.

## Pesquisa Forms
O formulário está preparado, mas ainda sem respostas. A atividade exige pelo menos 30 respostas reais. Após a coleta, categorizar as dúvidas, identificar recorrências e priorizar novos artigos com base nos dados observados. Não inventar resultados.

## Limites atuais
O chat usa JavaScript e JSON com busca local por expressões e palavras-chave. Ainda não há IA generativa, persistência em banco, autenticação, consulta de cadastro, emissão de documentos, confirmação de pagamentos ou integração de atendimento humano. A próxima evolução para perguntas abertas é integrar um modelo de linguagem no backend com recuperação da base (RAG).