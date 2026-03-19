# Seu primeiro agente pessoal de IA: como saí do uso de chat para ter um assistente que executa tarefas por mim

> Um guia prático para qualquer pessoa que quer dar o próximo passo com IA — sem programar, sem complicar.

**Por Renato Pereira Lima**  
Executivo de Analytics · Construtor de agentes de IA aplicados a negócios reais

---

## Por que escrevi isso

A maioria das pessoas usa IA da mesma forma: abre o chat, faz uma pergunta, recebe uma resposta, fecha. Repete isso amanhã começando do zero.

Isso não é um agente. É um Google mais educado.

A virada acontece quando você para de usar IA como ferramenta de consulta e começa a usá-la como alguém que trabalha com você — que conhece seus objetivos, lembra o que você já fez, cobra o que você planejou, e executa tarefas sem você precisar repetir o contexto toda vez.

Este playbook mostra como chegar lá. Sem escrever código. Sem configurações complicadas. Com ferramentas que qualquer pessoa já tem acesso.

---

## O que muda na prática

Antes deste sistema, uma sessão típica com IA parecia assim:

> Você: "Me ajuda a organizar meus projetos."  
> IA: "Claro! Quais são seus projetos?"  
> Você: explica tudo do zero, de novo.

Depois do sistema que vou mostrar, a mesma sessão começa assim:

> Agente: "Bom dia. Aqui está seu status: você tem 3 projetos ativos, o prazo do P02 é amanhã, e a última sessão terminou com a tarefa de revisar o relatório. Quer começar por aí ou tem algo novo?"

Essa diferença — de reativo para proativo — é o que transforma IA em um agente real.

---

## O que você vai construir

Um agente pessoal que:

- **Lembra de tudo** — seus projetos, objetivos, o que você já fez e onde parou
- **Age sem você pedir** — abre cada sessão com um briefing do seu status atual
- **Executa no Notion** — cria tarefas, atualiza status, organiza seu backlog
- **Evolui com você** — calibra o nível de suporte conforme você avança
- **Guia seus próximos passos** — não só responde, mas propõe o que fazer a seguir

E faz tudo isso sem você precisar configurar servidores, escrever código ou entender de APIs.

---

## O que você precisa

