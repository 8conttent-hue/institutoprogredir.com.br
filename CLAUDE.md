# CLAUDE.md — INSTITUTOPROGREDIR

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** INSTITUTOPROGREDIR
**Nicho:** Negócios e Empreendedorismo
**Keywords:** Nossa missao e orientar lideres a fazerem um trabalho eficiente e que
**Paleta de cores:** violet | **Fonte:** montserrat

Nossa missão é orientar líderes a fazerem um trabalho eficiente e que culminem em resultados com seus clientes, liderados e outros líderes. Falamos de princípios de liderança, como construir uma autoridade com o advento da internet, e como utilizar o marketing digital para vender mais e para propiciar maior conhecimento de marca pessoal ou empresarial. Acreditamos piamente que um bom líder deve ser exemplo e deve ser servidor. Em outras palavras, um bom líder deve ser “executador de tarefas” e também um “servidor” dos seus colaboradores. Caso você não seja assim hoje, comece amanhã mesmo a ser e logo repare uma grande mudança na maneira que os outros vão se relacionar com você. Acreditamos que o modo de vender e se relacionar mudou completamente, não tendo mais espaço para amadorismo e para ultrapassados. É imprescindível que se use internet para se relacionar, fazer negócios e conexões. Iremos abordar sobre esses assuntos e muito mais no nosso Blog.



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-G |
| Hero | Hero-J |
| Features | Features-H |
| About Section | About-H |
| Posts | Posts-H |
| Footer | Footer-J |
| Página Sobre | Sobre-D |
| Página Contato | Contato-G |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
