# 🚀 rafaelroot.com - Redesign com Astro

[![Astro](https://img.shields.io/badge/Astro-FF5D01?style=flat-square&logo=astro)](https://astro.build)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js)](https://nodejs.org)
[![SEO Optimized](https://img.shields.io/badge/SEO%20Optimized-4CAF50?style=flat-square)](https://developers.google.com/search/docs)
[![Mobile First](https://img.shields.io/badge/Mobile%20First-FF6B6B?style=flat-square)](https://developers.google.com/search/mobile-first)

## 📌 Sobre o Projeto

**rafaelroot.com** é um repositório que documenta a jornada de um **Fullstack Developer & Security Specialist** com 22+ anos de experiência. O site é um laboratório vivo de **otimizações SEO, performance web e segurança**, mostrando casos reais de crescimento de zero indexação para primeira página do Google.

### Objetivos do Redesign v2.0

- ✅ **Migração para Astro**: Framework moderno com SSG/SSR otimizado para performance
- ✅ **Node.js Backend**: APIs otimizadas para processamento de dados
- ✅ **SEO Enterprise**: Otimização completa para Google, Bing, DuckDuckGo e buscadores globais
- ✅ **Mobile-First**: Responsive design com performance máxima em mobile
- ✅ **Nginx Optimization**: Compressão, cache headers e rewrite rules
- ✅ **Web Vitals**: Core Web Vitals otimizados (LCP, FID, CLS)
- ✅ **Reindexação Global**: Structured Data, sitemaps multilíngues, hreflang tags

---

## 🏗️ Arquitetura

```
rafaelroot.com/
├── src/
│   ├── pages/              # Rotas Astro (SSG/SSR)
│   ├── components/         # Componentes Astro/React
│   ├── layouts/            # Layouts reutilizáveis
│   ├── content/            # CMS Astro Content Collections
│   ├── styles/             # CSS/SCSS otimizado
│   ├── utils/              # Helpers e utilidades
│   └── api/                # Endpoints Node.js (SSR)
├── public/
│   ├── sitemap.xml         # XML Sitemap principal
│   ├── sitemap-pt.xml      # Sitemap português
│   ├── sitemap-es.xml      # Sitemap espanhol
│   ├── robots.txt          # Instruções para crawlers
│   ├── security.txt        # Security.txt (RFC 9110)
│   └── .well-known/        # Security headers
├── server/                 # Node.js custom server
│   ├── middleware/         # Auth, logging, compression
│   ├── routes/             # API routes
│   └── cache/              # Redis/caching layer
├── nginx/                  # Configurações Nginx
│   ├── nginx.conf          # Config principal
│   ├── security.conf       # Headers de segurança
│   ├── compression.conf    # Gzip/Brotli config
│   └── cache.conf          # Cache directives
├── astro.config.ts         # Configuração Astro
├── tsconfig.json           # TypeScript config
└── package.json            # Dependencies
```

---

## 🎯 Stack Tecnológico

### Frontend
- **[Astro 4.x](https://astro.build)** - SSG/SSR framework otimizado
- **[TypeScript](https://www.typescriptlang.org)** - Type safety
- **[React 18](https://react.dev)** - Componentes interativos (UI islands)
- **[TailwindCSS 4](https://tailwindcss.com)** - Styling atomic
- **[Astro Image](https://docs.astro.build/en/guides/images)** - Otimização de imagens
- **[Sharp](https://sharp.pixelplumbing.com)** - Processamento de imagens WebP/AVIF

### Backend
- **[Node.js 22+](https://nodejs.org)** - Runtime JavaScript server-side
- **[Express.js](https://expressjs.com)** ou **[Fastify](https://www.fastify.io)** - Web framework
- **[Redis](https://redis.io)** - Cache e sessões
- **[Prisma](https://www.prisma.io)** - ORM para BD (opcional)

### Infraestrutura
- **[Nginx 1.27+](https://nginx.org)** - Reverse proxy & web server
- **[Docker](https://www.docker.com)** - Containerização
- **[GitHub Actions](https://github.com/features/actions)** - CI/CD

---

## 🔍 SEO - Otimizações Implementadas

### 1. **Structured Data (Schema.org)**
```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Rafael Cavalcanti da Silva",
  "title": "Fullstack Developer & Security Specialist",
  "url": "https://rafaelroot.com",
  "sameAs": [
    "https://github.com/ai-rafaelroot",
    "https://dev.to/rafaelroot"
  ]
}
```

### 2. **Meta Tags & Open Graph**
- ✅ Meta descriptions dinâmicas por página
- ✅ Open Graph tags (og:title, og:image, og:type)
- ✅ Twitter Card tags (@username)
- ✅ Canonical tags para evitar duplicate content
- ✅ Hreflang tags para versões multilíngues (pt-BR, es-ES, en-US)

### 3. **Sitemaps Multilíngues**
```xml
<!-- sitemap.xml -->
<?xml version="1.0" encoding="UTF-8"?>
<sitemapindex xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
              xmlns:xhtml="http://www.w3.org/1999/xhtml">
  <sitemap>
    <loc>https://rafaelroot.com/sitemap-pt.xml</loc>
  </sitemap>
  <sitemap>
    <loc>https://rafaelroot.com/sitemap-es.xml</loc>
  </sitemap>
  <sitemap>
    <loc>https://rafaelroot.com/sitemap-en.xml</loc>
  </sitemap>
</sitemapindex>
```

### 4. **Robots.txt Otimizado**
```
User-agent: *
Allow: /
Allow: /sitemap*.xml
Disallow: /admin/
Disallow: /private/

Sitemap: https://rafaelroot.com/sitemap.xml
Crawl-delay: 1

# Google-specific
User-agent: Googlebot
Allow: /

# Bing
User-agent: Bingbot
Allow: /
```

### 5. **Core Web Vitals**
- **LCP (Largest Contentful Paint)** < 2.5s
  - Lazy loading de imagens
  - Preloading de recursos críticos
  - Font-display: swap para Web Fonts
  
- **FID → INP (Interaction to Next Paint)** < 200ms
  - Code splitting com Astro
  - Event delegation otimizada
  - Zero layout shifts
  
- **CLS (Cumulative Layout Shift)** < 0.1
  - Fixed width/height em imagens
  - Font size-adjust em Web Fonts
  - Avoidance de dynamic content injection

---

## ⚡ Performance - Otimizações Nginx

### 1. **Compressão Brotli + Gzip**
```nginx
# nginx/compression.conf
gzip on;
gzip_vary on;
gzip_min_length 1024;
gzip_types text/plain text/css text/xml text/javascript 
           application/x-javascript application/xml+rss 
           application/json application/javascript;
gzip_comp_level 6;

brotli on;
brotli_comp_level 4;
brotli_types text/plain text/css text/xml text/javascript 
             application/x-javascript application/xml+rss 
             application/json application/javascript;
```

### 2. **HTTP/2 Push & Preload**
```nginx
location / {
  http2_push_preload on;
  add_header Link "</css/main.css>; rel=preload; as=style" always;
  add_header Link "</fonts/inter.woff2>; rel=preload; as=font; type=font/woff2; crossorigin" always;
}
```

### 3. **Caching Inteligente**
```nginx
# nginx/cache.conf
# Cache estático por 1 ano
location ~* \.(jpg|jpeg|png|gif|ico|css|js|svg|woff|woff2)$ {
  expires 365d;
  add_header Cache-Control "public, immutable";
  etag off;
}

# Cache HTML por 5 minutos (revalidação)
location ~* \.html$ {
  expires 5m;
  add_header Cache-Control "public, must-revalidate";
}

# Sem cache para API
location /api/ {
  expires -1;
  add_header Cache-Control "no-store, no-cache, must-revalidate";
}
```

### 4. **Headers de Segurança & SEO**
```nginx
# nginx/security.conf
add_header Strict-Transport-Security "max-age=31536000; includeSubDomains" always;
add_header X-Content-Type-Options "nosniff" always;
add_header X-Frame-Options "DENY" always;
add_header X-XSS-Protection "1; mode=block" always;
add_header Referrer-Policy "strict-origin-when-cross-origin" always;
add_header Permissions-Policy "geolocation=(), microphone=(), camera=()" always;

# Preconnect para recursos externos
add_header Link "</dns-prefetch>; rel=dns-prefetch" always;
```

### 5. **Rewrite Rules para URLs Limpas**
```nginx
# Remove index.html
location / {
  try_files $uri $uri/ @missing;
}

location @missing {
  rewrite ^/(.*)$ /index.html last;
}

# WWW canonicalization
server {
  server_name rafaelroot.com;
  return 301 https://www.rafaelroot.com$request_uri;
}
```

---

## 🌍 Reindexação Global

### 1. **Google Search Console Integration**
```javascript
// src/api/indexing.ts - Google Indexing API
import { google } from 'googleapis';

async function notifyGoogleIndexing(url: string) {
  const indexing = google.indexing({
    version: 'v3',
    auth: new google.auth.GoogleAuth({
      keyFile: process.env.GOOGLE_SERVICE_ACCOUNT_KEY,
      scopes: ['https://www.googleapis.com/auth/indexing'],
    }),
  });

  await indexing.urlNotifications.publish({
    requestBody: {
      url,
      type: 'URL_UPDATED',
    },
  });
}
```

### 2. **Bing Webmaster Tools**
```xml
<!-- public/BingSiteAuth.xml -->
<?xml version="1.0"?>
<users>
    <user>your-bing-verification-code</user>
</users>
```

### 3. **Hreflang Alternates (Multilíngue)**
```html
<!-- pt-BR -->
<link rel="alternate" hreflang="pt-BR" href="https://rafaelroot.com/pt/" />

<!-- es-ES -->
<link rel="alternate" hreflang="es-ES" href="https://rafaelroot.com/es/" />

<!-- en-US (default/fallback) -->
<link rel="alternate" hreflang="en-US" href="https://rafaelroot.com/en/" />
<link rel="alternate" hreflang="x-default" href="https://rafaelroot.com/" />
```

### 4. **Feed RSS para Buscadores**
```xml
<!-- public/feed.xml -->
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0" xmlns:content="http://purl.org/rss/1.0/modules/content/">
  <channel>
    <title>Rafael Cavalcanti - Blog</title>
    <link>https://rafaelroot.com</link>
    <description>SEO, Performance & Security Articles</description>
    <!-- Items gerados dinamicamente -->
  </channel>
</rss>
```

---

## 📱 Mobile-First Optimization

### 1. **Viewport Meta Tag**
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
```

### 2. **Responsive Images com Astro**
```astro
---
import { Image } from 'astro:assets';
import mainImage from '../assets/hero.jpg';
---

<Image 
  src={mainImage}
  alt="Hero section"
  widths={[200, 400, 800]}
  sizes="(max-width: 640px) 100vw, (max-width: 1024px) 50vw, 33vw"
  format="webp"
/>
```

### 3. **Fluid Typography**
```css
/* TailwindCSS com responsive sizing */
h1 {
  font-size: clamp(1.5rem, 5vw, 3rem);
  line-height: 1.2;
}

p {
  font-size: clamp(1rem, 2vw, 1.125rem);
  line-height: 1.6;
}
```

### 4. **Touch-Friendly Interactions**
```css
/* Minimum 48px touch target */
button, a[role="button"] {
  min-height: 48px;
  min-width: 48px;
  padding: 12px 16px;
}

/* Active states para mobile */
@media (hover: none) {
  button:active {
    background: var(--color-active);
  }
}
```

---

## 🚀 Como Começar

### Instalação
```bash
# Clone o repositório
git clone https://github.com/ai-rafaelroot/rafaelroot.com.git
cd rafaelroot.com

# Instale as dependências
npm install

# Configure variáveis de ambiente
cp .env.example .env.local

# Inicie o servidor de desenvolvimento
npm run dev

# Build para produção
npm run build

# Preview da build
npm run preview
```

### Variáveis de Ambiente
```env
# .env.local
PUBLIC_SITE_URL=https://rafaelroot.com
PUBLIC_ANALYTICS_ID=G-XXXXXXXXXX

# Google Indexing API
GOOGLE_SERVICE_ACCOUNT_KEY=path/to/service-account.json

# Bing Webmaster
BING_WEBMASTER_API_KEY=your-key

# Database (opcional)
DATABASE_URL=postgresql://user:pass@localhost/rafaelroot

# Redis (cache)
REDIS_URL=redis://localhost:6379

# Node.js
NODE_ENV=production
```

---

## 📊 Métricas & Monitoramento

### Google Analytics 4
```astro
---
// src/components/Analytics.astro
const analyticsId = import.meta.env.PUBLIC_ANALYTICS_ID;
---

<script async src={`https://www.googletagmanager.com/gtag/js?id=${analyticsId}`}></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', '{analyticsId}');
</script>
```

### Core Web Vitals Tracking
```typescript
// src/utils/vitals.ts
export function trackWebVitals() {
  // LCP
  const perfObserver = new PerformanceObserver((list) => {
    const entries = list.getEntries();
    entries.forEach((entry) => {
      console.log('LCP:', entry.renderTime || entry.loadTime);
    });
  });
  perfObserver.observe({ entryTypes: ['largest-contentful-paint'] });
}
```

---

## 🔒 Segurança

### Implementações
- ✅ HTTPS/TLS 1.3 obrigatório
- ✅ HSTS (HTTP Strict Transport Security)
- ✅ CSP (Content Security Policy)
- ✅ CORS properly configured
- ✅ Rate limiting em APIs
- ✅ Input validation & sanitization
- ✅ Security.txt (RFC 9110)
- ✅ Regular dependency updates

```nginx
# Exemplos em nginx/security.conf
add_header Content-Security-Policy "default-src 'self'; script-src 'self' 'unsafe-inline' *.googletagmanager.com; style-src 'self' 'unsafe-inline';" always;
```

---

## 📝 Desenvolvimento

### Scripts Disponíveis
```json
{
  "dev": "astro dev",
  "build": "astro build",
  "preview": "astro preview",
  "lint": "eslint src/ --fix",
  "type-check": "tsc --noEmit",
  "test": "vitest",
  "sitemap": "node scripts/generate-sitemap.js",
  "optimize-images": "sharp -i src/assets -o public/images"
}
```

### Testing
```bash
npm run test        # Unit tests
npm run lint        # ESLint + Prettier
npm run type-check  # TypeScript check
```

---

## 🤝 Contribuindo

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/amazing-feature`)
3. Commit suas mudanças (`git commit -m 'Add amazing feature'`)
4. Push para a branch (`git push origin feature/amazing-feature`)
5. Abra um Pull Request

---

## 📄 Licença

Este projeto está sob a licença [MIT](LICENSE).

---

## 📚 Recursos & Referências

- [Astro Documentation](https://docs.astro.build)
- [Google Search Central](https://developers.google.com/search)
- [Web.dev - Performance](https://web.dev/performance)
- [MDN Web Docs](https://developer.mozilla.org)
- [Nginx Documentation](https://nginx.org/en/docs)
- [Schema.org](https://schema.org)

---

## 👨‍💻 Autor

**Rafael Cavalcanti da Silva**
- 🌐 [rafaelroot.com](https://rafaelroot.com)
- 🐙 [GitHub](https://github.com/ai-rafaelroot)
- 📝 [DEV Community](https://dev.to/rafaelroot)
- 🔗 [Founder: xpusher.net](https://xpusher.net)

---

## 📞 Contato & Suporte

Para dúvidas, sugestões ou reportar bugs:
- Abra uma [Issue](https://github.com/ai-rafaelroot/rafaelroot.com/issues)
- Visite [rafaelroot.com](https://rafaelroot.com)

---

**Última atualização**: Junho 2026 | **Status**: Em Desenvolvimento 🚀
