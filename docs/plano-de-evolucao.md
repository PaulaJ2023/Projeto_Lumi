# Plano de evolução

## Etapa 1 — Protótipo atual
- [x] Visão do aluno em página web.
- [x] Alternância para área administrativa.
- [x] Telas demonstrativas de agentes, prompts, conhecimento, testes, resultados e histórico.
- [x] Identidade visual em português brasileiro.
- [ ] Testes de usabilidade com estudantes.

## Etapa 2 — Preparar conteúdo
- [ ] Realizar pesquisa de campo com pelo menos 30 estudantes reais, conforme orientação do trabalho.
- [ ] Consolidar dúvidas frequentes e priorizar funcionalidades.
- [ ] Criar base inicial do caso fictício Instituto Horizonte.
- [ ] Revisar respostas e fontes com a equipe/professor.

## Etapa 3 — Integração
- [ ] Criar projeto Supabase e esquema de dados.
- [ ] Implementar autenticação e papéis administrativos.
- [ ] Criar workflows n8n para entrada, classificação, roteamento e resposta.
- [ ] Conectar o modelo de linguagem com prompts versionados.
- [ ] Conectar recuperação de conteúdo à base de conhecimento.
- [ ] Registrar conversas e eventos de avaliação.

## Etapa 4 — Validação
- [ ] Montar conjunto de perguntas reais anonimizadas.
- [ ] Medir qualidade das respostas e encaminhamentos.
- [ ] Testar perguntas fora do escopo e tentativas de induzir respostas inventadas.
- [ ] Revisar acessibilidade, responsividade e heurísticas de Nielsen.
- [ ] Documentar limitações e próximos passos.

## Critério de integração
Alterar um prompt ou artigo no painel deverá refletir no atendimento real, com controle de acesso, registro de versão e possibilidade de teste antes da publicação.
