# Nano Store — landing page

Site estático (HTML + CSS + JS leve). Não precisa de build: basta enviar a pasta inteira para a hospedagem
(GitHub Pages, Netlify, Vercel, Cloudflare Pages ou servidor comum).

## O que editar (tudo em `config/store.js`)
- `WHATSAPP_NUMBER` — número do WhatsApp, só dígitos com 55 + DDD (ex.: `5547999999999`). Enquanto estiver vazio,
  os botões abrem o WhatsApp com a mensagem pronta para escolher o contato.
- `address` e `mapsUrl` — endereço já preenchido; o botão "Como chegar" abre o Google Maps pelo endereço.
- `categories` — fotos reais de iPhone, Acessórios e Destaques (substituem os espaços reservados).
- `aboutFacts` — números reais da loja (opcional).
- `texts` — textos editáveis.

## Instagram automático (fotos do perfil)
O Instagram não permite ler o perfil de fora sem autorização do dono. O caminho mais simples é um serviço de feed:

1. Crie uma conta gratuita em **behold.so** e conecte o Instagram da loja (o dono da conta autoriza).
2. Crie um feed e copie o endereço JSON (algo como `https://feeds.behold.so/XXXXXXXX`).
3. Cole em `igFeedUrl` no `config/store.js`.

Pronto: a seção do Instagram passa a mostrar as últimas publicações, cada uma linkando para o post.
Se o endereço estiver vazio ou o serviço falhar, a página mostra 3 fotos da loja já incluídas.

## SEO — antes de publicar
Troque `https://SEU-DOMINIO.com.br` pelo domínio real em: `index.html` (canonical, og:url, og:image, JSON-LD),
`robots.txt` e `sitemap.xml`. Quando o WhatsApp/telefone for confirmado, inclua `telephone` no JSON-LD.
Cadastre a loja no Perfil da Empresa no Google com o mesmo endereço.

## Tipografia
Sora (licença livre, auto-hospedada em `assets/fonts`).
