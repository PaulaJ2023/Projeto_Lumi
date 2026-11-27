# LUMI — Sua jornada universitária, mais leve

Projeto de extensão universitária: assistente virtual de atendimento acadêmico com duas experiências conectadas — área do estudante e painel administrativo.

## Acessar
Abra **[index.html](./index.html)** no navegador. O protótipo é estático e não exige instalação.

## Duas áreas
- **Visão do aluno:** chat demonstrativo, atalhos e central de ajuda.
- **LUMI Studio:** visão geral, agentes, prompts, base de conhecimento, laboratório de testes, resultados e histórico.

## Agentes previstos
1. **Generalista:** acolhe, identifica intenção e encaminha.
2. **Acadêmica:** matrícula, documentos, declarações e secretaria.
3. **Financeira:** mensalidades e pagamentos.
4. **Campus:** calendário, avaliações, cursos e vida acadêmica.

O atendimento humano é uma rota de encaminhamento, não um agente especialista.

## Tecnologias planejadas
- Interface web: HTML, CSS e JavaScript (protótipo atual).
- Orquestração: n8n.
- Banco de dados e base de conhecimento: Supabase.
- Modelo de linguagem: a definir e justificar na documentação técnica.
- Docker: opcional para empacotamento.

## Estado atual e limitações
Este repositório contém um **protótipo de interface**, não uma aplicação com IA integrada. As respostas usam regras simples por palavras-chave. Prompts e itens da base podem ser editados na interface, mas não persistem. Ainda não há autenticação administrativa, banco de dados, API ou integração com n8n/modelo de linguagem. Indicadores ilustrativos não são dados reais.

O caso **Instituto Horizonte é fictício**. Não apresentar informações inventadas como regras oficiais de uma instituição real. A pesquisa de campo deve ser feita com estudantes reais e relatada separadamente.

## Estrutura
```
Projeto_Lumi/
├── index.html
├── README.md
└── docs/
    ├── arquitetura.md
    ├── guia-administrativo.md
    └── plano-de-evolucao.md
```

## Próximos passos
Consulte [plano de evolução](docs/plano-de-evolucao.md), [arquitetura](docs/arquitetura.md) e [guia administrativo](docs/guia-administrativo.md).
