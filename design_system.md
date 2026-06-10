# Design System — Santos Advocacia

> Sistema visual extraído da landing page de referência (apcardoso.adv.br) e adaptado à identidade da Santos Advocacia.
> O esqueleto visual — proporções, espaçamento, tipografia, hierarquia — é preservado. A camada cromática é totalmente reconstruída para a paleta azul-marinho + laranja da marca.

---

## 1. VISÃO GERAL DO ESTILO

### Adjetivos-chave
**Premium · Editorial · Institucional · Minimalista · Sofisticado · Jurídico · Clean · Confidente**

### Princípios fundadores
1. **Respiro acima de tudo.** O luxo do design vem do espaço em branco. Cada seção tem padding vertical generoso (96–160px). Cards têm padding interno amplo. Nada é apertado.
2. **Hierarquia tipográfica forte.** Um único título grande domina cada seção. Textos de apoio são pequenos e discretos, sempre em cinza. Não há competição visual.
3. **Cores como exceção, não regra.** O design vive de branco, off-white e azul-marinho escuro. O laranja aparece apenas em momentos pontuais de destaque (CTA principal, badges, ícones específicos).
4. **Composição editorial.** Layouts assimétricos (texto à esquerda + imagem à direita, e vice-versa) que lembram revistas de arquitetura ou catálogos premium.
5. **Detalhes pequenos, mas precisos.** Setas circulares nos cards, numeração "01" discreta, eyebrow texts em maiúsculas, raio de borda consistente. Detalhes definem a qualidade percebida.

### O que **preservar** da página original
- Estrutura geral das seções e seu fluxo vertical
- Proporções de espaçamento (padding vertical generoso, gaps modulares)
- Hierarquia tipográfica (título grande → subtítulo cinza pequeno → corpo regular)
- Cards com cantos arredondados, numeração e seta circular
- Layouts assimétricos (texto + imagem lado a lado)
- Fotografia profissional em ambiente neutro
- Footer escuro de alto contraste com colunas
- Botões pill com seta circular interna

