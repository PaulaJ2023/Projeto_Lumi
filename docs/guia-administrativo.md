# Guia do LUMI Studio

O LUMI Studio é a área administrativa demonstrativa destinada à equipe do projeto acadêmico.

## Contexto institucional
A pesquisa de campo será realizada com estudantes da **UNP — Unidade Salgado Filho**. A LUMI é uma proposta acadêmica independente, não um canal oficial da universidade. O case fictício “Instituto Horizonte”, definido no enunciado do professor, pode ser usado para dados e demonstrações técnicas. Não cadastrar regras inventadas como se fossem políticas da UNP.

## Visão geral
Apresenta indicadores da sessão e uma visão ilustrativa dos temas procurados. Na versão integrada, os dados deverão vir do banco, com período e filtros explícitos. Não usar números de exemplo como resultados da pesquisa.

## Agentes
Apresenta os quatro papéis da arquitetura. A ativação visual no protótipo não altera um serviço de IA real.

## Prompts
O prompt principal define identidade, tom, limites e estratégia de roteamento. Recomendações:
- falar em português brasileiro, com clareza e acolhimento;
- consultar a base antes de responder;
- não inventar procedimentos, datas, valores ou políticas da UNP;
- informar quando não souber;
- oferecer encaminhamento humano;
- não pedir senhas ou dados sensíveis;
- identificar quando a pergunta exige informação oficial atualizada.

## Base de conhecimento
Cada registro real deverá conter:
- título/pergunta;
- resposta validada;
- categoria e agente responsável;
- fonte oficial ou documento de referência;
- responsável pela validação;
- data de criação e última revisão;
- status (rascunho, publicado, arquivado).

Para conteúdos sobre a UNP, usar somente informações verificadas em canais oficiais ou validadas por responsável autorizado. Enquanto isso, manter textos como exemplos fictícios do Instituto Horizonte, identificados como tais.

## Laboratório de testes
Criar cenários para pergunta conhecida por cada especialista, pergunta ambígua, pergunta fora do escopo, informação ausente na base, tentativa de obter dado pessoal e pedido de atendimento humano.

Avaliar correção, clareza, roteamento, uso da fonte e comportamento de fallback.

## Resultados
Acompanhar volume de conversas, assuntos, agente acionado, taxa de resolução, perguntas sem resposta, encaminhamentos e avaliação do usuário. Classificação de sentimento é uma estimativa e não deve ser tratada como verdade objetiva. Os dados reais da pesquisa de campo devem ser apresentados separadamente dos dados simulados do chatbot.

## Histórico
Restringir acesso, mascarar dados pessoais e estabelecer política de retenção.
