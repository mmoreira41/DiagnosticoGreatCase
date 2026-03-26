/# Coachly — CLAUDE.md
> Memória permanente do projeto. Lê este ficheiro antes de qualquer ação.

## O que é este projeto

Coachly é um produto digital orientado a **coaching** (desportivo, performance, hábitos ou vida — o posicionamento exato fica documentado à medida que o produto amadurece). Este repositório serve de **fonte de verdade** para o sistema de skills por domínio e, quando existir código de aplicação, para padrões de implementação e entrega.

**Estado do repositório:** neste momento a raiz contém sobretudo `skills/` e `README.md`. Quando forem adicionados `app/`, `lib/`, `components/`, etc., atualiza a secção **Estrutura de diretórios** e a **Stack** abaixo para refletir a realidade.

---

## Stack

| Camada | Tecnologia | Notas |
|--------|-----------|-------|
| Framework | *A definir* (ex.: Next.js App Router, Expo, outro) | Documentar aqui após decisão |
| Banco / auth | *A definir* (ex.: Supabase) | Se aplicável: RLS, políticas, clientes server vs browser |
| IA | *A definir* | Centralizar chamadas num helper de servidor; chaves só no servidor |
| UI | *A definir* | Mobile-first; alinhar com `skills/design/` + pacote UI transversal |
| Deploy / CI | *A definir* | Quando existir pipeline → `skills/engineering/devops-automator.md` |

**Regra:** quando a stack estiver fixa, substitui as células *A definir* e acrescenta variáveis de ambiente na secção correspondente.

---

## Estrutura de diretórios

```
Coachly/
├── skills/                      → Skills por domínio (ver secção dedicada)
│   ├── design/
│   ├── engineering/
│   ├── marketing/
│   ├── product/
│   ├── project-management/
│   ├── studio-operations/
│   ├── testing/
│   ├── front/
│   └── *.md                     → UI transversal (loading, erros, animação, etc.)
├── CLAUDE.md                    → Este ficheiro
├── README.md
└── (futuro) app/, components/, lib/, types/, supabase/, etc.
```

Quando o código existir, descreve aqui os caminhos reais (rotas, APIs, integrações IA, auth).

---

## Sistema de skills (`skills/`)

Todas as skills vivem na pasta **`skills/` na raiz do repositório** (não usar caminhos antigos como `.claude/skills/`).

### Regra de ouro — uso integral por domínio

1. **Identificar o domínio da tarefa** (design, engenharia, marketing, produto, gestão de projeto, operações de estúdio, testes).
2. **Ler e aplicar o conteúdo de todos os ficheiros `.md` dessa pasta**, não só um ou dois. O objetivo é alinhar o trabalho com o sistema completo de cada área.
3. Se a tarefa **cruzar domínios** (ex.: nova tela + API + copy), combina as pastas relevantes — cada uma envolvida deve ser coberta **na íntegra**.
4. Para **qualquer trabalho de interface** (componentes, páginas, folhas de estilo globais, fluxos visuais), além da pasta **`skills/design/`**, aplica também o **pacote UI transversal** abaixo.

### Pacote UI transversal (obrigatório com trabalho de UI)

Quando tocares na UI do Coachly, aplica **todos** estes ficheiros em conjunto com **`skills/design/`**:

| Ficheiro | Foco |
|----------|------|
| `skills/front/frontend-design.md` | Direção estética e qualidade de interface |
| `skills/animation-principles.md` | Animações com propósito, duração, easing |
| `skills/loading-states.md` | Skeletons, spinners, carregamento progressivo |
| `skills/error-handling-ux.md` | Prevenção, detecção, comunicação e recuperação de erros |
| `skills/ui-ux-pro-max.md` | UI/UX, acessibilidade, interação, responsividade |
| `skills/responsive-design.md` | Layouts adaptativos, mobile-first |
| `skills/dark-mode-design.md` | Modo escuro, contraste, hierarquia |

