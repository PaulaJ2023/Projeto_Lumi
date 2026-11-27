# Guia do LUMI Studio

O LUMI Studio é a área administrativa destinada à equipe do projeto.

## Visão geral
Apresenta indicadores da sessão e uma visão ilustrativa dos temas procurados. Na versão integrada, os dados deverão vir do banco, com período e filtros explícitos.

## Agentes
Apresenta os quatro papéis da arquitetura. A ativação visual no protótipo não altera um serviço de IA real.

## Prompts
O prompt principal define identidade, tom, limites e estratégia de roteamento. Recomendações:
- falar em português brasileiro, com clareza e acolhimento;
- consultar a base antes de responder;
- não inventar procedimentos, datas ou valores;
- informar quando não souber;
- oferecer encaminhamento humano;
- não pedir senhas ou dados sensíveis.

## Base de conhecimento
Cada registro real deverá conter:
- título/pergunta;
- resposta validada;
- categoria e agente responsável;
- fonte e referência;
- responsável pela validação;
- data de criação e última revisão;
- status (rascunho, publicado, arquivado).

## Laboratório de testes
Criar cenários para pergunta conhecida por cada especialista, pergunta ambígua, pergunta fora do escopo, informação ausente na base, tentativa de obter dado pessoal e pedido de atendimento humano.

Avaliar correção, clareza, roteamento, uso da fonte e comportamento de fallback.

## Resultados
Acompanhar volume de conversas, assuntos, agente acionado, taxa de resolução, perguntas sem resposta, encaminhamentos e avaliação do usuário. Classificação de sentimento é uma estimativa e não deve ser tratada como verdade objetiva.

## Histórico
Restringir acesso, mascarar dados pessoais e estabelecer política de retenção.
