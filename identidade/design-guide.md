# Identidade visual — paxyOS

> Como a marca aparece em tudo que o PaxyOS gera.
> As skills de conteúdo, carrossel e post leem esse arquivo antes de criar qualquer visual.
> Edite quando a marca evoluir.

---

## Cores

- **Fundo principal:** `#000000` — Void. O preto absoluto. Fundo padrão de carrossel, slide e proposta.

- **Cor de destaque / CTA:** `#5DE391` — Green (signal). Verde da marca. Usado no "y", em números, em CTA e em qualquer palavra que precisa puxar o olho. Um destaque por peça, no máximo dois.

- **Texto principal:** `#FFFFFF` — White. Sobre fundo escuro, sempre.

- **Fundo alternativo / cards:** `#0A0C0B` — Carbon · `#141715` — Graphite · `#232725` — Steel (bordas e divisórias).

- **Apoio:** `#A7FFE3` — Plasma Mint (glow, gradiente, brilho de fundo) · `#8A928D` — Ash (texto secundário, legenda, metadado).

- **Cor proibida:** qualquer cor fora dessa paleta. Nada de azul corporativo, roxo de startup, gradiente arco-íris. O verde é a única cor viva da marca — se tudo brilha, nada brilha.

### Paleta completa

| Nome | Hex | Uso |
|---|---|---|
| Void | `#000000` | Fundo principal |
| Carbon | `#0A0C0B` | Fundo de seção |
| Graphite | `#141715` | Cards |
| Steel | `#232725` | Bordas, divisórias |
| Green (signal) | `#5DE391` | Destaque, CTA, o "y" |
| Plasma Mint | `#A7FFE3` | Glow, gradiente, brilho |
| Ash | `#8A928D` | Texto secundário |
| White | `#FFFFFF` | Texto principal |

**Verde em fundo claro:** `#0F8A52` (contraste AA). O `#5DE391` só vive sobre fundo escuro.

---

## Tipografia

- **Títulos e destaques:** Space Grotesk — display da marca. É a fonte do logotipo.

- **Corpo, subtítulos e botões:** Manrope.

- **Técnico / dados / código:** JetBrains Mono. Números, métricas, labels de HUD, trechos de código.

- **Peso do título:** Bold (700). Manrope no corpo em Regular (400) e Medium (500).

```
Space Grotesk  →  https://fonts.google.com/specimen/Space+Grotesk
Manrope        →  https://fonts.google.com/specimen/Manrope
JetBrains Mono →  https://fonts.google.com/specimen/JetBrains+Mono
```

---

## Estilo geral

Escuro, técnico, com respiro. Cara de painel de sistema, não de post motivacional.
Muito preto, pouco elemento, um ponto de verde que guia o olho. A informação
tem hierarquia clara: um título grande, um corpo legível, um dado em mono.
Textura sutil de malha de pontos no fundo quando a peça pede profundidade.
Nada de stock photo sorrindo, nada de fundo branco.

---

## Elementos-chave

- **Bordas:** 1px `#232725`. Discretas — separam sem gritar.
- **Border-radius dos cards:** 16px. App icon usa squircle 22.9% (padrão iOS).
- **Botões:** fundo `#5DE391`, texto `#000000`, radius 12px, Manrope Medium.
- **Sombras:** não usar sombra tradicional. A profundidade vem de glow verde
  (`box-shadow: 0 0 40px rgba(93,227,145,.25)`) e de camadas de cinza.
- **Linha de energia:** régua horizontal fina com gradiente verde que desvanece
  nas pontas — assinatura visual da marca, usar abaixo de títulos-chave.
- **Malha de pontos:** grid de pontos `#232725` a 4-6% de opacidade no fundo.

---

## O que NUNCA fazer

- Usar o "y" em qualquer cor fora de `#5DE391` (fundo escuro), `#0F8A52` (fundo claro) ou `#000000` (sobre verde).
- Reduzir os arquivos grandes na mão — abaixo de 128px o glow some. Use o tamanho já gerado.
- Adicionar padding extra ao redor dos ícones nas plataformas: a área de respiro já está embutida.
- Encher a peça de verde. O verde é acento, não fundo.
- Fundo branco em peça de rede social. A marca vive no escuro.
- Emoji dentro da arte. Emoji, se houver, só na legenda.

---

## Logo

- **Arquivo:** `identidade/logo.png` (marca `paxyOS` completa, 1024×1024, fundo preto)
- **Símbolo isolado:** `identidade/logo-simbolo.png` (o "y" verde, fundo transparente)
- **Versão pra fundo claro:** `identidade/icones/marca-1x1-branco/paxyos-marca-branco-1024.png`
- **Onde usar:** slide final do carrossel (CTA), header de propostas, slides de apresentação
- **Tamanho sugerido:** largura entre 120-200px nos HTMLs

### Kit completo — `identidade/icones/`

| Pasta | O que é | Onde usar |
|---|---|---|
| `avatar-preto/` | Círculo preto, malha de pontos, "y" verde com glow | Foto de perfil: Instagram, X, LinkedIn, GitHub, WhatsApp |
| `avatar-transparente/` | Mesmo avatar sem fundo | Sobrepor em fundos escuros próprios |
| `app-icon-preto/` | Squircle preto com "y" verde | App icon iOS/Android, PWA, atalho de desktop |
| `app-icon-verde/` | Squircle verde com "y" preto e degradê plasma | Variante clara, destaque |
| `marca-1x1-preto/` | Logotipo `paxyOS` completo + linha de energia | Perfil com nome visível, cover, OG image |
| `marca-1x1-branco/` | Marca em fundo branco, "y" em `#0F8A52` | Impressos, documentos, fundos claros |
| `simbolo-y-verde/` | "y" isolado verde, transparente | Marca d'água, bullet, ícone dentro de UI |
| `simbolo-y-branco/` | "y" isolado branco, transparente | Sobre verde ou fundo colorido |
| `simbolo-y-preto/` | "y" isolado preto, transparente | Sobre verde/claro, impressão em 1 cor |
| `selo-hud/` | Anel verde com núcleo em glow e marcas de HUD | Selo de status, badge "sistema ativo" |
| `favicon/` | "y" verde sobre preto | favicon 16 · 32 · 64 · 180 · 512 |

Tamanhos disponíveis por pasta: 1024 · 512 · 256 · 192 · 180 · 64 · 32 px.

---

## Observações adicionais

**CSS base pra qualquer peça gerada:**

```css
:root {
  --void: #000000;
  --carbon: #0A0C0B;
  --graphite: #141715;
  --steel: #232725;
  --green: #5DE391;
  --plasma: #A7FFE3;
  --ash: #8A928D;
  --white: #FFFFFF;
  --display: 'Space Grotesk', system-ui, sans-serif;
  --body: 'Manrope', system-ui, sans-serif;
  --mono: 'JetBrains Mono', monospace;
}
```