### Inventário por pasta (aplicar 100% quando o domínio se aplica)

#### `skills/design/`

| Ficheiro | Papel |
|----------|--------|
| `brand-guardian.md` | Consistência de marca e tom |
| `ui-designer.md` | UI, hierarquia, design systems, micro-interações |
| `ux-researcher.md` | Pesquisa, usabilidade, necessidades de utilizador |
| `visual-storyteller.md` | Narrativa visual |
| `whimsy-injector.md` | Personalidade e detalhe sem perder clareza |

#### `skills/engineering/`

| Ficheiro | Papel |
|----------|--------|
| `ai-engineer.md` | Integração e padrões de IA em produto |
| `backend-architect.md` | APIs, dados, arquitetura servidor |
| `devops-automator.md` | CI/CD, infra, automação |
| `frontend-developer.md` | Frontend web (ex.: React/Next), performance, a11y, qualidade de código |
| `mobile-app-builder.md` | Mobile / PWA / nativo — aplicar o que for transferível |
| `rapid-prototyper.md` | Iteração rápida e protótipos |

**Coachly:** rotas API, Server Actions, clientes de IA no servidor, persistência → cruzar **backend-architect** + **ai-engineer** quando existirem; UI → **frontend-developer**; deploy e pipelines → **devops-automator**.

#### `skills/marketing/`

| Ficheiro | Papel |
|----------|--------|
| `app-store-optimizer.md` | ASO |
| `content-creator.md` | Copy longo e curto, email, social |
| `growth-hacker.md` | Crescimento e experimentação |
| `instagram-curator.md` | Instagram |
| `reddit-community-builder.md` | Reddit |
| `tiktok-strategist.md` | TikTok |
| `x-twitter-strategist.md` | X/Twitter |

**Coachly:** textos de produto, onboarding, emails, redes e prompts de IA ligados a conteúdo → **content-creator**; canal específico → especialista da rede correspondente.

#### `skills/product/`

| Ficheiro | Papel |
|----------|--------|
| `feedback-synthesizer.md` | Síntese de feedback |
| `sprint-prioritizer.md` | Priorização, backlog, RICE/MoSCoW |
| `trend-researcher.md` | Tendências de mercado e produto |

**Coachly:** roadmap, MVP, escopo e decisões de prioridade → **sprint-prioritizer** + **feedback-synthesizer**; exploração de mercado/features → **trend-researcher** quando fizer sentido.

#### `skills/project-management/`

| Ficheiro | Papel |
|----------|--------|
| `experiment-tracker.md` | Experiências e aprendizagem |
| `project-shipper.md` | Entrega e ship |
| `studio-producer.md` | Produção e coordenação |

**Coachly:** fechos de ciclo, releases, critérios de “pronto” → estas três skills em conjunto.

#### `skills/studio-operations/`

| Ficheiro | Papel |
|----------|--------|
| `analytics-reporter.md` | Relatórios e métricas |
| `finance-tracker.md` | Finanças |
| `infrastructure-maintainer.md` | Manutenção de infra |
| `legal-compliance-checker.md` | Compliance |
| `support-responder.md` | Suporte |

**Coachly:** métricas de produto, relatórios internos → **analytics-reporter**; operações legais, suporte, finanças → ficheiros correspondentes quando a tarefa for operacional.

#### `skills/testing/`

| Ficheiro | Papel |
|----------|--------|
| `api-tester.md` | Testes de API |
| `performance-benchmarker.md` | Performance |
| `test-results-analyzer.md` | Análise de resultados de testes |
| `tool-evaluator.md` | Avaliação de ferramentas |
| `workflow-optimizer.md` | Otimização de fluxos de trabalho |

**Coachly:** antes de considerar uma feature estável, cruzar com **api-tester** + **performance-benchmarker** quando houver endpoints ou caminhos críticos; análise de falhas/regressões → **test-results-analyzer**.

