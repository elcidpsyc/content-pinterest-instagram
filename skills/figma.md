---
name: figma
description: Design and generate visual content using Figma. Creates detailed, ready-to-implement Figma specifications including frames, components, auto-layout, text styles, color styles, and design tokens. Specializes in building reusable design systems for Pinterest Pins (1000x1500px), Instagram posts/carousels, and minimalist psychology-themed content. Generates step-by-step Figma instructions and JSON-ready design tokens the user can apply directly.
---

# Figma Design Skill

Gera especificações completas para Figma — desde frames individuais até sistemas de design reutilizáveis — com foco em conteúdo minimalista para Pinterest e Instagram. Ideal para quem quer consistência visual escalável com componentes e estilos reaproveitáveis.

## Conhecimento Base do Figma

### Conceitos Essenciais
- **Frame**: container principal do design (equivale ao "artboard")
- **Component**: elemento reutilizável (define uma vez, usa em vários lugares)
- **Variant**: variação de um componente (ex: slide-escuro / slide-claro)
- **Auto Layout**: organiza elementos automaticamente com espaçamento consistente
- **Text Style**: estilo de texto salvo globalmente (Heading, Body, Caption...)
- **Color Style**: cor salva globalmente (Primary, Background, Accent...)
- **Design Token**: valores de design exportáveis como JSON (cores, tipografia, espaçamentos)
- **Constraints**: define como um elemento se comporta ao redimensionar o frame

### Dimensões por Plataforma
| Formato | Frame Size | Proporção |
|---|---|---|
| Pinterest Pin | 1000 × 1500 | 2:3 |
| Pinterest Pin longo | 1000 × 2100 | 1:2.1 |
| Instagram Post | 1080 × 1080 | 1:1 |
| Instagram Portrait | 1080 × 1350 | 4:5 |
| Instagram Story | 1080 × 1920 | 9:16 |
| Instagram Carousel | 1080 × 1080 (por slide) | 1:1 |

### Plugins Úteis no Figma
- **Unsplash** — imagens de referência gratuitas
- **Content Reel** — preenche texto com conteúdo real
- **Iconify** — biblioteca de ícones line art (Material Symbols, Phosphor, Feather)
- **Figma Tokens / Token Studio** — gerencia design tokens em JSON
- **Contrast** — verifica acessibilidade de cor
- **Batch Styler** — aplica estilos em lote
- **LottieFiles** — animações para Stories/Reels

### Tipografia Figma (Google Fonts disponíveis via plugin)
**Serif elegantes:**
- Cormorant Garamond (400, 600, 700, Italic)
- Playfair Display (400, 700, Italic)
- EB Garamond (400, 500, Italic)
- Libre Baskerville (400, 700)

**Sans-serif limpas:**
- DM Sans (300, 400, 500)
- Inter (300, 400, 500, 600)
- Lato (300, 400, 700)
- Montserrat (300, 400, 600)

**Escalas tipográficas recomendadas (Pinterest 1000px):**
```
Display:  56–72px / Line-height: 1.1 / Letter-spacing: -0.5
Heading:  36–48px / Line-height: 1.2 / Letter-spacing: -0.3
Subhead:  24–30px / Line-height: 1.3
Body:     18–22px / Line-height: 1.6
Caption:  13–15px / Line-height: 1.5 / Letter-spacing: 0.5
```

---

## Workflow

Crie uma lista de tarefas e trabalhe uma por vez.

### 1. Receber o Briefing

Obtenha do contexto ou pergunte:
- Plataforma e formato (Pin, carrossel, post)
- Copy já definida (títulos, subtextos, citações)
- Precisa de componentes reutilizáveis ou frame único?
- Exportar como PNG, SVG ou entregar especificações?

### 2. Definir Design Tokens

Antes de montar o frame, defina os tokens da paleta:

