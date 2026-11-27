# Arquitetura — LUMI

## 1. Objetivo e escopo

A LUMI é um protótipo acadêmico independente de assistente virtual universitária, baseado em informações públicas da Universidade Potiguar (UnP) e voltado à experiência de autoatendimento dos estudantes. A proposta é centralizar orientação acadêmica, financeira e de campus em uma conversa única.

A LUMI não é um canal oficial da UnP e, nesta versão, não consulta dados pessoais nem executa operações em sistemas institucionais.

## 2. Agentes

- **LUMI Generalista:** acolhe, identifica a intenção e faz uma pergunta de esclarecimento quando necessário.
- **LUMI Acadêmica:** matrícula, ingresso, rematrícula, RA, documentos, declarações, frequência e secretaria.
- **LUMI Financeira:** mensalidades, boletos, pagamentos, divergências, bolsas e negociação.
- **LUMI Campus:** calendário, avaliações, cursos, biblioteca, ENADE, colação e vida acadêmica.

## 3. Fluxo de resposta atual

1. O estudante escreve livremente.
2. O JavaScript normaliza a pergunta e compara termos e expressões com perguntas e palavras-chave dos artigos.
3. Um mecanismo de pontuação seleciona o artigo mais compatível, exigindo pontuação mínima para evitar encaminhamentos aleatórios.
4. A resposta é apresentada em linguagem natural, com orientação prática.
5. A fonte institucional fica disponível quando o aluno pede a referência ou quando precisa consultar uma informação dinâmica.
6. Quando a pergunta é ambígua, a LUMI pede um esclarecimento; quando envolve dados individuais, explica o limite e ajuda a organizar o pedido.

## 4. Base de conhecimento

Arquivo operacional: `data/base-conhecimento-lumi.json`.

Cada artigo possui identificador, pergunta, palavras-chave, resposta, fonte e status de validação. O conteúdo é separado por agente. Calendários, editais e regras variáveis devem ser conferidos na versão aplicável ao curso, currículo, modalidade e período.

A pesquisa Forms com estudantes será incorporada somente após a coleta real. Não inserir percentuais ou necessidades presumidas.

## 5. Limites técnicos

A versão atual usa HTML, CSS, JavaScript e JSON local. O motor é baseado em regras e recuperação de artigos; ainda não há modelo generativo, banco de dados, autenticação, integração com registros acadêmicos/financeiros ou transferência real para atendentes. O painel administrativo é demonstrativo e não persiste edições.

Para responder perguntas abertas além dos artigos cadastrados, a próxima evolução técnica é integrar um modelo de linguagem no backend com recuperação da base (RAG), preservando fontes e limites de segurança. Chaves de API nunca devem ficar no frontend.

## 6. Segurança e qualidade

- Não solicitar senhas, tokens, dados bancários ou documentos pessoais.
- Não inventar datas, taxas, prazos, regras ou requisitos.
- Diferenciar orientação geral de consulta individual.
- Pedir contexto quando currículo, modalidade, curso ou período alterarem a resposta.
- Responder primeiro; usar links como referência complementar, não como substituto da explicação.
- Testar perguntas reais e registrar lacunas para atualização da base.
