# CBA X — Atividades de Salvamentos Marítimos

Landing page institucional do **Comando de Bombeiros de Área X (CBA X)** — CBMERJ. Conta a história de mais de um século de salvamento marítimo no Rio de Janeiro, mapeia as 10 unidades operacionais do litoral fluminense e apresenta o calendário crítico de eventos do verão, com vídeos reais de formação, prevenção e resgate.

🌐 **Site publicado em:** https://SEU-USUARIO.github.io/cbax-celverdini/

> ⚠️ Substitua `SEU-USUARIO` pelo seu username do GitHub neste README e nos meta tags Open Graph dentro de `index.html` antes de publicar.

---

## Estrutura

```
cbax-celverdini/
├── index.html              Landing page principal
├── 404.html                Página de erro estilizada
├── README.md               Este arquivo
├── .gitignore              Arquivos ignorados pelo Git
├── .nojekyll               Pula processamento Jekyll do GitHub
└── assets/
    ├── img/                27 imagens otimizadas (~3,7 MB)
    └── videos/             8 vídeos otimizados para web (~66 MB)
```

**Tamanho total do repositório:** ~70 MB

---

## Conteúdo

**Parte I — História (1808-2021):** 10 marcos institucionais em parallax cinematográfico — da Casa de Banho do Caju (D. João VI, 1808) até a redenominação do CBA X em 2021.

**Parte II — Geografia operacional:** Mapa interativo Leaflet com tiles de satélite, marcando as **10 unidades** nas coordenadas reais:

| # | Unidade | Coordenadas | Postos |
|---|---|---|---|
| 1 | 1° GMar — Botafogo | -22.9491, -43.1786 | 7 |
| 2 | DBM 1/M — Paquetá | -22.7550, -43.1116 | 2 |
| 3 | DBM 2/M — Piscinão de Ramos | -22.8398, -43.2512 | 5 |
| 4 | 2° GMar — Barra da Tijuca | -23.0151, -43.3040 | 37 |
| 5 | DBM 3/M — Recreio dos Bandeirantes | -23.0231, -43.4581 | 23 |
| 6 | DBM 4/M — Barra de Guaratiba | -23.0663, -43.5686 | 13 |
| 7 | DBM 5/M — Sepetiba | -22.9860, -43.6994 | 3 |
| 8 | CER — Coord. de Embarcações | -23.0064, -43.3077 | naval |
| 9 | 3° GMar — Copacabana | -22.9859, -43.1878 | 29 |
| 10 | 4° GMar — Itaipu | -22.9539, -43.0283 | 35 |

**Total: 154 postos · 100+ km de costa · 107 anos de história**

**Parte III — Eventos críticos do verão:** Dezembro (férias + verão) → Janeiro (réveillon, São Sebastião, Botinho, convergência de 5 eventos) → Fevereiro (Carnaval, grandes shows).

**Lema do GMar:**

> A qualquer hora! Em qualquer tempo! Em qualquer mar!

**Estatísticas 2026 do Estado do RJ:**

- 734.054 prevenções
- 815 crianças perdidas reencontradas
- 10.361 resgates

**Vídeo institucional cinematográfico de 90 segundos** com áudio original mixado.

---

## Como publicar no GitHub Pages

### Opção 1 — Pela interface web do GitHub (mais simples)

1. Acesse https://github.com/new e crie um repositório chamado **`cbax-celverdini`** (público).
2. Clique em **uploading an existing file** e arraste **todos os arquivos desta pasta** (incluindo a pasta `assets/`).
3. Faça commit na branch `main`.
4. Vá em **Settings → Pages**.
5. Em **Source**, selecione **Deploy from a branch** → branch `main` → folder `/ (root)`. Salve.
6. Aguarde 1-2 minutos. A URL aparece no topo: `https://SEU-USUARIO.github.io/cbax-celverdini/`

### Opção 2 — Pelo terminal (Git CLI)

```bash
# Dentro da pasta cbax-celverdini/
git init
git add .
git commit -m "Initial commit: CBA X landing page"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/cbax-celverdini.git
git push -u origin main
```

Depois ative o GitHub Pages em **Settings → Pages**, igual ao passo 4 da Opção 1.

### Opção 3 — GitHub Desktop

1. Baixe o GitHub Desktop em https://desktop.github.com
2. **File → Add Local Repository** → escolha a pasta `cbax-celverdini/`
3. Publish repository (público)
4. Ative GitHub Pages nas configurações do repositório

---

## Antes de publicar (checklist)

- [ ] Editar este README e trocar `SEU-USUARIO` pelo seu username do GitHub
- [ ] No `index.html`, trocar `SEU-USUARIO` nas tags `<link rel="canonical">` e `<meta property="og:*">` (linhas próximas ao topo do `<head>`)
- [ ] Testar localmente abrindo o `index.html` no navegador
- [ ] Verificar que o vídeo do Hero carrega
- [ ] Confirmar que o mapa Leaflet aparece (precisa de internet para carregar tiles do satélite)

### Find & Replace rápido

Em qualquer editor de texto (VSCode, Sublime, etc), faça **Find & Replace** em todos os arquivos:

- Encontrar: `SEU-USUARIO`
- Substituir por: `seu-username-do-github` (em letras minúsculas, sem `@`)

---

## Rodar localmente

Como o site usa CDNs externas (Tailwind, GSAP, Leaflet, fontes Google), abrir o `index.html` direto no Finder funciona se você tiver internet.

Para servir como um servidor HTTP local (mais fiel ao GitHub Pages):

```bash
# Python 3 (já vem instalado no macOS)
cd cbax-celverdini
python3 -m http.server 8000
```

Depois abra http://localhost:8000 no navegador.

---

## Stack técnica

- **HTML5** semântico
- **CSS** custom (paleta CBMERJ: vermelho #C8102E + amarelo #FFCB05 + preto #0A0A0A)
- **Tailwind CSS** via CDN (utility classes)
- **GSAP 3.12** + ScrollTrigger (animações parallax)
- **Leaflet 1.9** + Esri World Imagery (mapa satélite real)
- **Chart.js 4.4** (KPIs)
- Fontes Google: **Bebas Neue**, **Playfair Display**, **Inter**

---

## Performance e SEO

- **Open Graph** completo para preview em WhatsApp, LinkedIn e Facebook
- **Twitter Card** large image
- **Favicon SVG** inline (escudo CBMERJ)
- **Meta description** otimizada
- Imagens em JPEG otimizado (qualidade 82)
- Vídeos em H.264 + AAC, otimizados para web (faststart, max 1080p)
- Carregamento progressivo (poster JPG enquanto o vídeo carrega)

---

## Créditos

**Conteúdo institucional:** CBMERJ — Corpo de Bombeiros Militar do Estado do Rio de Janeiro
**Concepção e desenvolvimento:** Joel Alves — Assessor da CEO Rede Hospital Casa
**Vídeos:** Acervo CBA X · Reportagens autorizadas
**Coordenadas das unidades:** Levantamento operacional CBA X · 2026

---

## Licença

Conteúdo institucional do CBMERJ. Imagens e vídeos são de uso restrito do Corpo de Bombeiros do Estado do Rio de Janeiro. O código HTML/CSS/JS pode ser reutilizado livremente.

---

*Última atualização: 2026*
