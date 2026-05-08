# Briefing compartilhado — Blog Renata Ventura

> Você é um redator escrevendo um único post de blog para Renata Ventura. Leia este briefing inteiro antes de produzir o arquivo.

## Quem é a Renata
Engenheira de Produção (PUCRS), Auditora Líder ISO 9001, com 15+ anos liderando operações em Globo, Tim, Intelig, Oi Telecom e Instituto Gastronômico das Américas (IGA Brasil). Hoje é consultora de gestão administrativa e financeira para **consultórios, clínicas, escritórios profissionais (arquitetura, advocacia, contabilidade), comércio especializado e profissionais liberais**. Base no Rio de Janeiro, atende Brasil.

## Objetivo do blog
Capturar tráfego orgânico de pessoas pesquisando no Google sobre "como organizar finanças", "fluxo de caixa", "separar contas pessoais", etc. Cada post precisa:
- Ranquear bem para sua keyword principal
- Resolver dor real (não ser conteúdo raso)
- Levar o leitor para o CTA final (conversa via Cal.com)

## Voz e estilo

**FAZER:**
- Português brasileiro profissional, sóbrio, direto. Frases curtas (2-4 por parágrafo).
- Trazer dados reais com fonte (SEBRAE, IBGE, Receita Federal, Ceape Brasil, Conselho Federal de Odontologia, etc).
- Exemplos concretos com números (ex: "uma clínica que fatura R$ 80 mil/mês mas tem só R$ 2 mil de lucro real").
- Linguagem de quem viu muito negócio quebrar — segura, sem precisar gritar.
- Conectar com a história da Renata quando relevante (ex: "Em 15 anos coordenando operações na Globo e na Tim, vi esse mesmo erro em mesas de reunião com cifras milionárias.").

**NÃO FAZER:**
- Nada motivacional. Nada de "vamos juntos!", "olá, empreendedor!", "imagine só…", "spoiler:".
- Sem emojis. Sem clickbait. Sem listas genéricas tipo "10 dicas para…".
- Não citar concorrentes específicos pelo nome.
- Não usar "Imagine X" como recurso retórico mais de uma vez no texto.
- Não usar "vamos descobrir", "neste artigo você vai aprender", e outras fórmulas SEO antigas.
- Sem CTAs no meio do texto ("agende uma reunião!"). O CTA é só no fim, dentro do `.article-cta`.

## Tamanho
**1.300 a 1.700 palavras** no corpo (sem contar nav/footer).

## Estrutura obrigatória (no corpo)
1. **Lead** (`.article-lead`): 2 frases que prendem e prometem o que vem.
2. **Abertura** (sem H2): 2-3 parágrafos contextualizando a dor com um dado concreto.
3. **4 a 6 seções com H2** cobrindo o tema com profundidade.
4. **Pelo menos 1 bloco `.callout`** com um número de impacto + fonte.
5. **Fechamento** (sem H2): 1-2 parágrafos sintetizando.
6. **`.article-cta`**: bloco de chamada para conversa com a Renata.

## SEO obrigatório
- `<title>`: `[Título] | Renata Ventura` (máx 60 caracteres se possível)
- `<meta name="description">`: 150-160 caracteres, com keyword principal naturalmente
- `<link rel="canonical">`
- Open Graph completo + Twitter Card
- JSON-LD `Article` schema
- Keyword principal aparece no: `<title>`, meta description, H1, primeiro parágrafo (primeiras 100 palavras), pelo menos 1 H2

## Template HTML completo (use como base, preencha e ajuste o corpo)

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>{TÍTULO} | Renata Ventura</title>
<meta name="description" content="{DESCRIPTION 150-160 chars com keyword}">
<meta name="author" content="Renata Ventura">
<meta name="robots" content="index, follow, max-image-preview:large">
<link rel="canonical" href="https://renatanventura.com.br/blog/{SLUG}.html">

<meta property="og:title" content="{TÍTULO}">
<meta property="og:description" content="{DESCRIPTION}">
<meta property="og:type" content="article">
<meta property="og:url" content="https://renatanventura.com.br/blog/{SLUG}.html">
<meta property="og:image" content="https://renatanventura.com.br/renata.jpg">
<meta property="og:locale" content="pt_BR">
<meta property="og:site_name" content="Renata Ventura">
<meta property="article:author" content="Renata Ventura">
<meta property="article:published_time" content="2026-05-08T09:00:00-03:00">

<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="{TÍTULO}">
<meta name="twitter:description" content="{DESCRIPTION}">
<meta name="twitter:image" content="https://renatanventura.com.br/renata.jpg">

<link rel="icon" href="/renata.jpg" type="image/jpeg">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="/blog/blog.css">

<script>
(function (C, A, L) { let p = function (a, ar) { a.q.push(ar); }; let d = C.document; C.Cal = C.Cal || function () { let cal = C.Cal; let ar = arguments; if (!cal.loaded) { cal.ns = {}; cal.q = cal.q || []; d.head.appendChild(d.createElement("script")).src = A; cal.loaded = true; } if (ar[0] === L) { const api = function () { p(api, arguments); }; const namespace = ar[1]; api.q = api.q || []; if(typeof namespace === "string"){cal.ns[namespace] = cal.ns[namespace] || api;p(cal.ns[namespace], ar);p(cal, ["initNamespace", namespace]);} else p(cal, ar); return;} p(cal, ar); }; })(window, "https://app.cal.com/embed/embed.js", "Cal");
Cal("init", {origin: "https://app.cal.com"});
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "{TÍTULO}",
  "description": "{DESCRIPTION}",
  "image": "https://renatanventura.com.br/renata.jpg",
  "author": {
    "@type": "Person",
    "name": "Renata Ventura",
    "url": "https://renatanventura.com.br/"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Renata Ventura",
    "logo": {
      "@type": "ImageObject",
      "url": "https://renatanventura.com.br/renata.jpg"
    }
  },
  "datePublished": "2026-05-08",
  "dateModified": "2026-05-08",
  "mainEntityOfPage": "https://renatanventura.com.br/blog/{SLUG}.html",
  "keywords": "{KEYWORDS — separar por vírgula}"
}
</script>
</head>
<body>

