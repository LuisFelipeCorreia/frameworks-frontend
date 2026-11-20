# Aula 08 — Projeto React 01 (Componentes, Props & Hooks)

##  Resumo da Aula

Nesta aula foram aplicados os fundamentos essenciais de arquitetura de aplicações em React:

* **Componentização Modular:** divisão da interface em componentes funcionais independentes e reutilizáveis (`Header`, `FormTarefa`, `FiltroBar`, `CardTarefa`).
* **Fluxo de Dados Unidirecional (Props & Callbacks):** passagem de dados de pai para filho via `props` e comunicação inversa através de funções de *callback* (`onAdicionar`, `onAlternar`, `onRemover`).
* **Gerenciamento de Estado (`useState`):** controle reativo de listas, filtros combinados e formulários controlados.
* **Efeitos Colaterais e Persistência (`useEffect`):** sincronização automática do estado das tarefas com o `localStorage` do navegador.
* **Renderização Condicional e Listas:** uso de `.map()` com chaves únicas (`key`) e exibição dinâmica de estados vazios e contadores.

---

##  Entrega da Aula — TaskFlow React

* **Repositório:** [github.com/LuisFelipeCorreia/projeto-react-01](https://github.com/LuisFelipeCorreia/projeto-react-01)
* **Deploy (Vercel):** [https://projeto-react-01-rho.vercel.app](https://projeto-react-01-rho.vercel.app)

### Estrutura de Componentes (`src/`)
* `App.jsx`: componente raiz que centraliza o estado, regras de filtragem e persistência no `localStorage`.
* `components/Header.jsx`: cabeçalho com indicadores dinâmicos de tarefas totais, pendentes e concluídas.
* `components/FormTarefa.jsx`: formulário controlado para criação de tarefas com categoria e prioridade.
* `components/FiltroBar.jsx`: barra de pesquisa textual e botões de filtro por status.
* `components/CardTarefa.jsx`: cartão individual com ações de concluir/reabrir e excluir.