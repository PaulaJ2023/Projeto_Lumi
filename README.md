# LUMI — Sua jornada universitária, mais leve

Projeto de extensão de IA conversacional desenvolvido por uma dupla de estudantes da **UNP — Unidade Salgado Filho**.

## Contexto correto do projeto
A proposta nasce da realidade dos estudantes da UNP Salgado Filho: a pesquisa de campo deve ser aplicada a pelo menos 30 alunos reais dessa unidade, investigando quais informações e serviços eles gostariam de encontrar em um canal de autoatendimento. A atividade do professor define como pergunta central o que o aluno gostaria de ter no autoatendimento via WhatsApp da UNP.

**Importante distinguir duas coisas:**
- **Pesquisa e inspiração:** estudantes reais da UNP — Salgado Filho. Os resultados orientarão prioridades, funcionalidades e linguagem da LUMI.
- **Case técnico da atividade:** o PDF do professor define o cenário fictício “Instituto Horizonte — Central de Atendimento ao Aluno”. Para respeitar o enunciado, a demonstração técnica e exemplos de base podem usar esse case fictício.
- **Status da LUMI:** protótipo acadêmico independente. Não é canal oficial, produto, parceria ou sistema institucional da UNP. Não usar marca/logotipo oficial sem autorização nem apresentar conteúdo inventado como política da universidade.

## Acessar
Abra **[index.html](./index.html)** no navegador. O protótipo é estático e não exige instalação.

## Duas áreas
- **Visão do aluno:** chat acolhedor, atalhos por assunto, sugestões de próximos passos, indicador de status, retorno ao menu e opção de solicitar orientação humana. O encaminhamento humano é demonstrativo e ainda não abre chamado real.
- **LUMI Studio:** visão geral, agentes, prompts, base de conhecimento, laboratório de testes, resultados e histórico.

## Agentes previstos
1. **Generalista:** acolhe, identifica intenção e encaminha.
2. **Acadêmica:** matrícula, documentos, declarações e secretaria.
3. **Financeira:** mensalidades e pagamentos.
4. **Campus:** calendário, avaliações, cursos e vida acadêmica.

O atendimento humano é uma rota de encaminhamento, não um agente especialista.

## Canal de atendimento
O enunciado menciona o autoatendimento via WhatsApp na pesquisa, mas permite implementar a interação por **web chat ou WhatsApp**. A versão atual é web, conforme a escolha do grupo. A pesquisa deve perguntar sobre as necessidades no canal mencionado pelo professor, mesmo que o protótipo demonstrado seja web.

## Tecnologias planejadas
- Interface web: HTML, CSS e JavaScript (protótipo atual).
- Orquestração: n8n.
- Banco de dados e base de conhecimento: Supabase.
- Modelo de linguagem: a definir e justificar na documentação técnica.
- Docker: opcional para empacotamento.

## Estado atual e limitações
Este repositório contém um **protótipo de interface**, não uma aplicação com IA integrada. As respostas usam regras simples por palavras-chave. Prompts e itens da base podem ser editados na interface, mas não persistem. Ainda não há autenticação administrativa, banco de dados, API ou integração com n8n/modelo de linguagem. Indicadores ilustrativos não são dados reais.

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
