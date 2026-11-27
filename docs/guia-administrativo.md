# Guia administrativo — LUMI Studio

## 1. Contexto institucional fictício

A LUMI atende, exclusivamente no universo demonstrativo do projeto, a **Universidade Aurora (UVA)**.

| Elemento | Definição fictícia |
|---|---|
| Instituição | Universidade Aurora (UVA) |
| Campus | Campus Horizonte |
| Portal do estudante | Portal Aurora |
| Ambiente virtual | Aurora Online |
| Secretaria | Secretaria Acadêmica |
| Financeiro | Central Financeira |
| Atendimento geral | Central de Relacionamento Aurora |
| Biblioteca | Biblioteca Aurora |

Todos os nomes, serviços e procedimentos são fictícios. Não representam instituições reais.

## 2. Agentes

- **Generalista:** recebe a pergunta, acolhe, identifica a intenção e direciona.
- **Acadêmica:** matrícula, rematrícula, documentos, declarações, histórico, protocolos e secretaria.
- **Financeira:** mensalidades, pagamentos, cobranças vencidas, contestação, bolsas, negociação, extrato e estorno.
- **Campus:** calendário, avaliações, notas, frequência, cursos, disciplinas, atividades, biblioteca, apoio e ambiente virtual.

O atendimento humano é uma rota de escalonamento, não um quinto agente.

## 3. Regras de resposta

1. Falar em português brasileiro, com clareza, empatia e objetividade.
2. Responder com base no JSON institucional fictício.
3. Não misturar a UVA com universidades reais.
4. Não inventar datas de calendário, valores individuais, notas ou situação financeira.
5. Para assuntos individuais, direcionar ao Portal Aurora ou ao setor responsável.
6. Nunca solicitar senhas, códigos de autenticação, dados bancários ou documentos pessoais pelo chat.
7. Não afirmar que emitiu documento, confirmou pagamento ou abriu protocolo sem integração real.
8. Explicar quando a informação não estiver na base e oferecer encaminhamento.

## 4. Gestão da base

Arquivo principal: `data/base-conhecimento-lumi.json`.

Cada artigo contém:
- `id`: identificador único;
- `pergunta`: pergunta principal;
- `palavras_chave`: termos para localizar o conteúdo;
- `resposta`: orientação exibida pela LUMI;
- `fonte`: origem do conteúdo no universo fictício;
- `status`: situação editorial.

Antes de publicar uma alteração:
- conferir se o artigo pertence ao agente correto;
- testar perguntas com e sem acentos e sinônimos;
- verificar se a resposta não promete uma ação que o protótipo não executa;
- remover informações contraditórias;
- atualizar a versão e a data de revisão do JSON.

## 5. Segurança e privacidade

O chat não deve pedir senha, token, número completo de documento, cartão ou dados bancários. Em uma futura versão integrada, o acesso ao painel deverá exigir autenticação e perfis de permissão. Conversas deverão ter retenção limitada, acesso restrito e minimização de dados.

## 6. Testes recomendados

- Pergunta respondida por cada especialista.
- Pergunta com intenção ambígua.
- Pergunta fora do escopo.
- Pergunta cuja resposta não existe na base.
- Pedido de informação individual (nota, boleto, matrícula).
- Pedido de ação (emitir declaração, alterar matrícula, abrir chamado).
- Tentativa de obter dados sensíveis.
- Pedido de atendimento humano.

Avaliar precisão, clareza, agente selecionado, segurança e qualidade do encaminhamento.

## 7. Limites do protótipo

A versão atual consulta um arquivo JSON e seleciona respostas por palavras-chave. Não há IA generativa, consulta a cadastro, emissão de documentos, processamento financeiro, abertura de protocolos, integração com equipe humana ou persistência de edições do painel. A opção de atendimento humano é demonstrativa.
