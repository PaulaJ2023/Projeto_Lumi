# LUMI — Sua jornada universitária, mais leve

A LUMI é um **protótipo acadêmico independente de assistente virtual universitária**, desenvolvido em português brasileiro. A base inicial usa informações públicas da Universidade Potiguar (UnP), com foco de pesquisa nos estudantes da unidade Salgado Filho, em Natal/RN.

> **Importante:** a LUMI não é um canal oficial da UnP, não possui vínculo institucional, não consulta cadastros individuais nem consulta dados pessoais, acadêmicos ou financeiros. As respostas são orientações gerais e devem ser confirmadas nos canais oficiais.

## Acessar o protótipo

Abra [index.html](./index.html) por um servidor HTTP, como GitHub Pages ou servidor local, para que o navegador carregue o arquivo JSON da base.

## Agentes

1. **LUMI — Generalista:** acolhe, identifica a intenção e direciona.
2. **LUMI Acadêmica:** matrícula, RA, documentos, declarações, histórico e secretaria.
3. **LUMI Financeira:** mensalidades, boletos, pagamentos, cobranças, bolsas e financiamentos.
4. **LUMI Campus:** calendário, avaliações, cursos e vida acadêmica.

O atendimento humano é uma rota demonstrativa de encaminhamento, não um quinto agente. Não existe transferência real nem abertura de protocolo.

## Base de conhecimento

A fonte utilizada pelo chat é [data/base-conhecimento-lumi.json](./data/base-conhecimento-lumi.json). A documentação editorial completa está em [docs/base-conhecimento-lumi.md](./docs/base-conhecimento-lumi.md).

A base:
- separa artigos por agente;
- contém perguntas, palavras-chave, respostas, fontes e status de validação;
- utiliza links institucionais públicos da UnP;
- marca assuntos que exigem confirmação individual ou consulta a calendário/edital vigente;
- não contém resultados do Forms, pois a pesquisa com estudantes ainda será realizada.

## Pesquisa com estudantes

A pesquisa de campo deverá reunir **pelo menos 30 respostas reais de estudantes da UnP**, conforme a atividade. Os resultados serão analisados separadamente das regras institucionais. As respostas do formulário ajudarão a identificar prioridades e dúvidas frequentes, mas não comprovam políticas oficiais da universidade.

## Experiência do estudante

- Chat responsivo e acolhedor.
- Sugestões de assuntos e próximos passos.
- Identificação do agente especialista.
- Respostas carregadas do JSON.
- Exibição da fonte para conferência.
- Opção demonstrativa de atendimento humano.

## Área administrativa — LUMI Studio

O painel contém visão geral, agentes, prompts, base de conhecimento, laboratório de testes, resultados e histórico. As métricas são locais e demonstrativas. Alterações feitas nos campos do painel não são persistidas no JSON ou em banco de dados.

## Tecnologias e limites atuais

- Interface: HTML, CSS e JavaScript.
- Base: JSON versionado no GitHub.
- Roteamento: correspondência local por palavras-chave.
- Não há IA generativa, Supabase, n8n, autenticação administrativa ou integração com sistemas da UnP.
- Não consulta matrícula, notas, boletos ou pagamentos individuais.
- Não emite documentos nem abre chamados.

## Estrutura

```
Projeto_Lumi/
├── index.html
├── README.md
├── data/
│   └── base-conhecimento-lumi.json
└── docs/
    ├── arquitetura.md
    ├── base-conhecimento-lumi.md
    ├── guia-administrativo.md
    └── plano-de-evolucao.md
```

## Documentação

- [Base de conhecimento](docs/base-conhecimento-lumi.md)
- [Arquitetura](docs/arquitetura.md)
- [Guia administrativo](docs/guia-administrativo.md)
- [Plano de evolução](docs/plano-de-evolucao.md)

## Fontes institucionais principais

- [Sou Estudante](https://www.unp.br/sou-estudante/)
- [Calendário acadêmico](https://www.unp.br/sou-estudante/calendario/)
- [Manual do aluno](https://www.unp.br/sou-estudante/manual-do-aluno/)
- [Cursos](https://www.unp.br/cursos/)
- [Sou Candidato](https://www.unp.br/sou-candidato/)
- [LUMI]()