### O que **alterar** por causa da nova paleta
- Substituir todo preto puro (#0a0a0a) por **azul-marinho escuro #041A3D** — preserva o contraste e a sobriedade, mas alinha à marca
- Trocar fundo cinza neutro de seções por **off-white levemente azulado #F2F5F9**
- Cor de texto secundário muda do cinza neutro original para **cinza azulado #666B79**, que conversa com o azul-marinho
- Introduzir **laranja #EE6722 como cor de destaque pontual** — botões secundários, ícones de "Plantão 24h", indicadores ativos, hover states
- O footer escuro original (preto) passa a usar **azul-marinho escuro #041A3D** como base
- Botões CTA principais passam a usar azul-marinho como cor de fundo, e a seta circular interna fica em laranja (detalhe sutil de marca)

---

## 2. TOKENS DE COR

### Paleta primária (marca)

| Token | Hex | Uso |
|---|---|---|
| `--color-primary` | `#07275F` | Cor principal da marca. Botões primários, links, ícones, headings de destaque. |
| `--color-primary-dark` | `#041A3D` | Texto escuro, headings principais, fundo do footer, hover de botões. Substitui o "preto" da referência. |
| `--color-primary-darker` | `#020E22` | Estados pressed/active de botões escuros. Uso raro. |

### Escala azul-marinho estendida (para uso flexível)

| Token | Hex | Uso |
|---|---|---|
| `--color-primary-50` | `#EBEFF7` | Fundo sutil para badges, alerts informativos. |
| `--color-primary-100` | `#D2DBEC` | Hover sutil, divisores. |
| `--color-primary-300` | `#7E92BB` | Estados disabled. |
| `--color-primary-500` | `#07275F` | = primary. |
| `--color-primary-700` | `#041A3D` | = primary-dark. |
| `--color-primary-900` | `#020E22` | = primary-darker. |

### Cor de destaque (uso parcimonioso)

| Token | Hex | Uso |
|---|---|---|
| `--color-accent` | `#EE6722` | Destaque. CTA secundário, badge "Plantão 24h", ícones-chave, hover em links importantes. |
| `--color-accent-hover` | `#D9551A` | Hover do laranja. |
| `--color-accent-soft` | `#FDE9DC` | Fundo de badges/tags em laranja claro. |

**Regra de ouro do laranja:** não deve ocupar mais de **5% da composição visual de qualquer tela**. Se um botão laranja já existe no hero, evite um segundo no mesmo dobramento. Pense no laranja como sublinhado, não como bloco.

### Neutros (cinzas institucionais)

| Token | Hex | Uso |
|---|---|---|
| `--color-neutral-900` | `#111111` | Texto escuro alternativo (uso raro, prefira `primary-dark`). |
| `--color-neutral-700` | `#666B79` | Texto secundário, descrições de cards, parágrafos de apoio. |
| `--color-neutral-500` | `#98A3B8` | Texto terciário, eyebrows, captions, placeholders. |
| `--color-neutral-300` | `#C9D1DE` | Bordas de cards, divisores, inputs. |
| `--color-neutral-200` | `#E3E8F0` | Bordas extra-sutis, separadores horizontais finos. |
| `--color-neutral-100` | `#F2F5F9` | Fundo de seções alternadas (substitui o cinza claro do referência). |
| `--color-neutral-50`  | `#F8FAFB` | Off-white principal, fundo de páginas. |
| `--color-white` | `#FFFFFF` | Cards, fundos de hero, contraste máximo. |

### Cores semânticas (estendidas)

| Token | Hex | Uso |
|---|---|---|
| `--color-success` | `#1F7A4D` | Confirmações, badges positivos. |
| `--color-warning` | `#C77900` | Avisos. |
| `--color-error` | `#B83232` | Erros de formulário. |

### Tabela de aplicação — substituições diretas vs referência

| Elemento original (apcardoso) | Cor original | Novo token | Hex novo |
|---|---|---|---|
| Texto preto principal | `#0a0a0a` | `--color-primary-dark` | `#041A3D` |
| Background página | `#FFFFFF` | `--color-white` | `#FFFFFF` |
| Background seção "Áreas" | `#F5F5F5` | `--color-neutral-100` | `#F2F5F9` |
| Texto cinza secundário | `#666` | `--color-neutral-700` | `#666B79` |
| Eyebrow / labels pequenas | `#999` | `--color-neutral-500` | `#98A3B8` |
| Bordas sutis | `#E5E5E5` | `--color-neutral-200` | `#E3E8F0` |
| Footer preto | `#0a0a0a` | `--color-primary-dark` | `#041A3D` |
| Botão CTA preenchido | `#0a0a0a` | `--color-primary-dark` | `#041A3D` |
| Seta dentro do botão pill | `#FFFFFF` | `--color-accent` | `#EE6722` *(detalhe novo)* |

---

## 3. TOKENS DE TIPOGRAFIA

### Famílias

**Opção A — Sans-serif moderna (fiel à referência)**
- **Display & Body:** `Inter Tight` (Google Fonts) — variável, peso 300 a 700
- Fallback: `Inter`, `-apple-system`, `Segoe UI`, sans-serif
- Vantagem: limpa, técnica, geometria precisa. Combina com o tom "sério e técnico" do briefing.

**Opção B — Combo editorial (mais sofisticado)**
- **Display (títulos H1, H2):** `Fraunces` (Google Fonts) — peso 400 a 600, com axis opcional "soft"
- **Body, botões e UI:** `Inter` (Google Fonts) — peso 400 a 600
- Vantagem: a serifa moderna acrescenta peso editorial/institucional, diferencia o escritório no mercado.

**Recomendação:** **Opção A** se a prioridade é técnica e neutralidade. **Opção B** se a prioridade é diferenciação editorial (recomendado para advocacia premium).

### Escala tipográfica

Sistema modular baseado em uma escala de razão `1.25` (Major Third), ajustada visualmente.

| Token | Tamanho | Line-height | Letter-spacing | Peso | Uso |
|---|---|---|---|---|---|
| `--font-display-2xl` | 72px | 1.05 | -0.03em | 600 | H1 do hero (desktop). Mobile: 44px. |
| `--font-display-xl` | 56px | 1.08 | -0.025em | 600 | H2 de seções principais (desktop). Mobile: 36px. |
| `--font-display-lg` | 40px | 1.15 | -0.02em | 500 | Títulos secundários, blocos de CTA. Mobile: 30px. |
| `--font-heading-md` | 24px | 1.25 | -0.015em | 600 | Títulos de cards (ex.: "Direito Penal"). |
| `--font-heading-sm` | 20px | 1.3 | -0.01em | 500 | Subtítulos, títulos de seção menores. |
| `--font-body-lg` | 18px | 1.6 | 0 | 400 | Parágrafos do hero, textos institucionais maiores. |
| `--font-body-md` | 16px | 1.65 | 0 | 400 | Parágrafos padrão, descrições de cards. |
| `--font-body-sm` | 14px | 1.55 | 0 | 400 | Texto de apoio, legendas, listas de credenciais. |
| `--font-eyebrow` | 13px | 1.4 | 0.12em | 500 | "Advocacia Criminal & Compliance" — texto pequeno em maiúsculas acima de títulos. |
| `--font-caption` | 12px | 1.4 | 0.05em | 500 | Labels de cards de contato ("Telefone & WhatsApp"). |
| `--font-button` | 14px | 1 | 0.01em | 500 | Botões em geral. |

### Regras tipográficas

- **Eyebrow:** sempre em maiúsculas, com letter-spacing aberto (0.12em), em `--color-neutral-500`. Posicionado acima do título principal de cada seção, centralizado ou alinhado conforme o layout.
- **H1 e H2:** sempre em `--color-primary-dark` (#041A3D). Nunca em laranja.
- **Body:** sempre em `--color-neutral-700` (#666B79). Texto principal escuro só em casos de destaque pontual.
- **Listas com bullets:** os bullets podem ser pontos personalizados em `--color-primary` (azul-marinho) ou ícones discretos, nunca laranja.
- **Links inline:** `--color-primary` com sublinhado animado (underline offset 4px). Hover: muda para `--color-accent`.
- **Números grandes em cards** (ex.: "01", "02"): `--font-body-sm` em `--color-neutral-500`, com letter-spacing apertado.

---

## 4. TOKENS DE ESPAÇAMENTO

Sistema modular baseado em **4px** (compatível com Tailwind).

| Token | Valor | Uso típico |
|---|---|---|
| `--space-1` | 4px | Gaps mínimos, padding interno de ícones. |
| `--space-2` | 8px | Gap entre ícone e texto, entre tags. |
| `--space-3` | 12px | Espaçamento entre elementos próximos. |
| `--space-4` | 16px | Padding interno de botões pequenos, gap entre itens em listas. |
| `--space-6` | 24px | Padding horizontal padrão em mobile, gap entre cards pequenos. |
| `--space-8` | 32px | Padding interno de cards padrão. |
| `--space-10` | 40px | Margens entre blocos relacionados dentro de uma seção. |
| `--space-12` | 48px | Padding horizontal de containers em tablet. |
| `--space-16` | 64px | Padding horizontal de containers em desktop. |
| `--space-20` | 80px | Espaçamento vertical médio entre subseções. |
| `--space-24` | 96px | Padding vertical mínimo de seções em desktop. |
| `--space-32` | 128px | Padding vertical generoso de seções principais. |
| `--space-40` | 160px | Padding vertical máximo (hero, transições importantes). |

### Padrão de aplicação por contexto

- **Seções inteiras (vertical):** `--space-24` a `--space-32` (96–128px) em desktop. `--space-16` a `--space-20` (64–80px) em mobile.
- **Entre título e subtítulo:** `--space-3` (12px).
- **Entre subtítulo e conteúdo:** `--space-12` a `--space-16` (48–64px).
- **Padding interno de cards:** `--space-8` (32px), ocasionalmente `--space-10` (40px) em cards grandes.
- **Gap entre cards no grid:** `--space-5` a `--space-6` (20–24px).
- **Container horizontal:** `--space-6` (24px) mobile, `--space-16` (64px) desktop.

---

## 5. GRID E LAYOUT

### Container principal
- **Max-width:** `1200px` (≈ Tailwind `max-w-6xl` ou `max-w-7xl`).
- **Padding lateral:** `24px` mobile, `48px` tablet, `64px` desktop.
- **Centralização:** sempre `margin: 0 auto`.

### Sistema de grid
- **Desktop:** grid de 12 colunas, gap de `24px`.
- **Tablet:** grid de 8 colunas, gap de `20px`.
- **Mobile:** grid de 4 colunas (na prática, layout single-column), gap de `16px`.

### Breakpoints recomendados (compatíveis com Tailwind)
- `sm`: 640px
- `md`: 768px
- `lg`: 1024px
- `xl`: 1280px
- `2xl`: 1536px

### Padrões de layout por seção

| Seção | Layout desktop | Comportamento mobile |
|---|---|---|
| **Hero** | 3 colunas (texto pequeno esq · imagem central · texto pequeno dir), texto principal acima centralizado | Stack vertical: título → imagem → textos de apoio |
| **Áreas de atuação** | Grid 3 colunas × 2 linhas (5 cards + 1 célula textual) | 1 coluna empilhada |
| **Sobre o advogado** | 2 colunas (imagem 5/12 esq + texto 7/12 dir) | Imagem topo + texto abaixo |
| **CTA intermediário** | 2 colunas (texto 7/12 esq + imagem 5/12 dir) | Imagem topo + texto abaixo |
| **Contato** | 2 colunas (4 cards 5/12 esq + mapa 7/12 dir) | Cards empilhados + mapa abaixo |
| **Footer** | 4 colunas (logo + 3 colunas de links) | Stack vertical |

### Border radius global

| Token | Valor | Uso |
|---|---|---|
| `--radius-sm` | 8px | Tags, badges pequenos, inputs. |
| `--radius-md` | 12px | Botões secundários, cards pequenos. |
| `--radius-lg` | 16px | Cards padrão de áreas de atuação. |
| `--radius-xl` | 20px | Cards grandes, blocos institucionais. |
| `--radius-2xl` | 24px | Imagens do hero e seção sobre. |
| `--radius-full` | 9999px | Botões pill, avatares, indicadores. |

---

## 6. COMPONENTES

### 6.1 Header

```
[Logo Santos Advocacia]    [Sobre · Atuação · Contato]    [Fale Conosco →]
```

**Especificações:**
- **Posição:** sticky no topo, com leve sombra após scroll (`box-shadow: 0 4px 24px rgba(4, 26, 61, 0.04)`).
- **Altura:** 80px desktop, 64px mobile.
- **Background:** `--color-white` (translúcido com `backdrop-filter: blur(12px)` para efeito premium).
- **Padding lateral:** alinhado ao container.
- **Logo:** altura 40px, alinhamento vertical centralizado.
- **Menu:** centralizado horizontalmente, links em `--font-button` (14px), peso 500, cor `--color-primary-dark`. Hover: `--color-accent`.
- **CTA do header:** botão pill pequeno em `--color-primary-dark`, texto branco. Seta `→` em laranja (`--color-accent`).

### 6.2 Botões / CTAs

**Variantes:**

**Primário (`btn-primary`)** — para CTA principal
- Background: `--color-primary-dark` (#041A3D)
- Texto: branco
- Border-radius: `--radius-full` (pill)
- Padding: `14px 28px` (com seta circular: `8px 8px 8px 24px`)
- Seta circular interna: 32×32px, background branco, ícone "→" em `--color-accent`
- Hover: background `--color-primary` (azul-marinho médio), leve transform `translateY(-2px)`, shadow `0 10px 30px rgba(4, 26, 61, 0.18)`
- Transição: 200ms ease

**Secundário (`btn-secondary`)** — para ações de apoio
- Background: transparente
- Border: `1px solid var(--color-neutral-300)`
- Texto: `--color-primary-dark`
- Border-radius: `--radius-full`
- Padding: `14px 28px`
- Hover: border `--color-primary-dark`, background `--color-neutral-50`

**Destaque / Acento (`btn-accent`)** — uso muito pontual (ex.: "Plantão 24h", "Emergência")
- Background: `--color-accent` (#EE6722)
- Texto: branco
- Demais propriedades iguais ao primário
- **Regra:** no máximo 1 botão accent por viewport visível

**Botão circular com seta (`btn-icon-arrow`)** — usado dentro de cards
- Diâmetro: 36px
- Background: `--color-white` com border `1px solid var(--color-neutral-200)`
- Ícone: seta `→` em `--color-primary-dark`
- Hover: background `--color-primary-dark`, seta branca

### 6.3 Cards de áreas de atuação

**Anatomia:**
```
┌─────────────────────────────┐
│  01                    →    │
│                             │
│  Direito Penal              │
│                             │
│  Defesa de acusados e       │
│  assistência à vítima em    │
│  todas as fases da          │
│  persecução penal.          │
│                             │
└─────────────────────────────┘
```

**Especificações:**
- Background: `--color-white`
- Border: `1px solid var(--color-neutral-200)` (opcional — também funciona sem borda em fundo claro)
- Border-radius: `--radius-lg` (16px)
- Padding: 32px
- Shadow: nenhuma por padrão. Hover: `0 12px 32px rgba(4, 26, 61, 0.06)`
- **Número** (canto superior esquerdo): `--font-body-sm` em `--color-neutral-500`, peso 500
- **Seta circular** (canto superior direito): componente `btn-icon-arrow`
- **Título** (depois de espaço de 48–64px): `--font-heading-md` em `--color-primary-dark`, peso 600
- **Descrição** (depois de 12px): `--font-body-sm` em `--color-neutral-700`
- **Hover do card todo:** leve elevação (`translateY(-4px)`), shadow ativa, seta circular muda para variante invertida
- **Transição:** 250ms ease em todas as propriedades

### 6.4 Cards de contato (formato linha horizontal)

**Anatomia:**
```
┌────────────────────────────────────────┐
│  TELEFONE & WHATSAPP             →     │
│  +55 (11) 95419-5262                   │
└────────────────────────────────────────┘
```

**Especificações:**
- Background: `--color-white`
- Border: `1px solid var(--color-neutral-200)`
- Border-radius: `--radius-lg`
- Padding: `20px 24px`
- **Label** (linha superior): `--font-caption` em `--color-neutral-500`, maiúsculas
- **Valor** (linha principal): `--font-body-md` em `--color-primary-dark`, peso 500
- **Seta circular** à direita: alinhada verticalmente ao centro
- Hover: border `--color-primary` (azul-marinho), seta vira `--color-primary-dark` com fundo claro

### 6.5 Bloco de endereço (card escuro)

- Background: `--color-primary-dark` (#041A3D)
- Texto: branco
- Border-radius: `--radius-lg`
- Padding: 24px
- **Label "Escritório":** `--font-caption` em `--color-neutral-500`, maiúsculas
- **Texto do endereço:** `--font-body-sm` em branco, line-height 1.6
- Variante alternativa: mesmo bloco com fundo `--color-primary` (#07275F) como toque suave de marca

### 6.6 Imagens

**Imagem do hero:**
- Formato: retrato (3:4 ou 4:5), altura aproximada de 600–700px
- Border-radius: `--radius-2xl` (24px)
- Largura: 35–40% do container
- Tratamento: fotografia profissional em fundo claro neutro, light natural

**Imagem da seção "Sobre":**
- Formato: retrato, altura ~560px
- Border-radius: `--radius-xl` (20px)
- Posição: alinhada à esquerda, ocupando 5/12 colunas

**Imagem do CTA intermediário ("Soluções integradas"):**
- Formato: retrato, fundo escuro ou monocromático
- Border-radius: `--radius-xl`
- Tratamento sugerido: fotografia com fundo escuro contrastando com o texto à esquerda

**Regras gerais para fotos:**
- Sempre em fundos neutros (off-white, cinza muito claro, ou preto suave)
- Roupa formal, postura confiante, expressão serena
- Evitar cenários ostensivos (livros de direito atrás, martelos, balanças)
- Tratamento de cor: levemente desaturado, com leve tom frio (combina com a paleta azulada)
- Sempre com `object-fit: cover` e altura definida para uniformidade

### 6.7 Mapa

- Container com `border-radius: --radius-lg`
- Border: `1px solid var(--color-neutral-200)`
- Altura mínima: 320px desktop, 280px mobile
- Embed do Google Maps com tema "Silver" ou "Subtle Grayscale" para harmonizar
- Pin customizado opcional em `--color-accent` (laranja) — único momento em que o laranja aparece em mapa

### 6.8 Footer

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│  [Logo]              Navegação    Credenciais        Social        │
│  Tagline             Sobre        OAB/SP 438.577     Instagram     │
│                      Atuação      Membro OAB SP      WhatsApp      │
│                      Contato      Membro IBCCRIM                   │
│                                                                     │
│  ────────────────────────────────────────────────────────────────  │
│                                                                     │
│  © 2026 Santos Advocacia — Todos os direitos reservados.            │
│                                          São Paulo, SP — Brasil    │
└─────────────────────────────────────────────────────────────────────┘
```

**Especificações:**
- Background: `--color-primary-dark` (#041A3D)
- Texto principal: branco com 90% de opacidade
- Texto secundário (labels de coluna): `--color-neutral-500`
- Padding vertical: 80px desktop, 56px mobile
- Padding horizontal: alinhado ao container
- Divisor antes do copyright: linha 1px com opacidade 10% sobre branco
- Logo: versão monocromática (branca)
- Links: hover muda cor para `--color-accent` (único toque de laranja no footer)
- Copyright: `--font-body-sm`, opacidade 60%

### 6.9 Eyebrow (texto pequeno acima de títulos)

- `--font-eyebrow` (13px)
- Maiúsculas, letter-spacing 0.12em
- Cor: `--color-neutral-500`
- Pode ter um pequeno `○` ou `—` como prefixo visual (como no referência)
- Margem inferior: 24px

### 6.10 Lista de credenciais (bullets)

- Cada item em flex row, com bullet (•) ou ponto azul-marinho à esquerda
- Bullet: 6px de diâmetro, `--color-primary`, alinhado verticalmente ao center da primeira linha
- Texto: `--font-body-sm` em `--color-neutral-700`
- Gap entre itens: 12px
- Padding-left no bullet: 16px

---

## 7. DIRETRIZES DE USO

### Como usar espaçamentos
1. **Sempre prefira espaços maiores.** Quando em dúvida entre 64px e 96px, escolha 96px.
2. **Mantenha ritmo vertical.** Distâncias entre seções devem se repetir (ex.: sempre 128px entre seções principais).
3. **Não preencha espaços vazios "porque está vazio".** O espaço em branco é parte do design.

### Como usar botões
1. **Um único botão primário por seção** (no máximo dois quando há um secundário ao lado).
2. **Laranja somente para urgência ou destaque excepcional.** Ex.: "Plantão 24h", "Emergência", "Atendimento Imediato".
3. **Botões pill (radius-full) são o padrão.** Botões retangulares só em casos muito específicos (formulários).
4. **A seta interna circular dá personalidade.** Use em todos os CTAs principais.

### Como criar cards
1. Cantos arredondados grandes (`--radius-lg` mínimo).
2. Padding interno generoso (mínimo 24px).
3. Numeração + seta circular nos cards de áreas de atuação.
4. Background branco sobre fundo cinza-azulado claro (ou vice-versa em seções alternadas).
5. Hover sempre presente — uma elevação sutil e uma sombra discreta.

### Como tratar imagens
1. Sempre com `border-radius`. Imagens com cantos retos quebram o sistema.
2. Fotografia profissional obrigatória — nada de stock genérico.
3. Fundos neutros, sem competição visual.
4. Tratamento de cor consistente: levemente desaturado, com leve tom frio.

### Como organizar seções
1. **Alternância de fundos:** branco → cinza-azulado claro → branco → cinza... cria ritmo.
2. **Layouts assimétricos** (imagem + texto lado a lado) devem alternar a posição da imagem (uma seção esquerda, outra direita).
3. **Cada seção tem um único objetivo.** Não tente comunicar duas coisas no mesmo bloco.
4. **Cada seção começa com eyebrow + título.** Mantém o ritmo editorial.

### Como manter o visual elegante e institucional
1. **Discrição cromática.** Se algo está chamando atenção demais, está errado.
2. **Tipografia faz o trabalho pesado.** Bons tamanhos e bons pesos já criam hierarquia sem precisar de cores.
3. **Detalhes precisos.** Cantos arredondados, alinhamentos, espaçamentos consistentes — é nesses detalhes que mora a percepção de qualidade.
4. **Menos texto, mais respiro.** Cortar metade do texto sempre torna o design melhor.
5. **Confidence, não loudness.** Advocacia premium se comunica com calma, não com gritos visuais.

---

## 8. EXEMPLO DE APLICAÇÃO VISUAL (descrição cromática)

### Hero
- Background: `--color-white`
- Eyebrow "Advocacia Criminal & Compliance" em `--color-neutral-500`
- H1 "Defesa técnica, ágil e estratégica para o seu caso." em `--color-primary-dark`
- Botão CTA primário "Fale agora pelo WhatsApp →" em `--color-primary-dark` com seta laranja
- Imagem retrato no centro, cantos `--radius-2xl`
- Texto lateral esquerdo: bio curta em `--color-neutral-700`
- Texto lateral direito: descrição de atuação + OAB em `--color-neutral-700`

### Seção Áreas de Atuação
- Background: `--color-neutral-100` (off-white levemente azulado)
- Título centralizado em `--color-primary-dark`
- Subtítulo em `--color-neutral-700`
- Grid 3×2 de cards brancos
- Última célula (textual): "○ Soluções integradas — Cada caso é único" em peso regular

### Seção Sobre o Advogado
- Background: `--color-white`
- Foto à esquerda, texto à direita
- H2 "Douglas Santos." em `--color-primary-dark`
- Bullets de credenciais com ponto em `--color-primary`

### CTA Intermediário "Soluções integradas"
- Background: `--color-white`
- Título grande à esquerda em `--color-primary-dark`
- Imagem retrato escura à direita
- Botão "Falar pelo WhatsApp →" em `--color-primary-dark`

### Footer
- Background: `--color-primary-dark`
- Texto branco
- Links com hover em `--color-accent`

---

## 9. IMPLEMENTAÇÃO — CSS VARIABLES

```css
:root {
  /* === CORES === */

  /* Primário (marca) */
  --color-primary: #07275F;
  --color-primary-dark: #041A3D;
  --color-primary-darker: #020E22;

  /* Escala primária estendida */
  --color-primary-50: #EBEFF7;
  --color-primary-100: #D2DBEC;
  --color-primary-300: #7E92BB;
  --color-primary-500: #07275F;
  --color-primary-700: #041A3D;
  --color-primary-900: #020E22;

  /* Destaque (laranja) */
  --color-accent: #EE6722;
  --color-accent-hover: #D9551A;
  --color-accent-soft: #FDE9DC;

  /* Neutros */
  --color-neutral-900: #111111;
  --color-neutral-700: #666B79;
  --color-neutral-500: #98A3B8;
  --color-neutral-300: #C9D1DE;
  --color-neutral-200: #E3E8F0;
  --color-neutral-100: #F2F5F9;
  --color-neutral-50:  #F8FAFB;
  --color-white: #FFFFFF;

  /* Semânticas */
  --color-success: #1F7A4D;
  --color-warning: #C77900;
  --color-error: #B83232;

  /* === TIPOGRAFIA === */
  --font-display: 'Inter Tight', 'Inter', -apple-system, sans-serif;
  --font-body: 'Inter', -apple-system, sans-serif;
  /* Alternativa editorial: --font-display: 'Fraunces', Georgia, serif; */

  --font-size-display-2xl: clamp(2.75rem, 6vw, 4.5rem);  /* 44–72px */
  --font-size-display-xl:  clamp(2.25rem, 4.5vw, 3.5rem); /* 36–56px */
  --font-size-display-lg:  clamp(1.875rem, 3.5vw, 2.5rem); /* 30–40px */
  --font-size-heading-md:  1.5rem;   /* 24px */
  --font-size-heading-sm:  1.25rem;  /* 20px */
  --font-size-body-lg:     1.125rem; /* 18px */
  --font-size-body-md:     1rem;     /* 16px */
  --font-size-body-sm:     0.875rem; /* 14px */
  --font-size-eyebrow:     0.8125rem; /* 13px */
  --font-size-caption:     0.75rem;  /* 12px */
  --font-size-button:      0.875rem; /* 14px */

  /* === ESPAÇAMENTO === */
  --space-1:  0.25rem;
  --space-2:  0.5rem;
  --space-3:  0.75rem;
  --space-4:  1rem;
  --space-6:  1.5rem;
  --space-8:  2rem;
  --space-10: 2.5rem;
  --space-12: 3rem;
  --space-16: 4rem;
  --space-20: 5rem;
  --space-24: 6rem;
  --space-32: 8rem;
  --space-40: 10rem;

  /* === BORDER RADIUS === */
  --radius-sm:   0.5rem;
  --radius-md:   0.75rem;
  --radius-lg:   1rem;
  --radius-xl:   1.25rem;
  --radius-2xl:  1.5rem;
  --radius-full: 9999px;

  /* === SHADOWS === */
  --shadow-card:       0 4px 16px rgba(4, 26, 61, 0.04);
  --shadow-card-hover: 0 12px 32px rgba(4, 26, 61, 0.08);
  --shadow-button:     0 10px 30px rgba(4, 26, 61, 0.18);
  --shadow-header:     0 4px 24px rgba(4, 26, 61, 0.04);

  /* === LAYOUT === */
  --container-max: 1200px;
  --container-padding-mobile: 1.5rem;
  --container-padding-desktop: 4rem;

  /* === TRANSITIONS === */
  --transition-fast: 150ms ease;
  --transition-base: 250ms ease;
  --transition-slow: 400ms ease;
}
```

---

## 10. IMPLEMENTAÇÃO — TAILWIND THEME

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: {
          DEFAULT: '#07275F',
          dark: '#041A3D',
          darker: '#020E22',
          50:  '#EBEFF7',
          100: '#D2DBEC',
          300: '#7E92BB',
          500: '#07275F',
          700: '#041A3D',
          900: '#020E22',
        },
        accent: {
          DEFAULT: '#EE6722',
          hover: '#D9551A',
          soft: '#FDE9DC',
        },
        neutral: {
          50:  '#F8FAFB',
          100: '#F2F5F9',
          200: '#E3E8F0',
          300: '#C9D1DE',
          500: '#98A3B8',
          700: '#666B79',
          900: '#111111',
        },
      },
      fontFamily: {
        display: ['"Inter Tight"', 'Inter', 'system-ui', 'sans-serif'],
        body: ['Inter', 'system-ui', 'sans-serif'],
        // Alternativa editorial:
        // serif: ['Fraunces', 'Georgia', 'serif'],
      },
      fontSize: {
        'display-2xl': ['clamp(2.75rem, 6vw, 4.5rem)',   { lineHeight: '1.05', letterSpacing: '-0.03em', fontWeight: '600' }],
        'display-xl':  ['clamp(2.25rem, 4.5vw, 3.5rem)', { lineHeight: '1.08', letterSpacing: '-0.025em', fontWeight: '600' }],
        'display-lg':  ['clamp(1.875rem, 3.5vw, 2.5rem)',{ lineHeight: '1.15', letterSpacing: '-0.02em', fontWeight: '500' }],
        'heading-md':  ['1.5rem',    { lineHeight: '1.25', letterSpacing: '-0.015em', fontWeight: '600' }],
        'heading-sm':  ['1.25rem',   { lineHeight: '1.3',  letterSpacing: '-0.01em',  fontWeight: '500' }],
        'body-lg':     ['1.125rem',  { lineHeight: '1.6',  fontWeight: '400' }],
        'body-md':     ['1rem',      { lineHeight: '1.65', fontWeight: '400' }],
        'body-sm':     ['0.875rem',  { lineHeight: '1.55', fontWeight: '400' }],
        'eyebrow':     ['0.8125rem', { lineHeight: '1.4',  letterSpacing: '0.12em', fontWeight: '500' }],
        'caption':     ['0.75rem',   { lineHeight: '1.4',  letterSpacing: '0.05em', fontWeight: '500' }],
      },
      borderRadius: {
        'sm':   '0.5rem',
        'md':   '0.75rem',
        'lg':   '1rem',
        'xl':   '1.25rem',
        '2xl':  '1.5rem',
      },
      boxShadow: {
        'card':       '0 4px 16px rgba(4, 26, 61, 0.04)',
        'card-hover': '0 12px 32px rgba(4, 26, 61, 0.08)',
        'button':     '0 10px 30px rgba(4, 26, 61, 0.18)',
        'header':     '0 4px 24px rgba(4, 26, 61, 0.04)',
      },
      maxWidth: {
        'container': '1200px',
      },
      spacing: {
        '18': '4.5rem',
        '22': '5.5rem',
        '30': '7.5rem',
      },
      transitionDuration: {
        'base': '250ms',
      },
    },
  },
};
```

---

## 11. RESUMO — DECISÕES CRÍTICAS

### Preservar 100% da referência
- ✅ Estrutura de seções e ordem vertical
- ✅ Proporções de espaçamento e respiro
- ✅ Hierarquia tipográfica (eyebrow → título grande → corpo cinza)
- ✅ Cards com numeração + seta circular
- ✅ Layouts assimétricos com fotos retangulares de cantos arredondados
- ✅ Botões pill com seta circular interna
- ✅ Footer escuro com colunas
- ✅ Cards de contato em formato linha horizontal

### Alterar pela nova paleta
- 🔄 Preto puro → **azul-marinho escuro #041A3D** (texto, footer, botões primários)
- 🔄 Cinza neutro de fundo → **off-white azulado #F2F5F9** (seções alternadas)
- 🔄 Cinza secundário → **cinza azulado #666B79** (alinhado à paleta)
- ➕ **Laranja #EE6722** introduzido como destaque (setas internas, badge "Plantão 24h", hover de links, pin do mapa)
- 🔄 Footer preto → **azul-marinho escuro #041A3D**

### Identidade Santos Advocacia (vs Anna Paulina)
- Mais **frio e técnico** (azul-marinho) em vez de **neutro absoluto** (preto)
- Toque de **personalidade** com o laranja em momentos pontuais — sem perder a sobriedade
- Mesma sensação de **escritório premium**, mas com a alma da marca aparecendo nos detalhes

---

> Este design system é vivo. À medida que novos componentes forem necessários (formulários, modais, banners, conteúdo de blog, etc.), eles devem ser construídos respeitando os mesmos princípios: respiro generoso, hierarquia tipográfica clara, cromática contida e detalhes precisos.
