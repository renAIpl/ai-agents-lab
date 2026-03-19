# Seu primeiro agente pessoal de IA

> Como sair do uso de chat e ter um assistente que executa tarefas por você — sem escrever uma linha de código.

**Por Renato Pereira Lima** · AI Builder  
github.com/renAIpl/ai-agents-lab · v1.0 · 2026

---

## Por que isso importa

A maioria das pessoas usa IA da mesma forma: abre o chat, faz uma pergunta, recebe uma resposta, fecha. Amanhã começa do zero. Isso não é um agente — é um Google mais educado.

A virada acontece quando você para de usar IA como ferramenta de consulta e começa a usá-la como alguém que **trabalha com você** — que conhece seus objetivos, lembra o que você fez, cobra o que planejou, e executa tarefas sem você precisar repetir o contexto toda vez.

Este playbook mostra como chegar lá. Sem código. Sem configurações complicadas. Com ferramentas que qualquer pessoa já tem acesso.

---

## O que muda na prática

**Antes — chat comum:**

> Você: "Me ajuda a organizar meus projetos."  
> IA: "Claro! Quais são seus projetos?" — de novo.

**Depois — com o agente:**

> Agente: "Bom dia. Você tem 3 projetos ativos, o prazo do P02 é amanhã, e a última sessão terminou com a revisão do relatório. Quer começar por aí?"

Essa diferença — de reativo para proativo — é o que transforma IA em um agente real.

---

## O que você vai construir

Um agente pessoal que opera com três mandatos simultâneos:

**Mandato 1 — Arquiteto Estratégico**  
Define a arquitetura técnica de cada projeto. Pensa em modularidade, custo de operação, escala e integração entre sistemas. Nunca propõe soluções sem considerar o custo de manutenção.

**Mandato 2 — Gerente de Projetos Ativo**  
Organiza o backlog no Notion, propõe priorização, cria e atualiza cards, cobra prazos e apresenta status no início de cada sessão. Tem autonomia para desafiar prioridades — não apenas executá-las.

**Mandato 3 — Mentor Sênior em IA**  
Adapta a complexidade ao nível atual do usuário, que evolui a cada sessão. Ensina o conceito antes do código. Calibra o ritmo: desafiador o suficiente para evoluir, claro o suficiente para não travar.

E diferente de um chatbot comum, este sistema tem **memória real**: ele sabe o que você fez ontem, onde travou, e o que fazer hoje — mesmo em uma conversa completamente nova.

---

## O que você precisa

- **Claude Pro** — claude.ai — USD 20/mês
- **Notion** — notion.so — plano gratuito funciona
- **2 horas** para montar o sistema uma vez

Não precisa de Python, API key, nem servidor. Tudo roda no browser.

---

## Parte 1 — Criar o Claude Project

### O que é um Project

Um Project no Claude.ai é um espaço persistente com três camadas:

1. **Instruções fixas** — definem quem o Claude é e como ele se comporta em todas as conversas
2. **Knowledge** — arquivos que o Claude consulta automaticamente em toda conversa
3. **Histórico** — conversas organizadas dentro do mesmo contexto

A diferença entre usar o Claude normal e um Project configurado é a diferença entre briefar um freelancer do zero toda vez e ter um sócio que já conhece tudo.

### Como criar

1. Acesse claude.ai
2. Menu lateral → **Projects** → **New Project**
3. Dê um nome — ex: `Meu Agente Pessoal`
4. Clique em **Create project**

### As instruções — cole, personalize e cole no Project

No campo **Project Instructions**, cole o bloco abaixo. Personalize apenas as partes marcadas:

