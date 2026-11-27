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
## Acessar pesquisa 
- **Forms** [Link](https://docs.google.com/forms/d/e/1FAIpQLSfFFicaYkwS5v6d5wIOos3mm5JJpA2McIQC93cKxcObgwqB0w/viewform)

- **Respostas** [Link](https://docs.google.com/forms/d/1K65vBgRUYxiEN2L__sX1qlxAd32D2Ff38kmqOYsUblY/edit)

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

## Base de conhecimento da LUMI

O arquivo `data/base-conhecimento-lumi.json` contém artigos demonstrativos nas categorias Acadêmica, Financeira e Campus. O conteúdo foi estruturado a partir de temas comuns encontrados em referências públicas universitárias, mas foi reescrito como orientação genérica: não representa a UNP, não reproduz políticas institucionais e não deve ser apresentado como informação oficial de qualquer universidade.

A base inclui perguntas frequentes sobre matrícula, rematrícula, documentos, declarações, secretaria, mensalidades, boletos, pagamentos, bolsas, calendário, avaliações, cursos, disciplinas, biblioteca e apoio estudantil. Quando faltam dados específicos, a LUMI orienta o estudante a consultar o portal ou setor responsável, sem inventar datas, valores ou prazos.

**Integração atual:** o `index.html` carrega esse JSON com `fetch('./data/base-conhecimento-lumi.json')`. O chat percorre as palavras-chave dos artigos e apresenta a resposta com maior correspondência. Portanto, a base já alimenta a demonstração web, mas isso ainda não é uma integração com IA generativa, Supabase ou n8n. O navegador precisa abrir o site por um servidor HTTP (por exemplo, GitHub Pages); abrir o HTML diretamente como arquivo pode bloquear o `fetch()`.

Para editar a base, atualize o JSON mantendo a estrutura `categorias → categoria → itens`. Cada artigo possui `id`, `pergunta`, `palavras_chave`, `resposta`, `fonte` e `status`. Os links em `referencias_de_inspiracao` servem apenas para documentar os temas que inspiraram a organização; não transformam as respostas em políticas da instituição citada.

## Estado atual e limitações
Este repositório contém um **protótipo de interface**, não uma aplicação com IA integrada. As respostas usam regras simples por palavras-chave consultando o arquivo JSON. O arquivo JSON é versionado no GitHub; itens adicionados pelo formulário administrativo ainda não persistem. Ainda não há autenticação administrativa, banco de dados, API ou integração com n8n/modelo de linguagem. Indicadores ilustrativos não são dados reais.

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
