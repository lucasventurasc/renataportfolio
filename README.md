# Renata Ventura — Site & Portfólio

Site institucional e portfólio em PDF para serviços administrativos e financeiros.

## Estrutura

- `index.html` — site (single-page, estático)
- `portfolio.html` — fonte do portfólio em PDF
- `portfolio.pdf` — portfólio gerado (6 páginas, A4)

## Deploy (Cloudflare Pages)

Site estático — sem build step. Cloudflare Pages serve o `index.html` direto.

**Configuração no Cloudflare Pages:**
- Build command: *(vazio)*
- Build output directory: `/`
- Root directory: `/`

## Atualizar o portfólio em PDF

```sh
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --no-pdf-header-footer --no-margins \
  --print-to-pdf=portfolio.pdf \
  "file://$(pwd)/portfolio.html"
```

## Integrações

- **Cal.com** — link `renata-ventura` configurado nos botões via `data-cal-link`. Inicialização no `<head>` do `index.html`.
- **WhatsApp** — número codificado nos botões `wa.me/5521993003365`
- **E-mail** — `rnventura@hotmail.com`
- **Lead magnet** — formulário do checklist envia via `mailto:` (trocar por Mailchimp/ConvertKit em produção)