```
# Identidade e Papel

Você é meu Arquiteto Estratégico, Gerente de Projetos e Mentor em IA.
Não um assistente que responde perguntas — um parceiro que me conduz
do zero até ter meu primeiro time de agentes funcionando.

Mandato 1 — Arquiteto Estratégico
Define a arquitetura técnica de cada etapa. Pensa em modularidade,
custo de operação, escala e integração entre sistemas. Nunca propõe
soluções sem considerar o custo de manutenção.

Mandato 2 — Gerente de Projetos Ativo
Organiza o backlog no Notion, propõe priorização, cria e atualiza
cards, cobra prazos e apresenta status no início de cada sessão.
Tem autonomia para desafiar prioridades — não apenas executá-las.

Mandato 3 — Mentor Sênior em IA
Adapta a complexidade ao meu nível atual, que evolui a cada sessão.
Ensina o conceito antes do código. Calibra o ritmo: desafiador o
suficiente para evoluir, claro o suficiente para não travar.

# Meu Objetivo Final com IA

↓ ESCREVA O SEU OBJETIVO — seja específico sobre onde quer chegar
  os exemplos abaixo são só inspiração, não copie

Ex: "Quero um agente que organize meus emails e me dê um resumo diário"
Ex: "Quero um agente que avalie oportunidades de investimento"
Ex: "Quero um time de agentes que produz e publica conteúdo por mim"
Ex: "Quero automatizar a análise de métricas do meu negócio"

→ Substitua pelos seus objetivos e delete esta linha

# Sessão 0 — Onboarding Obrigatório

Na PRIMEIRA conversa, antes de qualquer outra coisa:

Passo 1 — Faça no máximo 5 perguntas para entender:
  nível técnico · tempo disponível · ferramentas que usa
  o que já tentou com IA · detalhes do objetivo final

Passo 2 — Monte o plano personalizado:
  jornada em etapas até o objetivo · marcos com prazo
  primeira ação para hoje · riscos e trade-offs honestos
  aguarde validação antes de prosseguir

Passo 3 — Configure o Notion via MCP:
  hub central · database de Projetos com marcos
  database de Tarefas · Log de Evolução
  popule com os projetos do plano validado

Passo 4 — Feche com resumo e primeira ação concreta

# Protocolo de Sessões (após Sessão 0)

ABERTURA — sempre primeiro:
---
BRIEFING — [DATA] · [Etapa atual]
Status: [No prazo / Atenção / Em risco]
Ativos: [projetos com status]
Alerta: [prazo próximo ou item parado]
Pendente: [tarefa da última sessão]
→ Foco sugerido: [recomendação + justificativa]
---

ENCERRAMENTO — sempre ao final:
---
RESUMO — [DATA]
Foco · Decisões · Entregáveis
Próxima ação: [UMA tarefa concreta]
Notion: [cards a criar ou atualizar]
---

# Jornada — Do Zero ao Time de Agentes

Etapa 1 — Fundação: prompt engineering · Notion como GP
           saída: estrutura qualquer pedido sem ajuda

Etapa 2 — Primeiro Agente: resolve um problema real e mensurável
           saída: agente funcionando no domínio do objetivo

Etapa 3 — Automação: roda sem o usuário estar presente
           saída: tarefa autônoma com resultado verificável

Etapa 4 — Time: múltiplos agentes executando o objetivo final
           saída: objetivo da Sessão 0 sendo executado pelo time

Nunca pule etapa sem domínio demonstrado da anterior.

# Regras

SEMPRE: pergunte 2-3x antes de pedidos amplos · indique
         complexidade · explique conceito antes do código

NUNCA:  pular etapas · ignorar trade-offs · prometer
         automação sem MVP manual validado
```

> **Por que a Sessão 0 muda tudo:** o agente não começa trabalhando — começa orientando. Ele entende seu objetivo real, monta um plano personalizado, valida com você e só então configura o Notion com os projetos e marcos da sua jornada. O sistema reflete quem você é — não um template genérico.

---

## Parte 2 — Os três arquivos de memória

O agente tem memória porque você vai dar a ele três arquivos de contexto — documentos simples que ele consulta automaticamente em toda conversa. Crie no bloco de notas, salve como `.md` e suba no Project.

**Como subir:** Project → **Add content** → **Upload files** → selecione os arquivos.

---

### Arquivo A: `meu-perfil.md`

Quem você é. O agente usa para calibrar respostas ao seu contexto real.

```markdown
# Meu Perfil

## Sobre mim
Nome: [seu nome]
Área: [ex: gestão, marketing, educação, vendas]
Objetivo com IA: [o que você quer alcançar]

## Pontos fortes
- [ex: boa comunicação, pensamento analítico]
- [ex: experiência em gestão de times]

## Contexto atual
- [ex: trabalho em empresa X, estou em transição de carreira]
- [ex: tenho 3 horas por semana para projetos pessoais]

## O que preciso de ajuda
- [ex: organizar meus projetos pessoais]
- [ex: aprender IA de forma progressiva]
```

---

### Arquivo B: `log-evolucao.md` ← o mais crítico

A memória do que já aconteceu. Sem este arquivo, cada conversa começa do zero.

```markdown
# Log de Evolução

## Status atual
Início: [data de hoje]
Etapa: 1 — Fundação

## Sessão 1 — [data]
O que fizemos: configurei o agente e criei os arquivos de memória
Decisões: [descreva qualquer decisão relevante]
Próxima ação: [o que você vai fazer na próxima sessão]
```

**Regra de ouro:** ao final de cada sessão, o agente gera o bloco "RESUMO". Copie e cole aqui. Suba o arquivo atualizado no Project. Leva 2 minutos — é o que mantém o sistema inteligente ao longo do tempo.

---

### Arquivo C: `projetos-ativos.md`

Seu backlog pessoal. O agente usa para montar o briefing de abertura.

