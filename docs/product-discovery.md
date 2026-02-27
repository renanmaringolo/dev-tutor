# Product Discovery — Dev Tutor (nome provisorio)

> Ferramenta local-first de inteligencia de crescimento profissional que analisa como desenvolvedores interagem com assistentes de IA para revelar gaps de conhecimento, padroes de dependencia e sinais reais de senioridade.

**Status**: Discovery / Ideacao
**Autor**: Renan Proenca
**Atualizado em**: 2026-02-24

---

## Sumario

1. [Problema](#1-problema)
2. [Usuario-alvo](#2-usuario-alvo)
3. [Panorama de Mercado](#3-panorama-de-mercado)
4. [Principios do Produto](#4-principios-do-produto)
5. [Capacidades Core](#5-capacidades-core)
6. [Modelo de Privacidade e Compliance](#6-modelo-de-privacidade-e-compliance)
7. [Escopo do MVP — Fase 0](#7-escopo-do-mvp--fase-0)
8. [Roadmap](#8-roadmap)
9. [Riscos e Mitigacoes](#9-riscos-e-mitigacoes)
10. [Criterios de Sucesso](#10-criterios-de-sucesso)

---

## 1. Problema

O mercado de desenvolvimento assistido por IA atingiu $5.42B em 2026 com projecao de $47.3B ate 2034 (CAGR de 24%). A adocao e praticamente universal: 84% dos devs usam ferramentas de IA, que ja geram 41% de todo codigo. Mas uma desconexao perigosa esta emergindo por baixo das metricas de superficie. A confianca dos devs na acuracia de codigo gerado por IA caiu de 40% para 29%, 48% do codigo gerado por IA contem vulnerabilidades de seguranca e 46% dos devs nao confiam totalmente nos outputs. Nao sao problemas de adocao — sao problemas de competencia. Devs estao entregando mais codigo enquanto entendem menos dele.

A evidencia de degradacao de skills nao e mais anedotica. A propria pesquisa da Anthropic mostra que devs que delegam tudo pra IA completam tarefas mais rapido, mas demonstram resultados mensuravelmente piores de aprendizado. Surveys internos da Anthropic revelam que enquanto engenheiros se tornam mais "full-stack" em amplitude, ha preocupacao crescente com a atrofia de skills profundas e especializadas. O consenso da industria agora recomenda manter 20-30% do trabalho sem assistencia de IA especificamente para prevenir erosao de skills. O problema e estrutural: toda ferramenta de IA para codigo e otimizada para velocidade de output, e nenhuma fornece feedback sobre se o dev esta de fato crescendo ou lentamente se tornando um operador de prompts.

Isso cria um risco profissional silencioso. Um dev que aceita sugestoes de IA sem entende-las, que nunca questiona codigo gerado, que delega cadeias inteiras de resolucao de problemas — esse dev nao esta se tornando mais produtivo. Esta se tornando mais dependente. Hoje nao existe ferramenta que surface esse padrao. Nenhuma ferramenta diz ao dev: "Voce parou de raciocinar sobre queries de banco 3 meses atras" ou "Voce aceita codigo critico de seguranca sem revisao 73% das vezes". O mercado inteiro de $5.42B e um ponto cego para crescimento profissional.

---

## 2. Usuario-alvo

**Persona: O Dev Pleno Autoconsciente**

Dev backend com 3-5 anos de experiencia, trabalhando principalmente com Ruby on Rails e/ou Node.js/TypeScript. Usa Claude Code (ou assistente de IA equivalente) diariamente como parte central do workflow. Entrega features consistentemente e e considerado produtivo pelos padroes do time.

Sua dor nao e velocidade — e direcao. Ele sente que esta se apoiando na IA pra coisas que antes raciocinava sozinho, mas nao consegue quantificar. Nao sabe quais skills estao crescendo e quais estao atrofiando. Quer chegar a senior, mas nao consegue distinguir entre "completei essa tarefa" e "entendi essa tarefa". Nenhuma ferramenta no stack atual da esse sinal.

Nao esta procurando um dashboard de produtividade. Esta procurando um espelho — um que mostre o dev que ele esta de fato se tornando, nao apenas o codigo que esta produzindo.

---

## 3. Panorama de Mercado

O ecossistema atual se divide em tres categorias, nenhuma das quais aborda crescimento profissional:

**Ferramentas de Geracao de Codigo com IA** — GitHub Copilot, Cursor, Claude Code, Windsurf. Esse e o mercado de $5.42B. Sao aceleradores puros de output. Medem sucesso por taxa de aceitacao, linhas geradas e tempo economizado. Tem zero insight sobre se o dev aprendeu algo. Nao sao concorrentes — sao o substrato de onde este produto le dados.

**Plataformas de Inteligencia de Desenvolvimento** — DX (getdx.com) e o player adjacente mais proximo, fornecendo inteligencia de engenharia via surveys, metricas e analise de workflow. Porem, o DX e desenhado para lideranca de engenharia avaliando produtividade em nivel de time. Responde "como o time esta indo?", nao "como EU estou crescendo?". Outras ferramentas nesse espaco (LinearB, Jellyfish, Pluralsight Flow) compartilham a mesma orientacao: top-down, escopo de time, foco em produtividade.

**Plataformas de Aprendizado** — Pluralsight, Udemy e similares oferecem avaliacoes de skills, mas sao desconectadas do trabalho real. Medem o que o dev sabe num ambiente artificial, nao como ele se comporta no workflow real com ferramentas reais.

**O gap e preciso e desocupado.** Nenhum produto opera como meta-layer sobre desenvolvimento assistido por IA para analisar comportamento cognitivo — como o dev pensa, questiona, aceita e revisa quando trabalha com IA. Este produto se posiciona entre as ferramentas de IA (fonte de dados) e o dev (usuario final), ocupando uma posicao nova: inteligencia de crescimento individual derivada de padroes de interacao com IA.

---

## 4. Principios do Produto

1. **Sinal cognitivo sobre ruido operacional.** Medimos como devs pensam, nao quais ferramentas clicam. Contagem de comandos, uso de ferramentas e duracao de sessao sao irrelevantes. Qualidade de raciocinio, pensamento critico e gaps de conhecimento sao o sinal.

2. **Local-first, sem excecoes.** Todos os dados sao capturados, armazenados e processados na maquina do dev. Nada sai sem consentimento explicito e informado. Privacidade e arquitetura, nao politica.

3. **Silencioso por padrao, cirurgico quando fala.** O produto roda em background 95% do tempo. So surface insights quando o padrao e forte e o valor e alto. Quando fala, importa.

4. **Falhas sobre elogios.** O produto foca em gaps, pontos cegos e padroes de dependencia — nao metricas de vaidade. Tom construtivo, nunca punitivo. O objetivo e crescimento, nao julgamento.

5. **Avaliacao multi-dimensional.** Senioridade nao e um numero unico. Um dev pode ser senior em backend e junior em infra. Toda analise e especifica por vertical, ponderada por frequencia e profundidade de interacao.

6. **Organico sobre artificial.** Sem comandos forcados. Sem gamificacao. Sem badges. O produto se integra ao workflow natural do dev e entrega valor sem exigir atencao.

7. **Transparencia de metodo.** O dev sempre consegue entender o que esta sendo analisado, por que um padrao foi sinalizado e como uma conclusao foi alcancada. Sem avaliacoes caixa-preta.

---

## 5. Capacidades Core

### 5.1 Analise de Qualidade de Raciocinio

Avalia como o dev formula pedidos para assistentes de IA. Detecta se problemas sao descritos com clareza e contexto, ou jogados como reclamacoes vagas ("ta bugado, conserta"). Mede a capacidade do dev de decompor problemas complexos em partes trataveis versus jogar tudo de uma vez. Esse e o sinal fundamental: como voce pergunta revela como voce pensa.

### 5.2 Deteccao de Avaliacao Critica

Rastreia o que acontece depois que a IA responde. Identifica padroes de aceitacao cega (merge sem revisao, sem follow-up) versus engajamento ativo (perguntar "por que", desafiar outputs incorretos, pegar erros antes de serem commitados). Distingue entre devs que usam IA como muleta e aqueles que usam como sparring partner.

### 5.3 Mapeamento de Gaps Tecnicos

Constroi um perfil de conhecimento por vertical baseado no que o dev pergunta, no que nunca pergunta e em como engaja com explicacoes. Topicos que sempre precisam de assistencia indicam gaps reais. Topicos nunca abordados indicam maestria ou evitacao — o sistema diferencia cruzando com atividade no codebase. Comportamento de follow-up apos explicacoes (perguntas mais profundas vs. ignorar) revela se o dev esta aprendendo ou apenas extraindo codigo.

### 5.4 Perfil de Autonomia e Dependencia

Mede a capacidade do dev de iterar independentemente apos um direcionamento inicial. Detecta padroes repetitivos: fazer a mesma pergunta de formas diferentes (sinal de nao-compreensao), retornar a mesma categoria de problema repetidamente (gap estrutural), ou colar prints de conversas externas sem conseguir articular o problema (gap de comunicacao + gap de dominio). Rastreia quando o dev modifica codigo gerado pela IA — sinal forte de dominio do assunto.

### 5.5 Avaliacao de Senioridade por Vertical

Produz um perfil de senioridade multi-dimensional atraves de verticais tecnicas (backend, frontend, DevOps, dados, infra, etc.). Cada vertical e pontuada independentemente baseada em padroes de interacao, ponderada por frequencia. Arquetipos comportamentais: junior (delegativo, acritico), pleno (contextual, questionador, com gaps especificos), senior (opiniao formada, desafia a IA, usa para validacao nao geracao). Verticais nao abordadas sao sinalizadas como pontos cegos potenciais, nao assumidas como dominio.

### 5.6 Sintese Periodica

Gera relatorios macro em cadencia configuravel (semanal ou quinzenal). Agrega padroes ao longo do tempo para revelar tendencias: areas em melhoria, gaps persistentes, mudancas em padroes de dependencia. Projetado para auto-reflexao, nao vigilancia. Se o relatorio nao tem nada significativo a dizer, nao diz nada.

---

## 6. Modelo de Privacidade e Compliance

### Arquitetura

Toda captura de interacao, analise de padroes e armazenamento de dados acontecem exclusivamente na maquina local do dev. Sem servidor central, sem telemetria. Essa e uma restricao arquitetural rigida, nao uma feature flag.

### Cenarios de Fluxo de Dados

| Cenario | Descricao | Superficie de compliance |
|---|---|---|
| **Via Claude Code CLI (padrao)** | Plugin invoca `claude -p` localmente usando a assinatura existente do dev. Dados processados pela Anthropic sob os termos da assinatura do proprio usuario. | Minima para uso pessoal. Para uso publico: mesmas consideracoes de API (consentimento, transparencia). |
| **Via API key direta** | Dev configura API key propria para chamadas diretas. Mais controle sobre payloads e parametros. | Criador pode ser classificado como Controlador de Dados sob LGPD/GDPR (determina finalidade/meios do processamento). Provider da API e Processador. Requer: fluxo de consentimento, transparencia, minimizacao de dados. |

### LGPD/GDPR por Fase

| Fase | Requisito de compliance |
|---|---|
| Uso pessoal (Fase 0) | Nenhum. Auto-analise dos proprios dados. |
| Lancamento publico, modo local-only | Minimo. Politica de privacidade descrevendo tratamento local. |
| Lancamento publico, modo com API externa | Completo. Termos de uso, consentimento explicito, transparencia sobre o que e enviado, minimizacao de dados, direito a exclusao. |

### Principios de Dados

- Logs de conversa brutos sao processados em sinais comportamentais e depois descartados. O produto armazena padroes, nao transcricoes.
- Se o modo de API externa for usado, apenas resumos comportamentais abstraidos sao enviados — nunca codigo bruto, nunca conversas completas.
- O dev pode inspecionar, exportar e deletar todos os dados armazenados a qualquer momento.
- Consentimento explicito e granular obrigatorio antes de qualquer dado sair da maquina. Opt-in por sessao, nao um acordo generico.

---

## 7. Escopo do MVP — Fase 0

Fase 0 e uso pessoal exclusivo. O criador roda na propria maquina para validar se o modelo de dados produz insights significativos.

### Incluido

| # | Capacidade | Descricao |
|---|---|---|
| C1 | Integracao de Hooks | Hooks do Claude Code (PreToolUse, PostToolUse, Notification) com zero configuracao manual |
| C2 | Rastreamento de Sessao | Agrupar interacoes em sessoes logicas com limites de inicio/fim |
| C3 | Classificacao de Dominio | Tagear interacoes por dominio tecnico usando heuristicas de keyword/padrao |
| C4 | Score de Autonomia | Medir razao aceitar/rejeitar/modificar por dominio por sessao |
| C5 | Deteccao de Repeticao | Identificar quando o mesmo tipo de pergunta recorre entre sessoes |
| C6 | Geracao de Relatorio | Sumario estruturado semanal/quinzenal em markdown |
| C7 | Controle de Retencao | Limpar, exportar ou inspecionar todos os dados armazenados |

### Excluido

- Dashboard web ou qualquer GUI
- Nudges proativos no fluxo
- Suporte multi-LLM
- Geracao de insights com IA via API key direta (Fase 0 usa Claude Code CLI via assinatura existente + heuristicas deterministicas)
- Gamificacao, scoring ou framing competitivo
- Features de time/enterprise
- Qualquer transmissao de dados fora do localhost

### Stack Tecnica (Fase 0)

- **Core**: TypeScript
- **Storage**: SQLite (local, zero infra)
- **Integracao**: Hooks do Claude Code
- **Analise de insights**: Claude Code CLI (`claude -p`) via assinatura existente
- **Output**: Relatorios markdown (terminal/arquivo)

---

## 8. Roadmap

### Fase 0 — Dogfood Pessoal

Coletor funcional, storage local em SQLite, insights gerados via Claude Code CLI (assinatura existente), relatorios via terminal. Uso diario para validar se os metadados coletados produzem insights reais.

**Criterio de saida**: 4+ semanas de dados. Relatorios revelam pelo menos 2 padroes de dependencia nao-obvios que o dev nao tinha consciencia.

### Fase 1 — MVP Local (Alpha Publico)

Dashboard web em localhost com visualizacao radar chart. Sistema de nudge proativo nas sessoes do Claude Code (silencioso por padrao, apenas high-signal). Classificador de dominio aprimorado via Claude Code CLI. Suporte a API key direta como alternativa.

**Criterio de saida**: 5-10 usuarios alpha por 2+ semanas. 60%+ reportam nudges como uteis. Zero dados saem da maquina de qualquer usuario.

### Fase 2 — Produto (Beta Publico)

Suporte multi-LLM (VS Code Copilot, Cursor, outros CLIs) via camada de abstracao. Planos de estudo personalizados baseados nos gaps identificados. Arquitetura de plugins para classificadores contribuidos pela comunidade.

**Criterio de saida**: API de plugin estavel. 3+ integracoes com LLMs. Retencao de 30 dias medida.

### Fase 3 — Enterprise e Escala

Dashboard de time com skill maps anonimizados e agregados. Pipeline LGPD/GDPR-compliant para sync opcional na nuvem. Analise de gaps em nivel organizacional sem expor devs individuais.

**Criterio de saida**: Auditoria de compliance aprovada. Piloto com 1+ time de engenharia (10+ devs).

---

## 9. Riscos e Mitigacoes

| Risco | Impacto | Mitigacao |
|-------|---------|-----------|
| **Exposicao LGPD** — chamadas de API tornam criador Controlador de Dados | Alto | Fase 0: zero chamadas externas. Depois: modelo local como padrao, API externa apenas com consentimento explicito + key do usuario. |
| **Efeito Clippy** — nudges de baixa qualidade destroem confianca | Alto | Modo silencioso por padrao. Threshold de alta confianca. Primeiras 2 semanas so observacao. Usuario pode silenciar categorias. |
| **Imprecisao de calibracao** — perfis enganosos | Medio | Heuristicas multi-sinal. Expor dados brutos junto com interpretacoes. Feedback "discordo" para retreinar pesos localmente. |
| **Dependencia de plataforma** — API de hooks do Claude Code muda | Alto | Abstrair hooks atras de interface adapter. Desenhar camada de dados LLM-agnostica. |
| **Metricas rasas** — medir volume ao inves de qualidade | Medio | Rastrear mudanca comportamental ao longo do tempo (dependencia diminuiu?), nao contagem de sessoes. Direcao de tendencia sobre numeros absolutos. |
| **Friccao de adocao** — overhead de config/manutencao | Medio | Instalacao com comando unico (`npx`). Zero config. Auto-registro de hooks. Sem daemons em background. |
| **Scope creep** — construir UI antes de validar modelo de dados | Medio | Fase 0 e text-only, deliberadamente minimo. Sem UI ate criterios de saida serem atingidos. |

---

## 10. Criterios de Sucesso

### Validacao da Fase 0

O produto funciona se, apos 4+ semanas de uso pessoal:

1. **Revelacao de Gaps** — Relatorio semanal identifica pelo menos 2 areas tecnicas onde o dev consistentemente delega ao inves de resolver independentemente, confirmadas como gaps reais.

2. **Consciencia Comportamental** — Dev modifica comportamento em pelo menos 1 area como resultado direto de um insight do relatorio.

3. **Fidelidade de Dados** — Dados de sessao refletem com precisao o uso real. Sem dominios classificados incorretamente em >80% das entradas.

4. **Zero Friccao** — Ferramenta roda sem intervencao manual entre sessoes. Sem crashes, sem latencia perceptivel adicionada ao Claude Code.

5. **Sinal vs Ruido** — Todo item do relatorio e acionavel ou informativo de forma surpreendente. Sem preenchimento.

---

## Referencias

- [Anthropic Research: How AI assistance impacts the formation of coding skills](https://www.anthropic.com/research/AI-assistance-coding-skills)
- [Anthropic: How AI Is Transforming Work at Anthropic](https://www.anthropic.com/research/how-ai-is-transforming-work-at-anthropic)
- [Anthropic: Does Anthropic Act as a Data Processor or Controller?](https://support.claude.com/en/articles/9267385-what-is-the-data-relationship-between-anthropic-the-customer-and-the-user)
- [Anthropic: GDPR Approach](https://privacy.claude.com/en/articles/10015887-what-is-your-approach-to-gdpr-or-related-issues)
- [Anthropic Privacy Policy](https://www.anthropic.com/legal/privacy)
- [Stack Overflow Developer Survey 2025 — AI](https://survey.stackoverflow.co/2025/ai/)
- [AI Coding Assistant Statistics 2026](https://www.getpanto.ai/blog/ai-coding-assistant-statistics)
- [AI Code Assistant Market Size (Market.us)](https://market.us/report/ai-code-assistant-market/)
- [JetBrains: State of Developer Ecosystem 2025](https://blog.jetbrains.com/research/2025/10/state-of-developer-ecosystem-2025/)
- [DX: Developer Intelligence Platform](https://getdx.com/)
