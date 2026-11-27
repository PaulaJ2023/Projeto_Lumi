# Arquitetura proposta — LUMI / Universidade Aurora

## 1. Escopo

A LUMI é uma assistente virtual acadêmica concebida para a **Universidade Aurora (UVA)**, instituição inteiramente fictícia criada para a demonstração do projeto. Seu campus é o Campus Horizonte; o portal do estudante é o Portal Aurora; o ambiente virtual é o Aurora Online.

Nenhuma instituição, marca, política ou sistema real está representado.

## 2. Objetivo

Ajudar estudantes a encontrar orientações sobre serviços acadêmicos, financeiros e vida no campus, com linguagem acolhedora e encaminhamento seguro quando a base não for suficiente.

## 3. Fluxo lógico

1. O estudante envia uma pergunta pelo chat web.
2. O agente generalista identifica a intenção.
3. A pergunta é direcionada a Acadêmica, Financeira ou Campus.
4. O especialista consulta os artigos correspondentes no JSON.
5. A LUMI apresenta a resposta e sugere próximos passos.
6. Quando a informação não existe ou depende de cadastro individual, a LUMI explica o limite e orienta contato com o setor responsável.
7. A opção humana demonstra o encaminhamento à Central de Relacionamento Aurora, sem transferência real na versão atual.

## 4. Agentes e responsabilidades

| Agente | Escopo |
|---|---|
| Generalista | Acolhimento, identificação de intenção e roteamento |
| Acadêmica | Matrícula, rematrícula, documentos, declarações, histórico, protocolos e secretaria |
| Financeira | Mensalidades, pagamentos, cobranças, bolsas, negociação, extrato e estorno |
| Campus | Calendário, avaliações, notas, frequência, cursos, disciplinas, biblioteca, apoio e Aurora Online |

## 5. Componentes

- **Frontend:** interface web em HTML, CSS e JavaScript.
- **Base de conhecimento:** `data/base-conhecimento-lumi.json`.
- **Roteamento atual:** busca local por palavras-chave.
- **Evolução planejada:** n8n para orquestração; modelo de linguagem com recuperação de conteúdo; Supabase para autenticação, artigos, conversas e métricas; Docker opcional para empacotamento.

## 6. Governança da informação

A base é a fonte de verdade do universo ficcional. Cada artigo deve ter identificador, pergunta, palavras-chave, resposta, fonte e status. Regras específicas só podem ser alteradas de forma coordenada para evitar contradições entre artigos e respostas.

A LUMI não deve inventar datas de calendário, valores individuais, notas, frequência ou situação cadastral. Esses dados seriam consultados em sistemas integrados numa versão futura; até lá, o estudante deve consultar o Portal Aurora.

## 7. Segurança

- Não solicitar senhas, tokens, dados bancários ou documentos pessoais pelo chat.
- Não colocar chaves de API no frontend.
- Proteger o painel com autenticação e autorização na versão integrada.
- Minimizar dados armazenados e definir política de retenção.
- Registrar versões e datas de revisão dos artigos.
- Informar claramente que o cenário é fictício.

## 8. Limitações atuais

O protótipo não usa IA generativa e não consulta sistemas acadêmicos ou financeiros. O chat seleciona respostas do JSON por correspondência de palavras-chave. Não emite documentos, confirma pagamentos, altera matrícula, consulta notas ou abre chamados. O painel administrativo não persiste alterações.