<nav class="nav">
  <div class="nav-inner">
    <a href="/" class="nav-brand">Renata Ventura<span class="dot">.</span></a>
    <ul class="nav-links">
      <li><a href="/blog/">Blog</a></li>
      <li><a href="/#sobre">Sobre</a></li>
      <li><a href="/#servicos">Serviços</a></li>
      <li><button data-cal-link="renata-ventura-a87qj8" data-cal-config='{"layout":"month_view"}' class="nav-cta">Conversa de 20 min</button></li>
    </ul>
  </div>
</nav>

<article class="article">
  <div class="article-eyebrow">{CATEGORIA}</div>
  <h1 class="article-title">{H1 — pode usar <em>palavra</em> para itálico em destaque}</h1>
  <div class="article-meta">
    <span class="article-meta-author">Renata Ventura</span>
    <span class="article-meta-dot">·</span>
    <span>{LEITURA} min de leitura</span>
    <span class="article-meta-dot">·</span>
    <span>8 de maio de 2026</span>
  </div>
  <p class="article-lead">{LEAD — 2 frases impactantes}</p>

  <div class="article-body">
    <!-- 2-3 parágrafos de abertura sem H2 -->
    <p>...</p>

    <!-- Pelo menos 1 callout em algum lugar do corpo -->
    <div class="callout">
      <div class="callout-num">{NÚMERO ex: 75%}</div>
      <div class="callout-text">{frase impactante com o dado}</div>
      <div class="callout-source">Fonte: {SEBRAE / IBGE / etc}</div>
    </div>

    <!-- 4-6 seções com H2 -->
    <h2>{H2 — pode usar <em>palavra</em> em destaque}</h2>
    <p>...</p>

    <!-- Use <h3>, <ul>, <ol>, <blockquote>, <table> conforme fizer sentido -->

    <!-- Fechamento sem H2 -->
    <p>...</p>
  </div>

  <div class="article-cta">
    <div class="article-cta-eyebrow">Próximo passo</div>
    <h3>Quer um <em>raio-X</em> da gestão do seu negócio?</h3>
    <p>20 minutos, sem compromisso. Você sai com clareza sobre o que pode ser organizado e por onde faz sentido começar — mesmo que decida fazer sozinho depois.</p>
    <button data-cal-link="renata-ventura-a87qj8" data-cal-config='{"layout":"month_view"}' class="btn-primary">Conversar com a Renata <span class="arrow">→</span></button>
  </div>
</article>

<footer class="footer">
  <div class="footer-brand">Renata Ventura<span class="dot">.</span></div>
  <p>Gestão administrativa &amp; financeira para pequenos negócios.</p>
  <p style="margin-top: 12px;">
    <a href="mailto:venturanrenata@gmail.com">venturanrenata@gmail.com</a>
    &nbsp;·&nbsp;
    <a href="https://linkedin.com/in/renata-ventura-9620a731" target="_blank" rel="noopener">LinkedIn</a>
    &nbsp;·&nbsp;
    <a href="/blog/">Mais posts</a>
  </p>
</footer>

</body>
</html>
```

## Dados confiáveis para citar (use à vontade quando couber)

- **75%** dos empreendedores brasileiros têm dificuldade com fluxo de caixa (Ceape Brasil, 2024)
- **62%** misturam contas pessoais com as da empresa (Ceape Brasil, 2024)
- **58%** não têm orçamento estruturado (Ceape Brasil, 2024)
- **60%** das micro e pequenas empresas fecham antes de 5 anos (IBGE / SEBRAE)
- **MEI** = teto R$ 81 mil/ano = ~R$ 6,7k/mês (Receita Federal)
- **ME** = até R$ 360 mil/ano; **EPP** = R$ 360k a R$ 4,8 milhões/ano
- **RJ 2025**: 425 mil novos pequenos negócios; setores que mais cresceram: Logística (17,6%), Saúde (13,3%), Alimentação (10,2%), Construção (7,9%) (SEBRAE-RJ)
- **SC 2025**: +21,3% em aberturas; serviços lideram com 62,7%; Floripa = Capital Nacional das Startups (SEBRAE-SC)
- **78%** dos pequenos empresários trabalham mais de 50h por semana (Fundação Dom Cabral)
- **Comércio** lidera mortalidade (30,2% fecham em 5 anos) (SEBRAE)
- **Brasil** tem ~441 mil dentistas registrados (CFO 2025) — uma das maiores densidades do mundo

## Lembretes finais
- Inclua a **keyword principal** no H1, na meta description, no primeiro parágrafo (primeiras 100 palavras), e em pelo menos 1 H2.
- Use **palavras-chave secundárias** ao longo do texto naturalmente.
- O CTA final deve estar dentro de `.article-cta` — só esse, no fim do post.
- **Não** invente depoimentos. **Não** insira imagens (não temos assets).
- Salve o arquivo no caminho exato fornecido.
- Não retorne resumo — apenas crie o arquivo.
