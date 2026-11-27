# LUMI — Assistente virtual universitária

**Projeto de extensão · IA Conversacional**  
**Equipe:** Paula e Duda · **Canal:** Web Chat · **Idioma:** Português brasileiro

A LUMI é uma proposta de assistente virtual para a Central de Atendimento ao Aluno do case fictício **Instituto Horizonte**, conforme a atividade final da disciplina. A experiência foi desenhada para ser acolhedora, simples, responsiva e fácil de usar.

## Objetivo

Ajudar estudantes a encontrar orientações acadêmicas, direcionando cada dúvida ao agente especialista adequado. Quando a informação não estiver disponível ou exigir análise individual, a LUMI deve explicar a limitação e orientar o contato com o setor responsável.

## Arquitetura de agentes

| Agente | Responsabilidade | Base própria |
|---|---|---|
| LUMI Generalista | Boas-vindas, identificação da intenção e roteamento | Escopo, intenções e encaminhamentos |
| LUMI Acadêmica | Matrícula e documentos | FAQ acadêmico |
| LUMI Financeira | Mensalidades e pagamentos | FAQ financeiro |
| LUMI Campus | Calendário, disciplinas e vida acadêmica | FAQ do campus |

## Funcionalidades do protótipo atual

- Interface web responsiva em português brasileiro.
- Chat com envio de mensagens, histórico da sessão e atalhos.
- Roteamento demonstrativo por assunto para três especialistas.
- Base de conhecimento em JSON, separada do código.
- Respostas de fallback para perguntas desconhecidas ou fora do escopo.
- Orientação para procurar atendimento humano quando necessário.
- Central de ajuda com busca.
- Dashboard ilustrativo com assuntos e sentimentos.
- Avisos claros sobre dados fictícios e privacidade.

> **Estado atual:** protótipo front-end. Ainda não há integração com Grok, n8n, Supabase ou sistemas da universidade. O painel contém exemplos fictícios, não resultados de pesquisa. A equipe deve validar e completar a base com informações autorizadas antes da demonstração final.

## Como executar

1. Baixe o repositório pelo botão **Code → Download ZIP** e extraia a pasta.
2. Abra a pasta no Visual Studio Code.
3. No terminal, execute:

```bash
python -m http.server 8000
```

4. Acesse http://localhost:8000 no navegador.

Também é possível usar a extensão **Live Server** do VS Code. É necessário utilizar um servidor local para carregar o arquivo JSON da base de conhecimento.

## Estrutura

```text
Projeto_Lumi/
├── index.html
├── styles.css
├── app.js
├── data/
│   └── knowledge-base.json
└── docs/
    ├── ARQUITETURA.md
    ├── TESTES.md
    └── PLANO-DE-ENTREGA.md
```

## Identidade visual

Paleta suave de lavanda, rosa antigo, verde sálvia, creme e branco; títulos em Manrope; textos em DM Sans; layout limpo e adaptável a computador, tablet e celular.

## Heurísticas de Nielsen consideradas

1. **Visibilidade do status:** identificação do estado da conversa e do ambiente demonstrativo.
2. **Correspondência com o mundo real:** linguagem familiar à rotina universitária.
3. **Controle e liberdade:** reiniciar a conversa e navegar entre áreas.
4. **Consistência e padrões:** componentes e navegação coerentes.
5. **Prevenção de erros:** aviso sobre dados sensíveis e limite de caracteres.
6. **Reconhecimento em vez de memorização:** atalhos e categorias visíveis.
7. **Flexibilidade e eficiência:** atalhos ou texto livre.
8. **Design estético e minimalista:** hierarquia visual sem excesso de elementos.
9. **Ajuda para reconhecer e recuperar erros:** fallback quando a pergunta não é reconhecida.
10. **Ajuda e documentação:** central de ajuda e orientação para atendimento humano.

## Requisitos da atividade que ainda precisam ser concluídos

- [ ] Aplicar formulário e obter **no mínimo 30 respostas de alunos reais da universidade**.
- [ ] Analisar os resultados e priorizar dúvidas com base nos dados.
- [ ] Validar a base com informações corretas e autorizadas.
- [ ] Implementar integração real com IA e orquestração dos agentes.
- [ ] Persistir histórico, assunto e sentimento em banco de dados.
- [ ] Conectar o dashboard aos dados reais.
- [ ] Testar perguntas reais, ambíguas, desconhecidas e encaminhamento humano.
- [ ] Finalizar relatório técnico e apresentação de 10 a 15 minutos.

## Ferramentas sugeridas no enunciado

O PDF sugere Grok para interpretação e geração de respostas, Supabase para banco de dados, n8n para orquestração e Docker para containerização. Como a equipe escolheu Web Chat, a integração WAHA/WhatsApp não é necessária nesta versão.

Chaves de API nunca devem ficar no JavaScript do navegador nem ser publicadas no GitHub.

## Documentação

- [Arquitetura](docs/ARQUITETURA.md)
- [Plano de testes e heurísticas](docs/TESTES.md)
- [Plano de entrega](docs/PLANO-DE-ENTREGA.md)

---
**LUMI** · Sua jornada universitária, mais leve. 💗