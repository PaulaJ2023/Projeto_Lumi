# Base de conhecimento da LUMI — UnP Salgado Filho

## Objetivo e escopo

Organizar orientações gerais para estudantes da Universidade Potiguar (UnP), com foco de pesquisa na unidade Salgado Filho, em Natal/RN. O conteúdo operacional utilizado pelo chat está em:

- [data/base-conhecimento-lumi.json](../data/base-conhecimento-lumi.json)

A LUMI é um protótipo acadêmico independente. Não é canal oficial da UnP, não possui vínculo institucional e não acessa sistemas acadêmicos ou financeiros. Não consultar cadastros, notas, frequência, boletos individuais ou pagamentos; não emitir documentos nem abrir protocolos.

## Agentes especialistas

### LUMI Acadêmica
- Ingresso e matrícula.
- Rematrícula e orientações sobre vínculo.
- RA, documentos, declarações e histórico.
- Frequência e encaminhamento à secretaria.

### LUMI Financeira
- Mensalidades e boletos.
- Pagamentos não identificados.
- Divergências de cobrança.
- Bolsas, financiamentos e preparação para negociação.

### LUMI Campus
- Calendário acadêmico.
- Avaliações e orientações sobre notas.
- Cursos e modalidades.
- Biblioteca, ENADE, colação de grau e vida acadêmica.

O agente generalista recebe a pergunta, identifica a intenção e direciona para o especialista. O atendimento humano é uma orientação de encaminhamento; ainda não existe transferência automática ou abertura real de chamado.

## Padrão obrigatório das respostas

1. Responder primeiro com explicação em linguagem simples e passos práticos, sempre que a base permitir.
2. Não substituir a explicação por um link. Apresentar a fonte como complemento, quando solicitada ou necessária para conferir uma informação dinâmica.
3. Se faltar contexto, fazer uma pergunta curta e específica.
4. Pedir curso, modalidade, currículo, unidade ou período quando esses dados mudarem a orientação.
5. Não inventar datas, valores, taxas, prazos, documentos obrigatórios, regras ou políticas.
6. Não pedir senhas, tokens, dados bancários ou documentos pessoais no chat.
7. Não afirmar que consultou cadastro, emitiu documento, confirmou pagamento ou concluiu protocolo.
8. Distinguir orientação geral de situação individual, que exige consulta autenticada pelos canais institucionais.

## Estrutura de cada artigo

Cada artigo no JSON deve conter:
- identificador único;
- pergunta de referência;
- palavras-chave e variações;
- resposta explicativa;
- fonte institucional;
- status de validação e observações sobre limites.

Antes de publicar uma orientação, conferir se a página institucional continua disponível e se a informação se aplica ao curso, modalidade, currículo e período mencionados. Informações dinâmicas, como calendário, editais e oferta de cursos, devem ser verificadas na versão vigente.

## Pesquisa com estudantes

O formulário elaborado pelo grupo ainda está sem respostas. A atividade do professor exige pelo menos 30 respostas reais de estudantes. Não inserir percentuais, ranking de dúvidas ou conclusões antes da coleta.

Depois da coleta:
1. registrar o número de participantes e o período da pesquisa;
2. organizar as respostas por assunto;
3. identificar dúvidas recorrentes sem expor dados pessoais;
4. comparar as necessidades relatadas com os artigos existentes;
5. priorizar novos conteúdos conforme os dados observados;
6. separar percepções dos estudantes de regras oficiais da universidade.

## Limites técnicos atuais

A versão atual usa HTML, CSS, JavaScript e um arquivo JSON local. A busca é baseada em palavras-chave e pontuação de compatibilidade; não é IA generativa. O painel de sentimento usa uma classificação lexical simples das mensagens escritas pelos alunos, apenas na sessão atual. Essa estimativa pode errar com ironia, negação e contexto e não deve ser tratada como diagnóstico ou resultado científico.

Não há persistência em banco, autenticação, integração com sistemas institucionais, WhatsApp, n8n, Supabase ou transferência real para atendentes.