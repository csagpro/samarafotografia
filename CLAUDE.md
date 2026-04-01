# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Projeto

Landing page estática para estúdio de fotografia gestante e newborn (Sinop/MT). Deploy no Vercel via `@vercel/static`.

## Desenvolvimento Local

```bash
# Python (sem dependências)
python -m http.server 8000

# Node.js
npx serve
```

Não há build step, bundler, package.json, nem framework. Edite os arquivos diretamente.

## Deploy

Deploy automático no Vercel via push para `master`. Para deploy manual:

```bash
vercel --prod
```

## Arquitetura

Site de página única (`index.html`) com seções: hero, sobre, galeria/portfólio, depoimentos, contato.

**Arquivos principais:**
- `index.html` — toda a estrutura HTML e conteúdo de texto
- `css/styles.css` — estilos com design tokens em `:root`
- `js/main.js` — interações vanilla JS (nav mobile, scroll suave, reveal por IntersectionObserver, contadores animados)
- `vercel.json` — config de deploy e headers de cache/segurança

**Design tokens (CSS variables em `:root`):**
- Paleta: `--bg`, `--cream`, `--gold`, `--dark`, `--text`, `--muted`
- Tipografia: `--font-display` (Cormorant Garamond) + `--font-body` (Jost)
- Sombras: `--shadow-sm/md/lg`; Transições: `--transition`, `--transition-slow`

**Animações JS:**
- `.reveal` — elementos ganham classe `.visible` ao entrar no viewport (IntersectionObserver)
- `.numero-item[data-target]` — counters animados com ease-out cúbico e stagger de 200ms

## Integrações Externas

- **Orçamento**: `https://app.samarafotografia.com.br` (link externo, sem integração de backend)
- **Instagram/Portfólio**: `@samara_rodrigo_photo`
- **Logo**: carregada de `samarafotografia.com.br` com fallback para texto se falhar
- **Fontes**: Google Fonts (Cormorant Garamond + Jost)
