<h1 align="center">TaskFlow</h1>
<p align="center">
  <img alt="ReactJS" src="https://img.shields.io/badge/React-61DAFB.svg?style=for-the-badge&logo=React&logoColor=black">
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-5FA04E.svg?style=for-the-badge&logo=nodedotjs&logoColor=white">
  <img alt="Express.js" src="https://img.shields.io/badge/Express-000000.svg?style=for-the-badge&logo=Express&logoColor=white">
</p>

![sample image](https://github.com/user-attachments/assets/1cef315b-48c4-4e52-849d-cc53cdfed1f8)

<p align="center">
  <a href="#introdu%C3%A7%C3%A3o">Introdução</a> |
  <a href="#recursos">Recursos</a> |
  <a href="#finalidade">Finalidade</a> |
  <a href="#como-utilizar">Como utilizar</a> |
  <a href="#cr%C3%A9ditos">Créditos</a>
</p>

### Introdução

TaskFlow é um sistema de gestão de tarefas Web que oferece um ambiente simplificado e acessível para que os usuários organizem suas demandas pessoais e profissionais por meio de tarefas que podem ser divididas em diferentes listas e quadros.

### Recursos

O TaskFlow permite com que os usuários realizem as seguintes ações:

- **Cadastro**: O usuário é capaz de criar uma conta utilizando nome de usuário, e-mail e senha, além de poder entrar em sua conta.
- **Alteração de dados cadastrais**: O usuário é capaz de mudar seu nome, e-mail, senha e foto de perfil quando quiser.
- **Quadros de Tarefas**: O usuário é capaz de criar, visualizar, editar e remover quadros, onde cada quadro possui um nome, descrição e suas próprias listas de tarefas.
- **Listas de Tarefas**: O usuário, dentro de um quadro, é capaz de criar, visualizar, editar e remover listas de tarefas, onde cada lista possui um nome e suas próprias tarefas.
- **Tarefas**: O usuário, numa lista, é capaz de criar, visualizar, editar e remover tarefas, onde cada tarefa possui um nome, descrição, estado e até no máximo três etapas para conclusão.

O estado de uma tarefa é definido por sua cor:
- **Card com cor normal**: A tarefa não passou da data de vencimento.
- **Card com cor azul**: A tarefa vence hoje.
- **Card com cor vermelha**: A tarefa está atrasada.
- **Card com cor verde**: A tarefa foi concluída. Todas as etapas de uma tarefa precisam ser cumpridas para que o usuário possa concluí-la.

### Finalidade

Um projeto de Sistema de Gestão de Tarefas Web foi idealizado pela equipe interna do Ramo Estudantil IEEE CEFET/RJ para avaliar o grupo de trainees do Processo Seletivo 24.2 para a equipe de desenvolvimento web da WolfByte. Com esta ideia, os trainees decidiram o nome e identidade visual do projeto, criaram o design, modelagem de banco de dados e desenvolveram o front-end e o back-end da aplicação. O TaskFlow foi aprovado pela diretoria do Ramo Estudantil, incorporando os trainees envolvidos à equipe de desenvolvimento web.

### Tecnologias utilizadas
- **Design**: FlutterFlow, Figma
- **Front-end**: React.js
- **Back-end**: Node.js, Express
- **SGBD**: MySQL

### Como utilizar

O TaskFlow possui alguns requisitos para funcionar:
- **MySQL Server** (Utilizado para criar o banco de dados para a aplicação)
- **Node.js e NPM** (Gerenciador de pacotes para o Node.js, que será utilizado para instalar os pacotes necessários para a aplicação)

Primeiro, crie o banco de dados local no MySQL Terminal:
```
CREATE DATABASE taskflowdb;
```
Então, utilize o seu terminal para ir até o diretório do projeto (Case-Web/taskflow) e instale os pacotes utilizados no projeto:
```
npm i
```
E atualize o banco de dados para ter as tabelas utilizadas pela aplicação:
```
npx knex migrate:latest
```
Também é necessário configurarmos nossas variáveis de ambiente utilizando o .env. Para isso:
1. Crie um arquivo de texto chamado .env na pasta taskflow
2. Dentro desse arquivo, insira as variáveis de ambiente. O .env nesse caso deve conter:
  - **DB_HOST** ("anfitrião" do banco)
  - **DB_PORT** (porta utilizada pelo banco)
  - **DB_DATABASE** (nome da base de dados a ser utilizada)
  - **DB_USERNAME** (nome de usuário do banco)
  - **DB_PASSWORD** (senha do usuário do banco)
  - **JWT_KEY** (pode ser "minhachave")

Informações como o HOST, PORT e USERNAME podem ser obtidas pelo terminal do MySQL ao utilizar os seguintes comandos:
  ```
  SHOW GLOBAL VARIABLES LIKE [opção];
  ```

Após estas etapas de configurações, podemos executar a aplicação.
Em um terminal na pasta taskflow, inicie o back-end:
```
npm run start
```
Em outro terminal, também na pasta taskflow, inicie o front-end:
```
npm run dev
```
No terminal que você iniciou o front-end, aperte O e depois Enter e uma aba será aberta no seu navegador contendo a aplicação.

### Créditos

O TaskFlow foi desenvolvido por:

- **Lucas Ferreira de Ornelas Santos**: Primeiro líder geral, atuando na subdivisão do grupo em equipes, no design e na modelagem do banco de dados.
- **Luiz Felipe Ribeiro Zuim Teixeira**: Último líder geral,, atuando no design e desenvolvimento front-end.
- **Allan Ribeiro de Souza**: Assessor de gestão, auxiliando na organização da equipe.
- **[Rafael do Amaral Costa](https://github.com/jake7038)**: Líder de desenvolvimento, atuando no design, modelagem do banco de dados, desenvolvimento front-end e desenvolvimento back-end.
- **[Erick Martins Silva](https://github.com/erickMartinsSilva)**: Membro técnico, atuando no design, modelagem do banco de dados e desenvolvimento front-end.
- **[Ennya Gomes Oliveira Campos](https://github.com/EnnyaGoc)**: Membro técnico, atuando no design, modelagem do banco de dados, desenvolvimento front-end e desenvolvimento back-end.
- **[Luiz Antonio de Souza da Silva](https://github.com/LuizAntonioSantos)**: Membro técnico, atuando no design e desenvolvimento front-end.
- Agradecimentos especiais aos assessores técnicos **[Gustavo Barros Rosa de Andrade](https://github.com/GustavoAndrad)** e **[João Pedro Weydt de Faria](https://github.com/jpwf)** por auxiliar os trainees durante o desenvolvimento do projeto. Obrigado!
