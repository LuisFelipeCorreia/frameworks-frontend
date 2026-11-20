# Aula 06 — Projetos Front-End (Gestão Ágil)

##  Resumo da Aula

Nesta aula foram estudados os fundamentos de planejamento, organização e entrega contínua aplicados ao desenvolvimento de software Front-end:

* **Metodologias Ágeis (Scrum e Kanban):** entregas incrementais em ciclos curtos (*Sprints*), transparência do fluxo de trabalho e adaptação rápida a mudanças de requisitos.
* **Product Backlog e Priorização:** levantamento de requisitos em formato de *User Stories* (Histórias de Usuário) priorizadas por valor de negócio (método MoSCoW: *Must, Should, Could, Won't*).
* **Estimativas (Planning Poker / Story Points):** mensuração de esforço, complexidade e risco utilizando a sequência de Fibonacci (`1, 2, 3, 5, 8, 13`).
* **Fluxo Git e Estratégia de Branches:** organização de branches (`main`, `develop`, `feature/*`, `fix/*`), *Conventional Commits* e revisão de código via *Pull Requests*.
* **Definition of Done (DoD):** checklist objetivo que garante qualidade técnica, responsividade e deploy validado antes de considerar uma tarefa concluída.

---

##  Projeto Integrador — Visão Geral

* **Produto:** **EventHub** — Plataforma Web para Divulgação e Inscrição em Eventos Acadêmicos e Tecnológicos.
* **Stack Definida:** React (Vite), Tailwind CSS, React Router, API REST (Node.js/Express) e Deploy na Vercel.
* **Board Kanban (GitHub Projects):** [https://github.com/LuisFelipeCorreia/frameworks-frontend/projects](https://github.com/LuisFelipeCorreia/frameworks-frontend/projects)

---

##  Product Backlog (Priorizado e Estimado)

| ID | História de Usuário (User Story) | Prioridade | Estimativa (SP) | Sprint |
| :--- | :--- | :--- | :---: | :---: |
| **US-01** | Como visitante, quero visualizar a listagem de eventos disponíveis com data, local e categoria para escolher em qual participar. | Alta (Must) | 5 | Sprint 01 |
| **US-02** | Como visitante, quero filtrar eventos por categoria e buscar pelo nome para encontrar rapidamente temas do meu interesse. | Alta (Must) | 3 | Sprint 01 |
| **US-03** | Como visitante, quero acessar uma página de detalhes do evento (`/evento/:id`) com descrição completa e palestrantes. | Alta (Must) | 5 | Sprint 01 |
| **US-04** | Como participante, quero preencher um formulário de inscrição com validação de campos para garantir minha vaga no evento. | Alta (Must) | 5 | Sprint 01 |
| **US-05** | Como participante, quero visualizar meus eventos inscritos em uma aba "Minhas Inscrições" salva localmente/API. | Média (Should) | 3 | Sprint 02 |
| **US-06** | Como organizador, quero cadastrar e editar novos eventos através de um painel administrativo protegido. | Média (Should) | 8 | Sprint 02 |
| **US-07** | Como usuário mobile, quero navegar por toda a plataforma em telas pequenas com layout 100% responsivo. | Alta (Must) | 3 | Sprint 01 |
| **US-08** | Como visitante, quero alternar entre modo claro e escuro para maior conforto visual. | Baixa (Could) | 2 | Sprint 02 |

---

##  Planejamento da Sprint 01

* **Duração:** 2 semanas (10 dias úteis)
* **Capacidade Total Planejada:** 21 Story Points
* **Meta da Sprint 01:** Entregar o MVP navegável do **EventHub** com listagem de eventos, filtros dinâmicos, página de detalhes com roteamento e formulário funcional de inscrição publicado na Vercel.

### Quebra de Tarefas Técnicas (Sprint Backlog)

1. **[SETUP-01]** Configurar repositório Git, estrutura de pastas React + Tailwind CSS e deploy contínuo na Vercel *(2 SP)*
2. **[UI-01]** Criar componentes reutilizáveis (`Navbar`, `EventCard`, `FilterBar`, `Footer`) *(3 SP)*
3. **[FEAT-01]** Implementar listagem e filtragem por categoria/busca em tempo real (`US-01`, `US-02`) *(5 SP)*
4. **[FEAT-02]** Configurar `React Router` e criar tela de detalhes dinâmicos `/evento/:id` (`US-03`) *(5 SP)*
5. **[FEAT-03]** Desenvolver formulário de inscrição com estado controlado e feedback visual (`US-04`) *(4 SP)*
6. **[QA-01]** Revisar responsividade mobile/desktop e corrigir ajustes de layout (`US-07`) *(2 SP)*

---

##  Quadro Kanban (Status Atual da Sprint 01)

| Backlog (Sprint 02) | To Do (A Fazer) | In Progress (Em Andamento) | Code Review (Revisão) | Done (Concluído) |
| :--- | :--- | :--- | :--- | :--- |
| **US-05** Minhas Inscrições *(3 SP)* | **[FEAT-03]** Formulário de Inscrição *(4 SP)* | **[FEAT-02]** Rota `/evento/:id` *(5 SP)* | **[FEAT-01]** Listagem e Filtros *(5 SP)* | **[SETUP-01]** Setup + Deploy Vercel *(2 SP)* |
| **US-06** Painel Organizador *(8 SP)* | **[QA-01]** Testes Responsivos *(2 SP)* | — | — | **[UI-01]** Componentes Base *(3 SP)* |
| **US-08** Tema Claro/Escuro *(2 SP)* | — | — | — | — |

---

##  Estratégia de Versionamento e Branches (Git Flow)

Para manter o código estável e rastreável durante o desenvolvimento:

* **`main`:** Branch de produção. Recebe apenas código testado e aprovado; cada merge dispara deploy automático na Vercel.
* **`develop`:** Branch de integração das funcionalidades concluídas da Sprint.
* **`feature/<nome-da-tarefa>`:** Criada a partir de `develop` para cada nova funcionalidade (ex.: `feature/filtro-eventos`, `feature/pagina-detalhes`).
* **`fix/<nome-do-ajuste>`:** Criada para correção de bugs específicos (ex.: `fix/validacao-formulario`).

### Padrão de Commits (*Conventional Commits*)
* `feat:` nova funcionalidade (ex.: `feat: adiciona filtro por categoria na listagem`)
* `fix:` correção de bug (ex.: `fix: ajusta quebra de layout no mobile`)
* `style:` ajustes visuais/CSS sem alteração de lógica
* `docs:` atualização de documentação e planejamento

---

##  Definition of Done (DoD)

Uma tarefa só pode ser movida para a coluna **Done** quando atender a todos os critérios abaixo:

1. **Código Implementado:** Requisitos da *User Story* atendidos sem erros no console do navegador ou warnings de build.
2. **Responsividade Validada:** Interface testada em resoluções mobile (`375px`), tablet (`768px`) e desktop (`1280px+`).
3. **Versionamento Limpo:** Código enviado via *Pull Request* com commits semânticos e revisado antes do merge em `develop`/`main`.
4. **Deploy Ativo:** Build gerado com sucesso e funcionalidade verificada na URL pública de produção (Vercel).