# Webschool.io - Curso Vue.js 2.x - Apostila


## vue-cli

O **vue-cli** é uma ferramenta com o intuito de facilitar a criação de projetos. Ele é responsável por criar alguns templates para projetos em Vue.js. Nesse projeto iremos utilizar o template do webpack disponibilizado pelo **vue-cli**.  

Para instalar o **vue-cli** basta executar o seguinte comando: `npm install -g vue-cli`.

Para visualizar os templates disponíveis basta executar o seguinte comando: `vue list`. E para criar um projeto com um template padrão do **vue-cli**, basta executar o seguinte comando: `vue init nome_template nome_projeto`, por exemplo, `vue init webpack vue-webpack`.

Ele irá instalar o projeto dividido em vários arquivos e pastas, vamos descobrir o que cada pasta possui e qual é sua responsabilidade.

* `build`: possui os arquivos de configuração que irão fazer o build da aplicação;
* `dist`: após realizar `npm run build` o webpack irá compilar o seu projeto para produção, minificando e concatenando todos os arquivos;  
* `config`: alguns arquivos que precisamos alterar uma coisa ou outra em nosso ambiente;
* `src`: é o nosso CÓDIGO FONTE, onde iremos brincar pra caramba.
