# MBA Fiap - Cadastro de usuários
<br>
Projeto de conclusão da disciplina de DESENVOLVIMENTO DE MICROSSERVIÇOS E APIS - MBA FIAP
<br>

<br>

## Aluno 
  -  Adriano Bastos e Silva (rm344764)
<br>

## Descrição:
O Projeto consiste numa aplicação para realizar as seguintes funções relacionadas a uma cadastro de usuários do sistema:
  - Cadastrar um usuário;
  - Criptografar a senha do usuário cadastrado;
  - Autenticar usuário;
  - Gerar token JWT;
  - Alterar a senha do usuário

<br>

## Requisitos:
- node versão 14.19.1 ou superior;
- instalar nodemon, com o comando abaixo: 
  ```
  npm install nodemon
  ```

## Rodando o projeto:
  - Para rodar o projeto é necessário rodar o comando:
    ```
    npm install && npm start
    ```

## Rotas: incluido arquivo do postman para execução das requisições -> TrabalhoFiap.postman_collection.json

  ### - Cadastro:
  - **POST:**
    - http://localhost:3001/api/usuarios/cadastro
    
  - **RETORNOS:**
    - **status (201):**
      "Cadastro realizado"
    
    - **status (500):**
      "Erra ao tentar gerar a senha -> Error: data and salt arguments required"
      "Erra ao cadastrar"
  
  ### - LOGIN:
  - **POST:**
    - http://localhost:3001/api/usuarios/login
   
  - **RETORNOS:**
    - **status (200):**
        "Autenticado",
       
    - **status (400):**
        "Usuário não localizado"

    - **status (500):**
       "Usuário ao tentar localizar"
       "Usuário ao validar senha"    
<br>

 ### - ATUALIZAR DADOS DO USUÁRIO:
  - **PUT:**
    - http://localhost:3001/api/usuarios/atualizarsenha/6434b05805d173c031373a04
    
  - **RETORNOS:**
    - **status (202):**
      "Atualizado",
      
    - **status (400):**
      "Não foi possível atualizar -> null"

    - **status (500):**
       "Erra ao tentar gerar a senhar"
       "Erro ao processar a atualização"

      