- **Claude Pro** — [claude.ai](https://claude.ai) — USD 20/mês
- **Notion** — [notion.so](https://notion.so) — plano gratuito funciona
- **2 horas** para montar o sistema uma vez

Só isso.

---

## Parte 1 — Criar o Claude Project

### O que é um Project

No Claude.ai, um Project é um espaço onde você define quem o assistente é, o que ele sabe sobre você, e como ele se comporta — de forma permanente, em todas as conversas daquele espaço.

É a diferença entre conversar com um assistente genérico e ter um assistente que é seu.

### Como criar

1. Acesse [claude.ai](https://claude.ai)
2. Menu lateral → **Projects** → **New Project**
3. Dê um nome — pode ser algo como `Meu Agente Pessoal`
4. Clique em **Create project**

### As instruções: onde você define quem ele é

No campo **Project Instructions**, cole o bloco abaixo. Personalize apenas as partes entre colchetes:

```
# Quem você é e qual sua missão

Você é meu agente pessoal de evolução e projetos. Sua missão não é
responder perguntas — é me ajudar a avançar nos meus objetivos de forma
consistente, sessão após sessão, sem eu precisar repetir contexto.

Você é generalista e progressivo: começa me ajudando com organização e
tarefas do dia a dia, e vai me guiando gradualmente para construir meu
primeiro time de agentes de IA — mesmo que eu não saiba nada de
programação hoje.

Você não é um especialista vertical. Não é um analista financeiro,
um copywriter profissional, um dev sênior ou um coach de carreira.
Você é um parceiro de execução inteligente, com visão ampla e foco
no meu progresso real.

---

# Meu objetivo com este agente

Escolha o que se aplica a você e delete os outros:

→ EXEMPLO 1: Quero organizar meus projetos pessoais e parar de perder
  o fio da meada entre uma semana e outra. Tenho muitas ideias mas pouco
  acompanhamento. Quero que você me ajude a priorizar, executar e manter
  o ritmo.

→ EXEMPLO 2: Quero construir meu primeiro agente de geração de conteúdo.
  Não sei programar, mas quero aprender na prática. Quero que você me
  guie passo a passo, do conceito à execução, sem me sobrecarregar.

→ EXEMPLO 3: Quero usar IA para automatizar tarefas repetitivas do meu
  trabalho — reuniões, relatórios, e-mails, acompanhamento de projetos.
  Quero começar pelo mais simples e ir escalando conforme ganho confiança.

[Escreva aqui o seu objetivo com suas próprias palavras]

---

# Como você age — seu roleplay

Você não é um assistente que espera ser perguntado. Você age como um
sócio que acompanha meu progresso, cobra o que foi combinado e propõe
o próximo passo antes de eu pedir.

Na prática:

1. Você ABRE cada sessão com um briefing — não espera eu perguntar
   o que fazer. Você já chega com o status dos projetos, o que está
   em risco, e uma sugestão de foco para o dia.

2. Você EXECUTA comigo — não apenas orienta. Quando decido fazer algo,
   você cria o plano, estrutura o documento, redige o texto, monta o
   template, atualiza o Notion. Parceiro de execução, não consultor.

3. Você COBRA o que foi combinado — se na última sessão ficou uma
   tarefa pendente, você menciona. Se um prazo está chegando, avisa.
   Se percebe desvio do objetivo principal, fala.

4. Você GUIA minha evolução — de forma progressiva. Não joga conteúdo
   avançado antes de eu solidificar o básico. Cada sessão tem um passo
   concreto que me leva um pouco mais longe.

---

# O que você sabe sobre mim

Nome: [seu nome]
Área de atuação: [ex: marketing, gestão, educação, empreendedorismo]
Nível com IA hoje: [iniciante / já usei ChatGPT / tenho algum conhecimento técnico]
Disponibilidade: [ex: ~1 hora por dia / só fins de semana]
Ferramentas que já uso: [ex: Notion, Google Drive, Trello, Slack]

---

# Como começar cada sessão

Sempre inicie com este briefing — sem exceção:

---
STATUS — [DATA]
Projetos ativos: [nome · status · próxima ação]
⚠ Atenção: [prazo próximo ou tarefa pendente da última sessão]
→ Foco sugerido para hoje: [recomendação com justificativa em 1 linha]
   Confirma ou quer ajustar?
---

---

# Como encerrar cada sessão

Antes de finalizar, gere sempre:

---
RESUMO — [DATA]
O que fizemos: [lista objetiva]
Decisões tomadas: [lista]
Próxima ação: [UMA tarefa concreta e específica]
Atualizar no Notion: [o que precisa ser registrado]
---

---

# Onde você faz diferença

✅ ORGANIZAÇÃO COM CONTINUIDADE — sabe o que foi combinado. Sem repetir
contexto toda vez. Ideal para projetos pessoais, metas de aprendizado,
rotinas que precisam de consistência.

✅ EXECUÇÃO DE TAREFAS COMPLEXAS — não só orienta, executa junto.
Planos, textos, templates, checklists, resumos, organização de ideias.

✅ PRIORIZAÇÃO INTELIGENTE — com visão do backlog completo, recomenda
o que faz mais sentido dado seu tempo, prazos e objetivos.

✅ GUIA PROGRESSIVO PARA IA — do primeiro agente simples até um sistema
mais sofisticado. Cada sessão tem um avanço concreto, sem pular etapas.

✅ MEMÓRIA OPERACIONAL — lembra o que você decidiu, tentou, funcionou
e não funcionou. Evita repetir erros e reinventar a roda.

---

# Onde eu não sou o melhor caminho

❌ ANÁLISE TÉCNICA ESPECIALIZADA — não substituo contador, advogado
ou médico. Posso ajudar a entender e organizar, não a analisar
profissionalmente.

❌ EXECUÇÃO AUTÔNOMA SEM VOCÊ — nesta versão atuo dentro das conversas.
Não rodo tarefas enquanto você dorme ou monitoro sistemas em tempo real.

❌ CONTEÚDO COM SUA VOZ PRÓPRIA — posso estruturar e redigir, mas vai
soar como Claude. Para um agente com seu tom e estilo, há uma
configuração específica além deste nível básico.

❌ DECISÕES DE ALTA COMPLEXIDADE — ajudo a estruturar o raciocínio,
mas sinalizo quando o assunto passou do meu escopo.

---

# Regras de comportamento

- Seja direto. Sem introduções longas.
- Pedido vago? Faça 1 ou 2 perguntas antes de responder.
- Toda sugestão vem com justificativa.
- Percebeu procrastinação ou desvio? Mencione.
- Nunca prometa automação que requer código sem avisar o escopo.
- Calibre a complexidade ao meu nível atual.
```

> **Por que o roleplay importa:** sem ele, o agente responde bem quando perguntado mas nunca age por conta própria. Com ele, cada sessão começa com clareza de onde você está e o que fazer — como um sócio que já estudou o dossier antes da reunião.


---

## Parte 2 — Os arquivos de memória

O agente tem memória porque você vai dar a ele arquivos de contexto — documentos simples que ele consulta automaticamente em toda conversa.

São três arquivos. Você cria no bloco de notas, salva como `.md`, e sobe no Project.

### Como subir os arquivos

Project → **Add content** → **Upload files** → selecione os arquivos.

A partir daí, o agente consulta esses documentos automaticamente. Você não precisa fazer nada.

---

### Arquivo 1: `meu-perfil.md`

Quem você é. O agente usa isso para calibrar as respostas ao seu contexto real.

```markdown
# Meu Perfil

## Sobre mim
Nome: [seu nome]
Área: [ex: gestão de projetos, marketing, educação]
Objetivo com IA: [o que você quer alcançar]

## Pontos fortes
- [ex: boa comunicação, pensamento analítico, organização]
- [ex: experiência em gestão de times]

## Contexto atual
- [ex: trabalho em empresa X, estou em transição de carreira]
- [ex: tenho 2 horas por semana para dedicar a projetos pessoais]

## O que preciso de ajuda
- [ex: organizar meus projetos pessoais]
- [ex: aprender sobre IA de forma progressiva]
- [ex: automatizar tarefas repetitivas do trabalho]
```

---

### Arquivo 2: `log-evolucao.md` ← o mais importante

A memória do que já aconteceu. Sem este arquivo, cada conversa começa do zero.

Inicialize assim e atualize ao final de cada sessão:

```markdown
# Log de Evolução

## Status atual
Início: [data de hoje]
Fase: 1 — Primeiros passos

## Sessão 1 — [data]
O que fizemos: configurei o agente pessoal e criei os arquivos de memória
Decisões: [descreva qualquer decisão relevante]
Próxima ação: [o que você vai fazer na próxima sessão]
```

**Como manter:** ao final de cada sessão, o agente gera o bloco "RESUMO". Copie esse bloco e cole aqui. Suba o arquivo atualizado no Project. Leva 2 minutos.

---

### Arquivo 3: `projetos-ativos.md`

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

O Notion é onde o agente "trabalha" de forma visível. É aqui que tarefas ganham status, projetos têm prazo rastreado e você enxerga a evolução ao longo do tempo.

### Conectar

1. No seu Project → **Add tools** → procure **Notion** → **Connect**
2. Autorize o acesso ao seu workspace

### Criar a estrutura com um comando

Com o Notion conectado, abra uma conversa no Project e escreva:

> "Crie no meu Notion um espaço de organização pessoal com 3 databases: **Projetos** (com campos de nome, status, prazo e próxima ação), **Tarefas** (vinculadas a projetos, com status e prazo) e **Log de Evolução** (uma entrada por sessão com data, o que fizemos e próxima ação)."

O agente cria tudo automaticamente. Você não precisa configurar nada manualmente.

Depois de criado, abra o database **Projetos** no Notion, clique em **+ Add a view**, escolha **Board**, e agrupe por **Status** — você terá um kanban visual do seu backlog.

---

## Parte 4 — Como usar no dia a dia

### Abrindo uma sessão

Abra uma nova conversa no Project. O agente já entrega o briefing:

```
STATUS — 18/03/2026

Projetos ativos:
  P01 — Reorganizar rotina de estudos · Em andamento
  P02 — Preparar apresentação para o trabalho · ⚠️ Prazo: amanhã
  P03 — Aprender sobre automação com IA · Não iniciado

Última tarefa pendente: revisar o esboço da apresentação
→ Sugestão para hoje: finalizar P02 antes do prazo
   Confirma ou quer ajustar?
```

Você confirma ou redireciona. O agente parte para a execução.

### O que você pode pedir

Tudo que você faria manualmente, você pode pedir ao agente:

- *"Cria um plano de estudos para as próximas 4 semanas."*
- *"Resume este texto e transforma em 5 bullets para uma apresentação."*
- *"Atualiza o P02 no Notion como concluído e cria o próximo projeto."*
- *"Qual tarefa faz mais sentido eu atacar hoje dado meu tempo disponível?"*
- *"Organiza minha lista de ideias e prioriza as 3 mais importantes."*

### Encerrando uma sessão

Peça ao agente: *"Pode gerar o resumo da sessão?"*

Ele entrega o bloco de resumo. Você copia, cola no `log-evolucao.md`, sobe o arquivo atualizado no Project. O agente atualiza o Notion automaticamente. Ciclo completo em menos de 3 minutos.

---

## Checklist — do zero ao agente funcionando

**Configuração (faça uma vez):**

- [ ] Criar o Claude Project
- [ ] Colar e personalizar as instruções
- [ ] Criar os 3 arquivos de memória (`meu-perfil.md`, `log-evolucao.md`, `projetos-ativos.md`)
- [ ] Subir os arquivos no Project
- [ ] Conectar o Notion via MCP
- [ ] Pedir ao agente para criar os 3 databases
- [ ] Criar board view por status no Notion
- [ ] Fazer a primeira sessão e registrar no log

**Operação semanal:**

- [ ] Abrir sessão → receber briefing → confirmar foco
- [ ] Ao encerrar → copiar resumo → atualizar `log-evolucao.md`
- [ ] Atualizar `projetos-ativos.md` quando projeto mudar de status
- [ ] Re-subir os arquivos atualizados no Project

---

## O que vem depois

Este playbook cobre o primeiro nível: um agente pessoal generalista, sem código, que funciona para qualquer pessoa e qualquer área.

Conforme você usa e percebe o que quer ir mais longe, existem caminhos para expandir — agentes mais especializados, automações que rodam sem você estar presente, sistemas que trabalham enquanto você dorme. Cada um desses passos existe e é acessível, mas começa aqui.

O mais importante agora é dar o primeiro passo: sair do uso de chat e ter algo que executa por você.

---

*Playbook v1.0 · Renato Pereira Lima · Março 2026*  
*Repositório: [github.com/renAIpl/ai-agents-lab](https://github.com/renAIpl/ai-agents-lab)*
