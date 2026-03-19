# ◈ AutoPortfolio

> Gere um portfólio profissional completo em minutos — sem servidor, sem npm, sem configuração.



## ✨ O que é

**AutoPortfolio** é uma ferramenta web que gera portfólios de desenvolvedor automaticamente. Você preenche um formulário, visualiza em tempo real e exporta um arquivo HTML único — pronto para hospedar no GitHub Pages, Netlify ou qualquer outro lugar.

Projeto pessoal construído inteiramente no navegador, sem dependências externas de servidor.

---

## 🚀 Demo

**[→ Abrir AutoPortfolio](https://jottaramoss.github.io/AutoPortfolio/)**

---

## 🎯 Funcionalidades

### Formulário completo
- **Perfil** — nome, título, tagline, bio, localização, anos de experiência, disponibilidade
- **Foto** — upload de arquivo ou URL, com 4 formatos (círculo, quadrado, hexágono, blob)
- **Tecnologias** — 50+ techs com ícones, busca inteligente, adição por clique
- **Habilidades** — barras de progresso com slider interativo
- **Projetos** — nome, categoria, descrição, link, repositório, imagem, tags, destaque — com drag & drop para reordenar
- **Experiência** — cargo, empresa, datas, descrição e logo
- **Educação** — curso, instituição e período
- **Certificados** — nome, emissor, ano e link de verificação
- **Serviços** — o que você oferece, com emoji e descrição
- **15 redes sociais** com ícones SVG — GitHub, LinkedIn, Twitter/X, Instagram, YouTube, Discord, Twitch, Telegram, WhatsApp, Behance, Dribbble, Medium, Dev.to, Website, E-mail

### Customização visual
- **5 templates** — Minimalista, Dark Studio, Cyberpunk, Criativo, Glassmorphism
- **10 cores de destaque** predefinidas + seletor de cor livre
- **6 famílias tipográficas** — DM Sans, Syne, Playfair Display, Space Mono, Poppins, Cabinet Grotesk
- **3 layouts de hero** — Lado a Lado, Centralizado, Banner
- **Estilo dos botões sociais** — Ícone + Texto / Só Ícone / Só Texto × Arredondado / Pílula / Quadrado
- **CSS personalizado** injetado diretamente no portfólio exportado
- **Seções togláveis** — ative ou desative qualquer seção com um clique

### Preview & Exportação
- Preview ao vivo com atualização em tempo real
- Modo mobile (390px, estilo iPhone)
- Modo fullscreen
- Exportação como arquivo `.html` único
- Cópia do código via clipboard
- SEO completo — meta description, keywords, idioma (PT/EN/ES/FR/DE)
- AutoSave via LocalStorage

---

## 🛠️ Construído com

![React](https://img.shields.io/badge/React-18.2-61dafb?style=for-the-badge&logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-f7df1e?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Babel](https://img.shields.io/badge/Babel-7.23-f9dc3e?style=for-the-badge&logo=babel&logoColor=black)
![Google Fonts](https://img.shields.io/badge/Google_Fonts-4285F4?style=for-the-badge&logo=google&logoColor=white)
![No Build](https://img.shields.io/badge/No_Build-✓-c8f135?style=for-the-badge)
![No Backend](https://img.shields.io/badge/No_Backend-✓-c8f135?style=for-the-badge)
![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-Ready-222?style=for-the-badge&logo=github&logoColor=white)


### Editor (a ferramenta em si)

| Tecnologia | Versão | Uso |
|---|---|---|
| [React](https://react.dev) | 18.2 | Interface do editor — componentes, estado, hooks |
| [Babel Standalone](https://babeljs.io) | 7.23 | Transpila JSX diretamente no browser, sem build |
| [Google Fonts](https://fonts.google.com) | — | Syne, DM Sans, Space Mono, Playfair Display, Poppins, Cabinet Grotesk |
| CSS puro | — | Layout, animações, dark theme do editor |
| LocalStorage API | — | Persistência automática do rascunho entre sessões |

### Portfólio gerado (o arquivo exportado)

| Tecnologia | Uso |
|---|---|
| HTML5 semântico | Estrutura de todas as seções |
| CSS inline | Estilização isolada, sem conflito externo |
| Google Fonts (CDN) | Tipografias carregadas no portfólio final |
| SVG inline | Ícones das redes sociais sem dependência de biblioteca |
| Vanilla JS puro | Nenhum framework no arquivo exportado |

### Conceitos e padrões aplicados

- **Component-based UI** com React functional components e hooks (`useState`, `useEffect`, `useCallback`, `useMemo`, `useRef`)
- **Debounce** no preview para evitar rerenders excessivos durante digitação
- **Geração de HTML via string** — o portfólio é montado como template literal e injetado em um `<iframe>` em tempo real
- **Drag & drop nativo** da Web API para reordenar projetos e experiências
- **FileReader API** para upload e preview de imagem local sem servidor
- **Clipboard API** para copiar o código gerado
- **Blob + URL.createObjectURL** para download do arquivo HTML sem backend

> **Zero dependências de servidor.** Nenhum npm, nenhum build, nenhum backend. Um arquivo HTML de ~100KB que abre direto no navegador.

---

## 📦 Como usar

### Opção 1 — Direto pelo browser
Baixe o arquivo e abra no navegador:

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/autoportfolio.git

# Entre na pasta
cd autoportfolio

# Abra o arquivo
open index.html       # macOS
start index.html      # Windows
xdg-open index.html   # Linux
```

### Opção 2 — GitHub Pages
1. Faça um fork deste repositório
2. Vá em **Settings → Pages**
3. Selecione a branch `main` e pasta `/ (root)`
4. Acesse `https://seu-usuario.github.io/autoportfolio`

### Opção 3 — Netlify (arrastar e soltar)
1. Acesse [netlify.com/drop](https://app.netlify.com/drop)
2. Arraste a pasta do projeto
3. Pronto — URL gerada automaticamente

---

## 📁 Estrutura do projeto

```
autoportfolio/
└── index.html    # Aplicação completa — editor + gerador de templates
```

Sim, é um arquivo só. Todo o código do editor React e dos 5 templates está dentro do `index.html`.

---

## 🎨 Templates

| Template | Estilo | Fundo |
|---|---|---|
| **Minimalista** | Tipográfico, editorial, espaçoso | Branco |
| **Dark Studio** | Profissional, estilo GitHub | `#0d1117` |
| **Cyberpunk** | Neon, grid de fundo, futurista | `#020209` |
| **Criativo** | Hero colorido com cor de destaque | `#fafaf8` |
| **Glassmorphism** | Gradiente escuro, efeito de vidro | `#0f0f1a` |

---

## 🗺️ Roadmap

- [ ] Mais templates
- [ ] Exportação em PDF
- [ ] Preview responsivo (tablet)
- [ ] Importar dados de perfil do GitHub via API
- [ ] Suporte a múltiplos idiomas no portfólio gerado
- [ ] Animações de entrada no portfólio exportado

---

## 🤝 Contribuindo

Contribuições são muito bem-vindas!

```bash
# Fork o projeto
# Crie uma branch para sua feature
git checkout -b feature/minha-feature

# Faça o commit
git commit -m "feat: adiciona minha feature"

# Abra um Pull Request
```

---

## 📄 Licença

MIT — use, modifique e distribua à vontade. Se usar como base para algo, um crédito é sempre apreciado. 🙂

---

<p align="center">Feito com ☕ como projeto pessoal · <a href="https://jottaramoss.github.io/AutoPortfolio/">autoportfolio</a></p>
