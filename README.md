# estagio-repo
Documentação de projetos

# Projeto Busca CEP
Uma aplicação simples que realiza uma chamada para a API pública do ViaCEP, retornando dados os dados tratados para o usuário. O objetivo desse projeto era consumir uma API externa e receber esses dados, tratar eles e devolver para a página inicial, facilitando a utilização da aplicação.
Tecnologias utilizadas: HTML5, CSS3, JavaScript, Bootstrap, jQuery, JavaScript e Fetch para realizar chamadas para a API.

Link da aplicação rodando: https://busca-cep-sistemas.vercel.app/

## Busca por CEP
Interface inicial:

![alt text](imagens/image.png)

Ao digitar o CEP e clicar o enviar, uma função é disparada e realiza uma busca até a API do ViaCEP

![alt text](imagens/image-2.png)

A partir disso, é gerado um card com a ajuda do Bootstrap devolvendo as informações necessárias para o usuário

![alt text](imagens/image-3.png)
![alt text](imagens/image-4.png)

## Busca por Rua
Para fazer uma busca por rua, é nécessário ser passado para a API, o estado(UF) e a cidade, para listar ao usuário, utilizei a API pública do IBGE.

![alt text](imagens/image-5.png)

Ao clicar em selecionar um estado uma chamada é feita para a API pública do IBGE, listando todos os estados do Brasil, preenchendo a lista

![alt text](imagens/image-6.png)
![alt text](imagens/image-8.png)

Depois, o estado selecionado é salvo e realizado uma nova busca para a API do IBGE, dessa vez listando as cidades do estado selecionado

![alt text](imagens/image-9.png)
![alt text](imagens/image-10.png)

Após isso, quando selecionado o estado, a cidade e digitado o nome da rua, ao realizar a busca será devolvido ao usuário todos os resultados encontrados com as especificações passadas

![alt text](imagens/image-11.png)
![alt text](imagens/image-12.png)

# Projeto Partner
Projeto da faculdade da disciplina de Projeto Integrador 3 - Fullstack
A idéia do projeto seria criar uma plataforma de cursos online com uma aplicação full stack, como requisito era necessário conter pelo menos um CRUD, autenticação de usuários, utilização da arquitetura MVC para melhorar a estrutura do projeto e que o back-end fosse separado do front-end, com o front-end apenas realizando as chamadas.
Tecnologias utilizadas: HTML5, CSS3, JavaScript, Bootstrap, jQuery, Fetch, SQLite

Link da aplicação rodando: https://front-fullstack-base9.vercel.app/
OBS: O back-end está hospedado no render.com, caso haja muitas requisições de uma vez elas são bloqueadas temporariamente.

Interface inicial:

![alt text](imagens/image-partner.png)
![alt text](imagens/image-partner-1.png)
![alt text](imagens/image-partner-2.png)

## Navegação do site

Para a navegação estou utilizando jQuery, ao selecionar uma página a div anterior é escondida e mostrado a nova, como por exemplo ao clicar em **Sobre**.

![alt text](imagens/image-partner-23.png)
![alt text](imagens/image-partner-5.png)
![alt text](imagens/image-partner-4.png)

O mesmo acontece com **Contato**

![alt text](imagens/image-partner-6.png)

## Autenticação

(Queria ressaltar que a parte de autenticação foi feita com base em um projeto pronto e uso de inteligência artificial.)

Para a autenticação, é fornecido o nome do usuário e a senha, ou no caso do registro de novo usuário: nome, email e senha

![alt text](imagens/image-partner-7.png)
![alt text](imagens/image-partner-8.png)

### Login

Quando fornecido usuário e senha, é checado no banco de dados, se as informações estiverem corretas o usuário recebe um token(hash), finalizando a autenticação e mostrando o conteúdo quando o usuário estiver logado. Caso as informações não estejam presentes no banco de dados resultará em erro.

![alt text](imagens/image-partner-9.png)
![alt text](imagens/image-partner-10.png)

### Registro

Para registro, quando fornecidos usuário, email e senha, é criado no banco de dados o usuário, para criptografia da senha foi utilizado o bcrypt. Também foi criado um usuário administrador, para que fosse feito os testes, o usuário administrador não pode ser deletado por outros usuários.

![alt text](imagens/image-partner-11.png)
![alt text](imagens/image-partner-12.png)

## Tela inicial (logado)

Nela podemos acessar 2 CRUDS, alunos e cursos.

![alt text](imagens/image-partner-13.png)

## Alunos

Ao clicar em alunos, já é realizado a primeira chamada para a API, listando todos os alunos presentes no banco de dados.

![alt text](imagens/image-partner-14.png)
![alt text](imagens/image-partner-15.png)

Para completar o CRUD, também é possivel editar um usuário, excluir um usuário e criar um novo no banco de dados.

### Editar

![alt text](imagens/image-partner-16.png)
![alt text](imagens/image-partner-17.png)

### Deletar

![alt text](imagens/image-partner-18.png)
![alt text](imagens/image-partner-19.png)

### Criar um novo

![alt text](imagens/image-partner-20.png)
![alt text](imagens/image-partner-21.png)

## Cursos

Voltando para a parte de cursos, temos mais um CRUD, onde o GET é feito também assim que a página é carregada, listando todos os cursos.

![alt text](imagens/image-partner-22.png)
![alt text](imagens/image-partner-25.png)

### Cadastrar novo curso

Para cadastrar um novo curso deverá ser informado: Nome do curso, descrição, duração em semanas, número de aulas, nível do curso e url da imagem do curso. Esses dados são enviados para o banco de dados e realizado mais um get, listando todos os cursos atualizados.

![alt text](imagens/image-partner-26.png)
![alt text](imagens/image-partner-27.png)
![alt text](imagens/image-partner-28.png)

## Editar um curso

Para editar, o menu de curso abre novamente com o ID do curso selecionado, podendo ser alterado com o patch, após isso o curso é atualizado no banco de dados. (como exemplo irei alterar a imagem do curso)

![alt text](imagens/image-partner-29.png)
![alt text](imagens/image-partner-30.png)

## Excluir um curso

Assim como a edição, primeiro é selecionado o id do curso e enviado a requisição de DELETE, para que seja deletado no banco de dados.

![alt text](imagens/image-partner-31.png)
![alt text](imagens/image-partner-32.png)

## Mais sobre o Back-end

### Rotas

#### Cursos

![alt text](imagens/image-partner-34.png)

#### Usuários

![alt text](imagens/image-partner-35.png)

#### Index / login

![alt text](imagens/image-partner-36.png)