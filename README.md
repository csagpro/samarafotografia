# Samara Fotografia

Landing page para estúdio de fotografia gestante e newborn.

## Deploy

Este projeto está configurado para deploy automático no Vercel.

### Deploy Rápido

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/seu-usuario/samarafotografia)

### Deploy Manual

1. Clone este repositório
2. Conecte ao Vercel: `vercel`
3. Deploy para produção: `vercel --prod`

## Estrutura

```
samarafotografia/
├── index.html      # Página principal
├── css/
│   └── styles.css  # Estilos
├── js/
│   └── main.js     # Interações
├── images/         # Imagens (adicionar)
└── README.md
```

## Desenvolvimento Local

Abra `index.html` diretamente no navegador ou use um servidor local:

```bash
# Com Python
python -m http.server 8000

# Com Node.js (npx)
npx serve
```

## Customização

### Imagens
Adicione suas imagens em `images/` e atualize os caminhos no HTML.

### Cores
Edite as variáveis CSS em `css/styles.css`:
```css
:root {
    --color-gold: #b8860b;
    --color-gold-light: #cd853f;
    /* ... */
}
```

### Conteúdo
Edite os textos diretamente em `index.html`.

## Integrações Externas

- **Orçamento**: [app.samarafotografia.com.br](https://app.samarafotografia.com.br)
- **Portfolio**: [@samara_rodrigo_photo](https://instagram.com/samara_rodrigo_photo)

## Licença

Uso exclusivo para Samara Fotografia.
