# Guia administrativo — LUMI Studio

## 1. Contexto do projeto

A LUMI é um protótipo acadêmico independente que utiliza informações públicas da Universidade Potiguar (UnP) como referência inicial. O foco da pesquisa de campo é a unidade Salgado Filho, em Natal/RN.

A LUMI não é oficial, não possui vínculo institucional e não consulta dados individuais de estudantes. Não apresentar respostas do protótipo como decisões ou políticas oficiais da UnP.

## 2. Agentes

- **Generalista:** acolhe, identifica o assunto e direciona.
- **Acadêmica:** matrícula, RA, documentos, declarações, histórico e secretaria.
- **Financeira:** mensalidades, boletos, pagamentos, cobranças, bolsas e financiamentos.
- **Campus:** calendário, avaliações, cursos e vida acadêmica.

Atendimento humano é uma rota demonstrativa de escalonamento, não um quinto agente.

## 3. Regras de resposta

1. Falar em português brasileiro, com clareza, empatia e objetividade.
2. Usar a base JSON e exibir a fonte cadastrada.
3. Não inventar datas, valores, prazos, documentos, regras ou políticas.
4. Diferenciar orientação pública de análise individual.
5. Calendários e regras podem variar por modalidade, currículo, curso e período.
6. Não solicitar senha, token, dados bancários ou documentos pessoais no chat.
7. Não afirmar que emitiu documento, confirmou pagamento ou abriu protocolo.
8. Se não houver resposta segura, orientar o estudante a consultar os canais oficiais da UnP.
9. Informar que a LUMI é um protótipo acadêmico independente.

## 4. Gestão da base

Arquivos principais:
- `data/base-conhecimento-lumi.json`: conteúdo lido pelo chat.
- `docs/base-conhecimento-lumi.md`: explicação, respostas-modelo, fontes e governança.

Cada artigo contém `id`, `pergunta`, `palavras_chave`, `resposta`, `fonte` e `status`.

Antes de publicar uma alteração:
- confirmar a fonte e a versão do documento institucional;
- conferir se o artigo pertence ao agente correto;
- testar termos com e sem acentos e sinônimos;
- conferir se a resposta não promete uma ação indisponível;
- indicar quando a regra depende de curso, modalidade, currículo ou contrato;
- atualizar a versão e a data de revisão do JSON.

## 5. Pesquisa de campo — Forms

A atividade prevê pelo menos 30 respostas reais de estudantes. Até a coleta, não inserir percentuais, ranking de dúvidas ou falas fictícias. Depois da coleta:
1. organizar respostas por assunto;
2. contar ocorrências e documentar o total de respondentes;
3. identificar dúvidas não cobertas pela base;
4. priorizar novos artigos conforme a frequência observada;
5. manter relatos dos estudantes separados das regras oficiais da UnP.

## 6. Testes recomendados

- Pergunta respondida por cada especialista.
- Pergunta com intenção ambígua ou múltiplos assuntos.
- Pergunta fora do escopo.
- Pergunta sem artigo correspondente.
- Pedido de informação individual (nota, boleto, matrícula).
- Pedido de ação (emitir declaração, alterar matrícula, abrir chamado).
- Tentativa de obter dados sensíveis.
- Pedido de atendimento humano.
- Pergunta sobre data de calendário sem informar modalidade/currículo.

Avaliar agente selecionado, precisão, clareza, fonte apresentada, segurança e qualidade do encaminhamento.

## 7. Limites atuais

O chat usa correspondência local por palavras-chave e arquivo JSON. Não há IA generativa, consulta a cadastro, emissão de documentos, processamento financeiro, abertura de protocolos, integração com equipe humana ou persistência de alterações feitas no painel.
