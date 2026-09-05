# Ícones e símbolos paxyOS — 1:1

PNG quadrados (1:1), Space Grotesk Bold, paleta oficial (#5DE391 signal · #A7FFE3 plasma · #000000 void · #232725 steel).
Tamanhos por pasta: 1024 · 512 · 256 · 192 · 180 · 64 · 32 px.

## Pastas

| Pasta | O que é | Onde usar |
|---|---|---|
| `avatar-preto/` | Círculo preto, malha de pontos, "y" verde com glow, borda #232725 | Foto de perfil: Instagram, X, LinkedIn, GitHub, Discord, WhatsApp |
| `avatar-transparente/` | Mesmo avatar sem fundo (1024, 512) | Sobrepor em fundos escuros próprios |
| `app-icon-preto/` | Squircle preto (raio 22.9%, padrão iOS) com "y" verde | App icon iOS/Android, PWA, atalho de desktop |
| `app-icon-verde/` | Squircle verde com "y" preto e degradê plasma | Variante clara, destaque, fundos escuros |
| `marca-1x1-preto/` | Logotipo `paxyOS` completo centrado + linha de energia | Perfil com nome visível, cover, OG image quadrada |
| `marca-1x1-branco/` | Marca em fundo branco, "y" em #0F8A52 (contraste AA) | Impressos, documentos, fundos claros |
| `simbolo-y-verde/` | "y" isolado verde, fundo transparente | Marca d'água, bullet, ícone dentro de UI |
| `simbolo-y-branco/` | "y" isolado branco, transparente | Sobre verde ou fundo colorido |
| `simbolo-y-preto/` | "y" isolado preto, transparente (1024, 512) | Sobre verde/claro, impressão em 1 cor |
| `selo-hud/` | Anel verde com núcleo em glow e marcas de HUD | Selo de status, badge "sistema ativo" |
| `favicon/` | "y" verde sobre preto, sem glow nos pequenos | favicon 16 · 32 · 64 · 180 · 512 |

## Instalação no site (Astro)

Copie `favicon/` e `app-icon-preto/` para `public/icons/` e no `<head>`:

```html
<link rel="icon" type="image/png" sizes="32x32" href="/icons/paxyos-favicon-32.png" />
<link rel="icon" type="image/png" sizes="16x16" href="/icons/paxyos-favicon-16.png" />
<link rel="apple-touch-icon" sizes="180x180" href="/icons/paxyos-app-icon-180.png" />
<link rel="manifest" href="/manifest.webmanifest" />
<meta name="theme-color" content="#000000" />
```

`public/manifest.webmanifest`:
```json
{
  "name": "paxyOS",
  "short_name": "paxyOS",
  "background_color": "#000000",
  "theme_color": "#5DE391",
  "display": "standalone",
  "icons": [
    { "src": "/icons/paxyos-app-icon-192.png", "sizes": "192x192", "type": "image/png" },
    { "src": "/icons/paxyos-app-icon-512.png", "sizes": "512x512", "type": "image/png", "purpose": "any maskable" }
  ]
}
```

## Regras
- O "y" só existe em #5DE391 (fundo escuro), #0F8A52 (fundo claro) ou #000000 (sobre verde).
- Abaixo de 128px o glow é removido — use os arquivos já gerados, não reduza os grandes.
- A área de respiro já está embutida; não adicione padding extra nas plataformas.
