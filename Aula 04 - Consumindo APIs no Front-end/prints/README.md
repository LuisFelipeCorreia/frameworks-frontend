# Aula 04 — Consumindo APIs no Front-end

##  Resumo da Aula

Nesta aula foram estudados os conceitos de comunicação cliente-servidor na Web e integração com APIs REST:

* **Protocolo HTTP e REST:** métodos (`GET`, `POST`, `PUT`, `DELETE`), endpoints, headers, formatos JSON e códigos de status (`200`, `201`, `400`, `404`, `500`).
* **Consumo Assíncrono no Front-end:** uso da `Fetch API` nativa, Promises e sintaxe `async/await` com tratamento de erros (`try/catch`).
* **CORS (Cross-Origin Resource Sharing):** configuração no back-end Express (`cors()`) para permitir requisições vindas de domínios diferentes.

---

##  Atividade 01 — 10 Projetos Clonados que Consomem APIs

Repositório reunindo 10 projetos open-source em Vanilla JS, React, Vue e Angular com tabela detalhando frameworks e APIs utilizadas:

* **Repositório e Tabela Completa:** [github.com/LuisFelipeCorreia/projetos-api-clones](https://github.com/LuisFelipeCorreia/projetos-api-clones)

---

##  Atividade 02 — API Express de Data/Hora + Front-end

* **Repositório (Back-end + Front-end):** [github.com/LuisFelipeCorreia/api-data-hora](https://github.com/LuisFelipeCorreia/api-data-hora)
* **Endpoint da API (Deploy):** [https://api-data-hora.vercel.app/data-hora](https://api-data-hora.vercel.app/data-hora)
* **Aplicação Front-end (Deploy):** [Acessar Relógio Online](https://api-data-hora-frontend.vercel.app)

###  Evidências (Prints)

1. **Código-fonte (Express + Fetch):**
   ![Código API e Front-end](./prints/01-codigo-api.png)
2. **API retornando JSON (`/data-hora`):**
   ![API Online](./prints/02-api-online.png)
3. **Front-end consumindo a API em tempo real:**
   ![Front-end Funcionando](./prints/03-frontend-funcionando.png)
4. **Painel de Deploy na Vercel:**
   ![Deploy Vercel](./prints/04-deploy-vercel.png)