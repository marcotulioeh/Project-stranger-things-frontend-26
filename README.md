# Boas vindas ao repositório do projeto Stranger Things!

---

<details>
  <summary><strong>👨‍💻 O que deverá ser desenvolvido</strong></summary><br />

  Você vai adaptar e configurar os projetos descritos nesse README para que seja feito o deploy deles. Você vai colocar os projetos front-end e back-end no ar com o `Heroku`, utilizando o `Docker` em ambiente de produção. Além disso, você vai alterar alguns comportamentos aplicando os conceitos vistos no conteúdo. 

  ## Desenvolvimento

  Adapte e configure os projetos descritos nesse *README* para que seja feito o deploy utilizando `Docker` por meio do `Heroku`.

</details>

---

# Requisitos do projeto

⚠️ Lembre-se de que o seu projeto só será avaliado se estiver passando por **todos os _checks_** do **Linter**. Utilize o comando `npm run lint` no seu terminal para verificar os _checks_ do **Linter** 😉 ⚠️

Os requisitos estão agrupados por `frontend` e `backend`. Realize as alterações nos respectivos diretórios de cada repositório.

⚠️**IMPORTANTE**: Para esse projeto, as variáveis de ambiente devem ser definidas em um arquivo .env e o arquivo deve ser enviando no seu PR(Pull Request). ISSO NÃO É UMA PRÁTICA DE MERCADO, contexto no qual o arquivo .env deve ser sempre incluído no .gitignore, pois contém informações sensíveis. Aqui o arquivo .env será enviado apenas por motivo de avaliação.

---

<details>
  <summary>
  Faça o deploy do front-end.
  </summary><br/>

  ⚠️**IMPORTANTE**: Assim como no `Back-end`, a variável de ambiente `GITHUB_USER` deverá ser criada com o seu nome de pessoa usuária do GitHub.

  1. Crie um app do Heroku com o front-end. Vamos deixar o Heroku utilizar as configurações padrão. No momento de criar o app do Heroku, utilize o `buildpack` descrito abaixo, em **Dicas**;

  2. O nome do seu app no Heroku deve ser seu nome de pessoa usuária do GitHub seguido de "-ft". Por exemplo, se o seu nome de pessoa usuária do GitHub for "student", o nome do seu app será "student-ft" e a URL ***precisar ser*** https://student-ft.herokuapp.com/;

  2. Configure as variáveis de ambiente do app para apontar para as API's publicadas;

  3. Faça o deploy com o git.

  Para publicar seu front-end React, utilize o buildpack [mars/create-react-app](https://elements.Heroku.com/buildpacks/mars/create-react-app-buildpack).

  Lembre-se de que é possível testar o comportamento definindo as variáveis de ambiente em sua máquina. Você pode fazer as variáveis apontarem tanto para o back-end rodando localmente em sua máquina, quanto para as API's já publicadas nos requisitos anteriores.

  O que será testado:

    - Se ao visitar sua página no Heroku, o botão de mudar de realidade existe;

    - Se a pesquisa funciona como deveria, fazendo chamada a API externa;

    - Se o botão de mudar de realidade funciona;

    - Se os botões de próxima página e página anterior funcionam.  
</details>

## Bônus

### 8 - Verifica os multi-ambientes e modo de desenvolvimento.

<details>
  <summary>
    Utilize a estratégia de multi-ambientes no front-end.
  </summary><br/>

  Para isso:

  - Renomeie o remote atual para `remote-desenvolvimento`;
  
  - Crie e faça o deploy de um novo app no Heroku, conforme [requisito 7](#7---verifica-se-foi-feito-o-deploy-do-frontend-no-heroku). O nome do seu novo app no heroku deve ser seu nome de usuário do github seguido de "-pd" ("pd" se refere à "produção", ou seja, não está em desenvolvimento). Por exemplo, se o seu usuário do github for "student", o nome do seu app será "student-pd" e a url ***precisa ser*** https://student-pd.herokuapp.com/;
  
  - Adicione um elemento ao frontend que identifique que a aplicação está rodando em modo de "desenvolvimento". Esse elemento **deve** ser visível e conter o texto "Em desenvolvimento";
  
  - Lembre-se de criar uma variável de ambiente para controlar esse comportamento, configurando-a para ter um valor diferente em cada um dos ambientes publicados. Atente-se às regras de nomes para [váriáveis de ambiente utilizadas no React](https://create-react-app.dev/docs/adding-custom-environment-variables/).
  
  O que será testado:

  - Se ao acessar o front-end de desenvolvimento, haverá a tag com o texto "Em desenvolvimento";

  - Se ao acessar o front-end de produção, não haverá a tag.
</details>

---