### Mapa rápido: tipo de tarefa → pastas (íntegra)

| Tipo de tarefa | Pastas a aplicar na íntegra |
|----------------|-----------------------------|
| Nova tela, componente, tokens CSS | `design/` + pacote UI transversal |
| API, servidor, IA, dados | `engineering/` |
| Copy, redes, conteúdo no produto ou nos prompts | `marketing/` (+ `design/` se houver UI) |
| Roadmap, MVP, priorização | `product/` + `project-management/` |
| Relatórios, métricas, operações de estúdio | `studio-operations/` (+ `product/` se for decisão de produto) |
| QA, performance, contratos de API | `testing/` (+ `engineering/` se houver alteração de código) |

### Dependências externas (skills npm)

```bash
# Quando houver geração de imagem avançada (complemento a engineering + design)
npx skills i YouMind-OpenLab/nano-banana-pro-prompts-recommend-skill
```

---

## Padrões obrigatórios (quando existir código)

### Chamadas de IA
- Centralizar chamadas num **módulo de servidor** (ex.: `lib/<provider>.ts`) — evitar chamadas diretas espalhadas em componentes de UI.
- Passar **contexto de utilizador / programa / sessão** quando o produto exigir personalização (equivalente ao “contexto de cliente” de sistemas B2B).
- Preferir **JSON estruturado** nas respostas e parsing seguro no servidor.
- Alinhar prompts e tom com **`skills/marketing/`** e identidade com **`skills/design/`** quando aplicável.

### Dados e auth
- **Não** expor chaves secretas nem lógica sensível no cliente.
- Escrita em base de dados: **sempre** através de camada de confiança no servidor (API, Server Action, edge function), conforme a stack escolhida.
- Se usares Supabase (ou similar) com RLS, **respeita o modelo de segurança** documentado no projeto — não duplicar regras só em código de aplicação quando a política for na base de dados.

### Componentes e UI
- Alvos de toque adequados em mobile (ex.: mínimo ~44px onde fizer sentido).
- Estados de carregamento em fluxos lentos (IA, rede) — ver **`skills/loading-states.md`**.
- Usar tokens e componentes do **design system do Coachly** quando existirem; evitar misturar bibliotecas de UI sem decisão explícita no `CLAUDE.md` / README.

### TypeScript
- Tipos partilhados num módulo central (ex.: `types/`) quando o projeto for TypeScript.
- Evitar `any`; interfaces nomeadas para props de componentes.

### Commits
- Padrão semântico: `feat:`, `fix:`, `chore:`, `refactor:`
- Exemplo: `feat(onboarding): fluxo inicial de objetivos`

---

## Variáveis de ambiente

Documenta aqui as variáveis reais quando a stack estiver definida. Exemplo genérico:

```bash
# Exemplo — substituir pelos nomes reais do projeto
# DATABASE_URL=...
# API_KEY_*=...          # só servidor
# NEXT_PUBLIC_*=...      # só o que for seguro expor no cliente
```

---

## Roadmap de módulos

| Módulo | Documento / notas | Status |
|--------|-------------------|--------|
| Skills e governança | `skills/`, este `CLAUDE.md` | Em curso |
| Aplicação | *A criar* | Pendente |

Atualiza esta tabela quando existirem ficheiros tipo `SEMANA1.md`, épicos ou milestones.

---

## Decisões que devem permanecer explícitas

1. **Skills na raiz `skills/`** — inventário completo por domínio; uso integral conforme mapas acima.
2. **UI** — qualquer trabalho visual combina `skills/design/` + pacote UI transversal listado.
3. **IA e segredos** — servidor por defeito; cliente só consome resultados já seguros.
4. **Este ficheiro** — deve ser atualizado quando a stack, pastas ou decisões arquiteturais mudarem.

---

## Contato / repositório

- Atualiza com nome da equipa, responsáveis e URL do repositório remoto quando fizer sentido.
