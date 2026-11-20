# Aula 09 — Projeto React 02 (Roteamento SPA com React Router)

##  Resumo da Aula

Nesta aula foi consolidado o desenvolvimento de Single Page Applications (SPAs) multi-páginas utilizando navegação declarativa e programática no ecossistema React:

* **React Router (`react-router-dom`):** configuração de `BrowserRouter`, `Routes` e `Route` para alternar telas sem recarregamento completo da página.
* **Navegação Declarativa (`Link` e `NavLink`):** criação de barras de navegação com destaque automático da rota ativa (`isActive`).
* **Rotas Dinâmicas (`useParams`):** leitura de parâmetros de URL (`/evento/:id`) para renderizar páginas individuais de detalhes a partir de uma fonte de dados.
* **Navegação Programática (`useNavigate`):** redirecionamento automático do usuário após a conclusão de ações (como o envio do formulário de inscrição).
* **Fallback 404 e Rewrites:** tratamento de rotas inexistentes (`path="*"`) e configuração de `vercel.json` para suportar atualização de página em rotas internas na Vercel.

---

##  Entrega da Aula — EventHub SENAI

* **Repositório:** [github.com/LuisFelipeCorreia/projeto-react-02](https://github.com/LuisFelipeCorreia/projeto-react-02)
* **Deploy (Vercel):** [https://projeto-react-02-topaz.vercel.app](https://projeto-react-02-topaz.vercel.app)

### Mapa de Rotas e Arquitetura (`src/`)
* `/` → `pages/Home.jsx`: vitrine de eventos com busca em tempo real e filtro por categoria.
* `/evento/:id` → `pages/EventoDetalhes.jsx`: página dinâmica com informações completas do evento e formulário controlado de inscrição.
* `/inscricoes` → `pages/MinhasInscricoes.jsx`: painel com comprovantes, protocolos gerados e opção de cancelamento persistidos via `localStorage`.
* `*` → `pages/NotFound.jsx`: página de erro 404 personalizada com retorno rápido à vitrine.