```markdown
# Projetos Ativos

| Projeto | Status | Prazo |
|---------|--------|-------|
| [Projeto 1] | 🔴 Não iniciado | [data] |
| [Projeto 2] | 🔴 Não iniciado | [data] |

## [P01] Nome do projeto
Status: 🔴 Não iniciado
Prazo: [data]
O que é: [descrição em 1-2 linhas]
Próxima ação: [passo concreto]
```

---

## Parte 3 — Conectar o Notion

O Notion é onde o agente "trabalha" de forma visível. Tarefas ganham status, projetos têm prazo rastreado e você enxerga a evolução ao longo do tempo.

### Conectar em 2 passos

1. No seu Project → **Add tools** → **Notion** → **Connect** → autorize o acesso
2. Peça ao agente para criar tudo com um comando

### O comando exato

Abra uma conversa no Project e escreva:

> "Crie no meu Notion um espaço de organização com 3 databases: **Projetos** (nome, status, prazo, próxima ação), **Tarefas** (vinculadas a projetos) e **Log de Evolução** (uma entrada por sessão)."

O agente cria tudo automaticamente em menos de 2 minutos. Depois abra o database Projetos → **+ Add a view** → **Board** → agrupe por Status. Você terá o kanban visual do seu backlog.

---

## Parte 4 — Como usar no dia a dia

### Abrindo uma sessão

Sem precisar explicar nada. O agente entrega o briefing:

```
BRIEFING — 19/03/2026 · Etapa 1

Status: 🟢 No prazo
Ativos:
  P01 — Estrutura do sistema · ✅ Concluído
  P02 — Primeiro agente · 🔴 Próximo · prazo 22/03
Pendente: definir o problema que o agente vai resolver
→ Foco sugerido: P02 — desbloqueia a Etapa 2
```

### O que você pode pedir

- *"Cria um plano de estudos para as próximas 4 semanas."*
- *"Resume este texto em 5 bullets para uma apresentação."*
- *"Atualiza o P02 no Notion como concluído e cria o próximo projeto."*
- *"Qual tarefa faz mais sentido atacar hoje dado meu tempo disponível?"*
- *"Organiza minha lista de ideias e prioriza as 3 mais importantes."*

### Onde ele vira diferencial real na sua rotina

**Segunda-feira de manhã** — em vez de uma lista caótica, você abre o agente e recebe: status dos projetos, o prazo que chega essa semana, e uma sugestão clara do que atacar primeiro.

**Projeto travado** — você descreve onde está. O agente sugere o próximo passo, estrutura a tarefa, cria o card no Notion e te entrega um rascunho para começar.

**Fim de sessão** — o agente gera o resumo, atualiza o log, registra a próxima ação. Você fecha o computador sabendo exatamente o que vem depois.

### Onde ele não substitui um especialista

| ✗ Não funciona bem para | ✓ Funciona muito bem para |
|-------------------------|---------------------------|
| Análise financeira complexa (DRE, valuation) | Organizar e priorizar projetos |
| Dados em tempo real (mercado, preços) | Redigir, revisar e estruturar textos |
| Diagnósticos médicos ou jurídicos | Criar e atualizar o Notion por você |
| Executar tarefas sem você presente | Sugerir próximos passos com justificativa |

---

## Checklist — do zero ao agente funcionando

**Configuração (faça uma vez):**

- [ ] Criar o Claude Project
- [ ] Colar e personalizar as instruções
- [ ] Criar os 3 arquivos de memória e subir no Project
- [ ] Conectar o Notion via MCP
- [ ] Pedir ao agente para criar os 3 databases
- [ ] Criar board view por status no Notion
- [ ] Fazer a primeira sessão (Sessão 0) e registrar no log

**Operação semanal:**

- [ ] Abrir sessão → receber briefing → confirmar foco
- [ ] Ao encerrar → copiar resumo → atualizar `log-evolucao.md`
- [ ] Atualizar `projetos-ativos.md` quando projeto mudar de status
- [ ] Re-subir arquivos atualizados no Project

---

## O que vem depois

Este playbook cobre o **primeiro nível**: um agente pessoal generalista, sem código, que funciona para qualquer pessoa e qualquer área.

Conforme você avança pelas etapas — Fundação, Primeiro Agente, Automação, Time — o sistema cresce com você. Agentes mais especializados, automações que rodam sem você estar presente, times que trabalham enquanto você dorme. Cada um desses passos existe e é acessível.

O mais importante agora é dar o primeiro passo: sair do uso de chat e ter algo que executa por você.

---

*Playbook v1.0 · Renato Pereira Lima · AI Builder · Março 2026*  
*Repositório: [github.com/renAIpl/ai-agents-lab](https://github.com/renAIpl/ai-agents-lab)*
