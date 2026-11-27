# Arquitetura — LUMI

## 1. Escopo e natureza

A LUMI é um protótipo acadêmico independente de assistente virtual universitária. Sua base inicial utiliza informações públicas da Universidade Potiguar (UnP), com foco de pesquisa nos estudantes da unidade Salgado Filho, em Natal/RN.

A LUMI **não é um canal oficial da UnP**, não possui vínculo institucional e não acessa o Ulife, cadastros, notas, matrículas, boletos ou pagamentos. O projeto não deve ser apresentado como parceria ou serviço institucional.

## 2. Objetivo

Ajudar estudantes a localizar orientações gerais sobre assuntos acadêmicos, financeiros e vida no campus, indicando fontes oficiais e encaminhando casos individuais para os canais adequados.

## 3. Fluxo atual

1. O estudante envia uma pergunta no chat web.
2. O JavaScript normaliza o texto e compara palavras-chave com os artigos do JSON.
3. O artigo mais compatível determina o agente especialista.
4. A interface apresenta a resposta e a fonte cadastrada.
5. Se não houver correspondência, a LUMI informa que não encontrou orientação segura e aponta a página Sou Estudante.
6. A opção de atendimento humano apenas demonstra o encaminhamento; não transfere a conversa nem cria protocolo.

## 4. Agentes

| Agente | Responsabilidade |
|---|---|
| Generalista | Acolhimento, identificação de intenção e encaminhamento |
| LUMI Acadêmica | Matrícula, RA, documentos, declarações, histórico e secretaria |
| LUMI Financeira | Mensalidades, boletos, pagamentos, cobranças, bolsas e financiamentos |
| LUMI Campus | Calendário, avaliações, cursos e vida acadêmica |

Atendimento humano é uma rota de escalonamento, não um agente especialista.

## 5. Componentes

- **Frontend:** `index.html`, com HTML, CSS e JavaScript.
- **Base operacional:** `data/base-conhecimento-lumi.json`.
- **Documentação editorial:** `docs/base-conhecimento-lumi.md`.
- **Roteamento:** busca local por palavras-chave.
- **Evolução planejada:** n8n para orquestração, modelo de linguagem com recuperação de conteúdo e Supabase para autenticação, artigos, conversas e métricas. Docker poderá ser usado para empacotamento.

## 6. Modelo de artigo

Cada item do JSON possui:
- `id`: identificador único;
- `pergunta`: pergunta principal;
- `palavras_chave`: termos para localizar o artigo;
- `resposta`: orientação exibida no chat;
- `fonte`: link institucional para conferência;
- `status`: condição editorial/necessidade de validação.

A estrutura é `categorias → categoria → itens`. Cada categoria também identifica o agente responsável.

## 7. Segurança e governança

- Não solicitar senhas, tokens, dados bancários ou documentos pessoais.
- Não inserir chaves de API no frontend.
- Não inventar datas, valores, prazos, documentos obrigatórios ou políticas.
- Não declarar que uma operação individual foi concluída.
- Calendários, editais, manuais e procedimentos devem ser conferidos em suas versões vigentes.
- Informações dependentes de contrato, modalidade, currículo ou cadastro devem ser encaminhadas ao canal oficial.
- Registrar fonte, status e data de revisão de cada artigo.
- Separar regras institucionais de relatos e necessidades apontados pelos participantes da pesquisa.

## 8. Integração futura

A versão integrada deverá proteger o painel com autenticação e autorização, manter segredos no backend, aplicar políticas de acesso no banco, limitar retenção de conversas e minimizar dados pessoais. A recuperação de conteúdo deverá retornar fontes e versões dos artigos.

## 9. Limitações atuais

O protótipo não usa IA generativa e não consulta sistemas acadêmicos ou financeiros. Seleciona respostas do JSON por palavras-chave. Não emite documentos, confirma pagamentos, altera matrícula, consulta notas, abre chamados ou transfere conversas para atendentes. O painel administrativo não persiste alterações.
