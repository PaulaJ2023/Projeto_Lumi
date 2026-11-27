# LUMI — Sua jornada universitária, mais leve

Projeto acadêmico de assistente virtual universitária. A LUMI foi concebida para atender estudantes da **Universidade Aurora (UVA)**, uma instituição inteiramente fictícia criada para este projeto.

## Universo institucional da LUMI

- **Universidade:** Universidade Aurora (UVA).
- **Campus:** Campus Horizonte.
- **Portal do estudante:** Portal Aurora.
- **Ambiente virtual de aprendizagem:** Aurora Online.
- **Atendimento acadêmico:** Secretaria Acadêmica.
- **Atendimento financeiro:** Central Financeira.
- **Atendimento geral:** Central de Relacionamento Aurora.
- **Biblioteca:** Biblioteca Aurora.

A Universidade Aurora, seus setores, sistemas, procedimentos e regras são fictícios. Não representam uma instituição real, não possuem vínculo institucional e não devem ser usados como orientação para estudantes de universidades reais.

## Acessar

Abra [index.html](./index.html) no navegador. Para carregar a base JSON, utilize um servidor HTTP, como GitHub Pages ou um servidor local.

## Experiência do estudante

- Chat acolhedor em português brasileiro.
- Sugestões de assuntos e próximos passos.
- Identificação do agente responsável.
- Retorno ao menu inicial.
- Opção demonstrativa de encaminhamento humano.
- Respostas consultadas no arquivo `data/base-conhecimento-lumi.json`.

## Agentes

1. **LUMI — Generalista:** acolhe, identifica a intenção e direciona.
2. **LUMI Acadêmica:** matrícula, rematrícula, documentos, declarações, histórico e secretaria.
3. **LUMI Financeira:** mensalidades, pagamentos, cobranças, bolsas, negociação e extrato.
4. **LUMI Campus:** calendário, avaliações, notas, cursos, disciplinas, biblioteca e vida acadêmica.

O atendimento humano é uma rota de encaminhamento, não um agente especialista. No protótipo, a opção apenas demonstra o fluxo e não transfere a conversa a uma equipe real nem abre protocolo.

## Base de conhecimento

O arquivo [base-conhecimento-lumi.json](./data/base-conhecimento-lumi.json) é a fonte de conteúdo do protótipo. Ele contém:
- identidade e descrição da Universidade Aurora;
- regras de comportamento e segurança da LUMI;
- artigos organizados por agente;
- perguntas frequentes, palavras-chave e respostas;
- orientações de encaminhamento e limites de atuação.

Os artigos descrevem procedimentos próprios do universo fictício UVA. Datas específicas, valores individuais, notas, frequência e dados de cadastro não são inventados pelo chatbot: quando dependem de contexto individual ou de calendário vigente, a LUMI orienta a consulta ao Portal Aurora ou ao setor responsável.

### Estrutura de cada artigo

Cada artigo possui `id`, `pergunta`, `palavras_chave`, `resposta`, `fonte` e `status`. A estrutura principal é `categorias → categoria → itens`.

## Área administrativa — LUMI Studio

O painel demonstra visão geral, agentes, prompts, base de conhecimento, laboratório de testes, resultados e histórico. A edição feita na interface ainda não é persistida no arquivo JSON nem em banco de dados.

## Tecnologias e limitações atuais

- Interface: HTML, CSS e JavaScript.
- Base: arquivo JSON versionado no GitHub.
- Roteamento: correspondência local por palavras-chave.
- Ainda não há modelo de IA generativa, Supabase, n8n, autenticação administrativa ou persistência de conversas.
- Indicadores do painel são demonstrativos, não métricas de uso real.

## Estrutura

```
Projeto_Lumi/
├── index.html
├── README.md
├── data/
│   └── base-conhecimento-lumi.json
└── docs/
    ├── arquitetura.md
    ├── guia-administrativo.md
    └── plano-de-evolucao.md
```

## Próximas etapas

Consulte [arquitetura](docs/arquitetura.md), [guia administrativo](docs/guia-administrativo.md) e [plano de evolução](docs/plano-de-evolucao.md).
