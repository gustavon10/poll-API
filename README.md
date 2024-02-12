<h1>API de Enquetes</h1>
<p>Durante o Rocketseat Next Level Week, edição Expert, foi concebido este projeto que viabiliza a criação e votação em enquetes. Essas enquetes são armazenadas de forma persistente em um banco de dados PostgreSQL, sendo o Prisma ORM a ferramenta utilizada para esta integração. Além disso, a API incorpora uma conexão Websocket. Cada vez que um usuário lança seu voto, a API dispara uma mensagem através dessa conexão, informando atualizações sobre a votação de uma enquete específica. A ordenação e gestão dos votos nas pesquisas são realizadas por meio do Redis.</p>
<h2>Tecnológias utilizadas</h2>
<div>
  <p><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg" width="40px" heigth="40px" /> NodeJS</p>
  <p><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/prisma/prisma-original.svg" width="40px" heigth="40px" /> Prisma</p>
  <p><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/redis/redis-original.svg" width="40px" heigth="40px" /> Redis</p>
  <p><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg" width="40px" heigth="40px" /> PostgreSQL</p>
  <p><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-plain-wordmark.svg" width="40px" heigth="40px" /> Docker</p>
  <p><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postman/postman-original.svg" width="40px" heigth="40px" /> Postman</p>
</div>

<h2>Rotas</h2>
<p>A API estará rodando http://localhost:3333 e o websocket no ws://localhost:3333.</p>

| Rota                   | Método   | Protocolo |     Descrição     |
| -------------          | -------- | --------- | ----------------- |
| /polls                 | POST     | HTTP      | Crie uma nova enquete. |
| /polls/:pollId         | GET      | HTTP      | Faça uma única enquete. |
| /polls/:pollId/vote    | POST     | HTTP      | Vote em uma opção de enquete. |
| /polls/:pollId/results | --       | WS        | Abra uma conexão WS para receber os resultados dos votos. |
