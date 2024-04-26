# Projeto de Testes End-to-End com Cobertura de Código

Este repositório contém um projeto de estudo sobre testes end-to-end utilizando o framework Mocha e a biblioteca Supertest para testar uma API em Node.js. O objetivo é demonstrar como realizar testes automatizados que cobrem diversas rotas e cenários de uma aplicação web.

## Descrição

O projeto consiste em uma API simples em Node.js (`api.js`) que define diferentes rotas e suas respectivas funções de tratamento de requisição. Utilizamos o módulo `http` para criar o servidor web e definimos as rotas da API dentro de um objeto `routes`.

Alguns pontos-chave do projeto incluem:

- **Roteamento de Requisições**: O servidor web roteia as requisições HTTP para funções específicas com base na URL e no método HTTP.
  
- **Tratamento de Requisições POST**: A rota `/login` é tratada de forma assíncrona para processar requisições POST de login e verificar as credenciais do usuário.

- **Testes Automatizados**: O arquivo de teste (`api.test.js`) utiliza o framework Mocha para estruturar os testes e o Supertest para realizar as requisições HTTP simuladas.

## Funcionalidades Testadas

No arquivo de teste (`api.test.js`), foram implementados os seguintes cenários de teste:

1. **Teste da Rota `/contacts`**:
   - Verifica se a página de contato retorna o código HTTP 200 e o conteúdo esperado ("contact us page").

2. **Teste de Redirecionamento da Rota Inexistente**:
   - Testa se uma rota inexistente (`/hi`) redireciona para a rota padrão (`/hello`) com sucesso.

3. **Teste de Login com Credenciais Válidas**:
   - Simula uma requisição POST de login com credenciais válidas e verifica se retorna o código HTTP 200 e a mensagem de sucesso ("Logging has succeeded!").

4. **Teste de Login com Credenciais Inválidas**:
   - Testa uma requisição POST de login com credenciais inválidas e verifica se retorna o código HTTP 401 e a mensagem de falha ("Logging failed!").