```json
{
  "color": {
    "background": {
      "primary":   { "value": "#F5EFE6", "type": "color" },
      "dark":      { "value": "#1C1C1E", "type": "color" },
      "fog":       { "value": "#ECEDEF", "type": "color" },
      "terra":     { "value": "#F0E0D6", "type": "color" }
    },
    "text": {
      "primary":   { "value": "#2C2420", "type": "color" },
      "light":     { "value": "#F0EDE8", "type": "color" },
      "muted":     { "value": "#7A7A7A", "type": "color" }
    },
    "accent": {
      "gold":      { "value": "#C4A882", "type": "color" },
      "sage":      { "value": "#8BA8A0", "type": "color" },
      "terra":     { "value": "#A05030", "type": "color" },
      "blueGray":  { "value": "#A8B5C8", "type": "color" }
    }
  },
  "spacing": {
    "margin-edge":   { "value": "60px",  "type": "spacing" },
    "section-gap":   { "value": "48px",  "type": "spacing" },
    "element-gap":   { "value": "24px",  "type": "spacing" },
    "tight":         { "value": "12px",  "type": "spacing" }
  },
  "typography": {
    "display": { "fontSize": "64", "fontFamily": "Cormorant Garamond", "fontWeight": "700", "lineHeight": "1.1" },
    "heading":  { "fontSize": "42", "fontFamily": "Cormorant Garamond", "fontWeight": "600", "lineHeight": "1.2" },
    "subhead":  { "fontSize": "26", "fontFamily": "DM Sans",            "fontWeight": "400", "lineHeight": "1.4" },
    "body":     { "fontSize": "20", "fontFamily": "DM Sans",            "fontWeight": "300", "lineHeight": "1.6" },
    "caption":  { "fontSize": "14", "fontFamily": "DM Sans",            "fontWeight": "400", "lineHeight": "1.5", "letterSpacing": "0.5" }
  }
}
```

### 3. Criar Estilos Globais no Figma

Instrução para salvar antes de iniciar qualquer frame:

```
ESTILOS DE COR (Color Styles):
→ Painel direito → + em "Local Styles" → Color
Crie:
  Background/Primary  → #F5EFE6
  Background/Dark     → #1C1C1E
  Text/Primary        → #2C2420
  Text/Muted          → #7A7A7A
  Accent/Gold         → #C4A882
  Accent/Sage         → #8BA8A0

ESTILOS DE TEXTO (Text Styles):
→ Selecione texto → Painel direito → + em "Text Styles"
Crie:
  Display   — Cormorant Garamond 700, 64px, LH 1.1
  Heading   — Cormorant Garamond 600, 42px, LH 1.2
  Subhead   — DM Sans 400, 26px, LH 1.4
  Body      — DM Sans 300, 20px, LH 1.6
  Caption   — DM Sans 400, 14px, LH 1.5, LS 0.5
```

### 4. Gerar Especificação Completa do Frame

Produza especificações no seguinte formato:

```
═══════════════════════════════════════════════
ESPECIFICAÇÃO FIGMA — [Nome do Pin/Post]
═══════════════════════════════════════════════

FRAME:
  Nome:    [nome descritivo]
  Tamanho: [largura] × [altura] px
  Fill:    [Color Style: Background/Primary] → #[código]
  Clip content: ON

AUTO LAYOUT (se aplicável):
  Direção:       Vertical
  Padding:       60px (todos os lados)
  Gap:           [px entre elementos]
  Alinhamento:   Center / Space between

── CAMADA 1: ELEMENTO VISUAL ──────────────────
  Tipo:       [Vector / Frame / SVG / Ícone Iconify]
  Plugin:     Iconify → buscar "[termo]" → estilo Phosphor/Feather
  Tamanho:    [px × px]
  Posição:    X: center, Y: [px do topo]
  Fill:       none
  Stroke:     [Color Style: Text/Primary] — 1.5px
  Constraints: Center horizontal, Top

── CAMADA 2: TEXTO PRINCIPAL ──────────────────
  Text Style: Heading (Cormorant Garamond 600, 42px)
  Fill:       [Color Style: Text/Primary]
  Width:      880px (fixo)
  Alignment:  Center
  Auto-height: ON
  Posição:    Abaixo do elemento visual — gap [px]
  Conteúdo:   "[texto exato]"

── CAMADA 3: LINHA DIVISÓRIA ──────────────────
  Tipo:       Rectangle
  Tamanho:    120 × 1 px
  Fill:       [Color Style: Accent/Gold]
  Posição:    Center horizontal — gap 24px abaixo do título

── CAMADA 4: SUBTEXTO ─────────────────────────
  Text Style: Body (DM Sans 300, 20px)
  Fill:       [Color Style: Text/Muted]
  Width:      820px (fixo)
  Alignment:  Center
  Auto-height: ON
  Conteúdo:   "[texto exato]"

── CAMADA 5: RODAPÉ / ASSINATURA ──────────────
  Text Style: Caption
  Fill:       [Color Style: Text/Muted]
  Constraints: Center horizontal, Bottom
  Margin-bottom: 60px
  Conteúdo:   "@[perfil]" ou logo

══ EXPORT ══════════════════════════════════════
  Selecione o Frame → Export → + →
  PNG @ 2x → Export [nome].png
═══════════════════════════════════════════════
```

