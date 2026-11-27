# Plano de evolução — LUMI

## Etapa 1 — Protótipo web
- [x] Interface responsiva em português brasileiro.
- [x] Identidade visual acolhedora.
- [x] Visão do estudante e área administrativa.
- [x] Generalista e três agentes especialistas.
- [x] Chat consulta arquivo JSON local.
- [x] Sugestões rápidas, status e identificação do agente.
- [x] Exibição da fonte cadastrada.
- [x] Opção demonstrativa de encaminhamento humano.
- [x] Aviso de que a LUMI é um protótipo acadêmico independente.

## Etapa 2 — Base de conhecimento UnP
- [x] Criar base inicial com referências públicas da UnP.
- [x] Organizar artigos por Acadêmica, Financeira e Campus.
- [x] Registrar fonte e status de validação nos artigos.
- [x] Documentar limites e situações de encaminhamento.
- [ ] Conferir cada artigo com a versão vigente dos manuais e páginas institucionais.
- [ ] Ampliar sinônimos e perguntas alternativas.
- [ ] Criar testes de regressão por agente.

## Etapa 3 — Pesquisa com estudantes
- [ ] Aplicar Forms a pelo menos 30 estudantes reais da UnP.
- [ ] Consolidar respostas sem fabricar dados.
- [ ] Categorizar dúvidas acadêmicas, financeiras e de campus.
- [ ] Comparar necessidades relatadas com a cobertura atual da base.
- [ ] Priorizar artigos novos conforme os resultados.
- [ ] Documentar método, período, número de respondentes e limitações.

## Etapa 4 — Integração técnica
- [ ] Criar projeto Supabase e esquema de dados.
- [ ] Implementar autenticação e perfis administrativos.
- [ ] Criar workflows n8n para entrada, classificação, roteamento e resposta.
- [ ] Conectar modelo de linguagem com prompts versionados.
- [ ] Implementar recuperação de artigos com fontes e controle de versão.
- [ ] Registrar conversas e avaliações com minimização de dados.
- [ ] Proteger chaves e segredos exclusivamente no backend.

## Etapa 5 — Validação e entrega
- [ ] Testar perguntas conhecidas, ambíguas e fora do escopo.
- [ ] Testar tentativas de induzir a IA a inventar regras.
- [ ] Testar pedidos de dados individuais e informações sensíveis.
- [ ] Medir precisão do roteamento e utilidade das respostas.
- [ ] Revisar acessibilidade, responsividade e heurísticas de Nielsen.
- [ ] Preparar apresentação de 10 a 15 minutos e demonstração.
- [ ] Documentar arquitetura, base, pesquisa, testes, limitações e próximos passos.

## Critério de qualidade

Toda resposta institucional deve estar ligada a uma fonte identificável. Informações específicas devem ser marcadas como pendentes de validação. Resultados da pesquisa com estudantes nunca devem ser apresentados como regra oficial da universidade.
