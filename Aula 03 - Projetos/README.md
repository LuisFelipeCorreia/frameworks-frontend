# Aula 03 — Projetos com Frameworks Front-end

##  Resumo da Aula

Nesta aula foram explorados na prática os principais frameworks e bibliotecas do ecossistema Front-end moderno, desenvolvendo a **mesma aplicação (Catálogo de Cursos Tech)** em quatro tecnologias distintas, além da prática de clonagem e versionamento de repositórios existentes.

---

##  Projetos Desenvolvidos

| Projeto | Tecnologia | Repositório | Deploy (Vercel) |
| :--- | :--- | :--- | :--- |
| **Projeto 01** | React (Vite) | [github.com/LuisFelipeCorreia/tema-react](https://github.com/LuisFelipeCorreia/tema-react) | [tema-react.vercel.app](https://tema-react.vercel.app) |
| **Projeto 02** | Vue 3 (Vite) | [github.com/LuisFelipeCorreia/tema-vue](https://github.com/LuisFelipeCorreia/tema-vue) | [tema-vue.vercel.app](https://tema-vue.vercel.app) |
| **Projeto 03** | Angular | [github.com/LuisFelipeCorreia/tema-angular](https://github.com/LuisFelipeCorreia/tema-angular) | [tema-angular.vercel.app](https://tema-angular.vercel.app) |
| **Projeto 04** | Next.js | [github.com/LuisFelipeCorreia/tema-nextjs](https://github.com/LuisFelipeCorreia/tema-nextjs) | [tema-nextjs.vercel.app](https://tema-nextjs.vercel.app) |
| **Projeto 05** | React (Clone MDN) | [github.com/LuisFelipeCorreia/projeto-clone](https://github.com/LuisFelipeCorreia/projeto-clone) | Repositório clonado com histórico |

---

##  Comparativo Técnico entre os 4 Frameworks

Abaixo está a análise comparativa obtida ao implementar as mesmas funcionalidades (busca em tempo real, filtro por categoria e lista dinâmica de favoritos) nas quatro ferramentas:

| Critério | React | Vue 3 | Angular | Next.js |
| :--- | :--- | :--- | :--- | :--- |
| **Natureza** | Biblioteca focada na camada de visualização (UI) | Framework progressivo | Framework completo (*batteries-included*) | Meta-framework full-stack baseado em React |
| **Linguagem Principal** | JavaScript / TypeScript + JSX | JavaScript / TypeScript + SFC (`.vue`) | TypeScript obrigatório + HTML/CSS separados | JavaScript / TypeScript + JSX |
| **Reatividade e Estado** | Hooks explícitos (`useState`, `useMemo`) | Reatividade nativa via Proxy (`ref`, `computed`) | Detecção de mudanças baseada em classes e Signals | Hooks do React + Server/Client Components (`'use client'`) |
| **Estrutura de Arquivos** | Livre e flexível (`App.jsx` + `App.css`) | Single File Component (`<script>`, `<template>`, `<style>` no mesmo arquivo) | Rígida e modular (`app.ts`, `app.html`, `styles.css`) | Baseada em sistema de arquivos (`src/app/page.js`) |
| **Renderização** | CSR (Client-Side Rendering) por padrão | CSR por padrão (SSR via Nuxt) | CSR por padrão (SSR opcional via Angular SSR) | Híbrida: SSR, SSG e CSR nativos |
| **Curva de Aprendizado** | Baixa a moderada | Baixa (sintaxe intuitiva próxima ao HTML/JS) | Alta (exige TypeScript, decorators e arquitetura própria) | Moderada (exige entender fronteira servidor/cliente) |
| **Indicação de Uso** | SPAs dinâmicas, dashboards e ecossistemas customizáveis | Projetos ágeis, times enxutos e migração gradual | Sistemas corporativos de grande porte e equipes padronizadas | Aplicações com foco em SEO, e-commerce e performance inicial |

###  Principais Conclusões Práticas

1. **Produtividade e Sintaxe:** O **Vue 3** destacou-se pela concisão ao unir lógica, marcação e estilo em um único arquivo `.vue` com `v-model` e `computed`.
2. **Flexibilidade:** O **React** ofereceu controle direto sobre o fluxo de dados imutável com `useState` e `.filter()`, mantendo o código enxuto.
3. **Padronização Corporativa:** O **Angular** trouxe maior estrutura inicial e tipagem forte com TypeScript, ideal para projetos grandes que exigem arquitetura rígida.
4. **Capacidade Full-Stack e SEO:** O **Next.js** manteve a mesma sintaxe do React, acrescentando roteamento por pastas e suporte nativo à renderização no servidor.