### 5. Criar Componente Reutilizável (para Carrossel)

Quando o conteúdo tem múltiplos slides:

```
COMPONENTE BASE — PinSlide

1. Crie o primeiro slide conforme especificação
2. Selecione o Frame → Cmd+Alt+K (Mac) / Ctrl+Alt+K (Win)
   → "Create Component"
3. Nomeie: "PinSlide/Base"
4. No painel de propriedades, adicione:
   → Properties → + → Text → "headline" (para trocar o texto)
   → Properties → + → Text → "body"
5. Crie variantes:
   → Botão "+" no painel Component → "Add variant"
   → Variant 1: "Theme=Light"
   → Variant 2: "Theme=Dark" (inverta as cores)

Para usar:
   → Aba Assets → busque "PinSlide"
   → Arraste para o canvas
   → Troque texto pelo painel direito
```

### 6. Checklist de Qualidade Figma

Antes de entregar:
- [ ] Todos os elementos usam Color Styles (não cor avulsa)
- [ ] Todos os textos usam Text Styles
- [ ] Camadas nomeadas de forma descritiva (não "Rectangle 47")
- [ ] Frame com Clip Content ativado
- [ ] Margens mínimas de 60px respeitadas
- [ ] Hierarquia de camadas organizada (topo = elemento mais acima visualmente)
- [ ] Export configurado em 2x para nitidez
- [ ] Contraste texto/fundo: mínimo 4.5:1 (verificar com plugin Contrast)

---

## Estruturas de Layout Figma

### Layout 1 — Texto Central Puro (Auto Layout Vertical)
```
Frame [1000×1500, Fill: Background/Primary]
  └─ Auto Layout Vertical, padding 60px, gap: space-between
       ├─ Spacer (flex grow)
       ├─ Heading Text [Center, 880px wide]
       ├─ Divider [120×1px, Accent/Gold]
       ├─ Body Text [Center, 820px wide]
       ├─ Spacer (flex grow)
       └─ Caption/Signature [Center, Bottom]
```

### Layout 2 — Ícone + Texto (Auto Layout Vertical)
```
Frame [1000×1500, Fill: Background/Primary]
  └─ Auto Layout Vertical, padding 60px, gap 48px
       ├─ Icon Frame [240×240, stroke only]
       ├─ Heading Text [Center]
       ├─ Divider [120×1px]
       ├─ Body Text [Center]
       └─ Caption [Bottom]
```

### Layout 3 — Citação Destacada
```
Frame [1000×1500, Fill: Background/Primary]
  ├─ QuoteMarks ["❝" — Display style, opacity 15%]
  └─ Auto Layout Vertical, Center, padding 80px, gap 32px
       ├─ Quote Text [Italic, Heading style]
       ├─ Divider [80×1px]
       ├─ Attribution ["— Autor", Caption]
       └─ Body Text [smaller, muted]
```

---

## Wrap Up

Após gerar as especificações, confirme:
- Frame criado com dimensão correta
- Tokens/estilos aplicados consistentemente
- Componentes criados para reaproveitamento (se carrossel)
- Instruções de export entregues
- Sugira: sistema de design completo, variantes escuro/claro, kit de templates
