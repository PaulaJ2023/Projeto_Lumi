# Plano de evolução — LUMI

## Etapa 1 — Protótipo atual
- [x] Interface web responsiva em português brasileiro.
- [x] Identidade visual e tom acolhedor.
- [x] Visão do estudante e área administrativa.
- [x] Quatro papéis: Generalista, Acadêmica, Financeira e Campus.
- [x] Base JSON organizada por domínio.
- [x] Sugestões rápidas, status e identificação do agente.
- [x] Opção demonstrativa de encaminhamento humano.
- [x] Cenário institucional fictício: Universidade Aurora (UVA).

## Etapa 2 — Aprimorar a base
- [x] Criar universo institucional próprio para a Universidade Aurora.
- [x] Definir Campus Horizonte, Portal Aurora, Aurora Online e setores.
- [x] Criar artigos de matrícula, documentos, secretaria, mensalidades, pagamentos, calendário, avaliações, cursos e vida acadêmica.
- [ ] Criar perguntas alternativas e sinônimos para cada artigo.
- [ ] Criar conjunto de testes de regressão para cada agente.
- [ ] Revisar consistência e cobertura da base com usuários de teste.

## Etapa 3 — Integração
- [ ] Criar projeto Supabase e esquema de dados.
- [ ] Implementar autenticação e perfis administrativos.
- [ ] Criar workflows n8n para entrada, classificação, roteamento e resposta.
- [ ] Conectar modelo de linguagem com prompts versionados.
- [ ] Implementar recuperação de artigos com fontes e controle de versão.
- [ ] Registrar conversas e avaliações com minimização de dados.

## Etapa 4 — Validação
- [ ] Testar perguntas conhecidas, ambíguas e fora do escopo.
- [ ] Testar tentativas de induzir a IA a inventar regras.
- [ ] Testar pedidos de dados individuais e informações sensíveis.
- [ ] Medir precisão do roteamento, utilidade e taxa de encaminhamento.
- [ ] Revisar acessibilidade, responsividade e heurísticas de Nielsen.

## Etapa 5 — Entrega
- [ ] Preparar demonstração de 10 a 15 minutos.
- [ ] Demonstrar perguntas para os três agentes especialistas.
- [ ] Explicar a natureza fictícia da Universidade Aurora.
- [ ] Documentar arquitetura, base, testes, limitações e próximos passos.

## Critério de integração

Uma alteração em artigo ou prompt deverá ser versionada, revisada e testada antes de afetar o atendimento. A interface deverá indicar quando a resposta vem da base e quando não há informação suficiente.
