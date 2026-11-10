# 📘 Atividade: Building REST APIs with FastAPI

## 🎯 Objetivo

Construa e teste uma API REST com FastAPI para gerenciar itens em memória. Você praticará criação de endpoints, validação de dados com modelos, uso de códigos HTTP e testes automatizados.

## 📝 Tarefas

### 🛠️ Criar e executar uma aplicação FastAPI

#### Descrição
Configure uma aplicação FastAPI mínima e execute o servidor localmente para explorar a documentação interativa gerada pelo framework.

#### Requisitos
O programa concluído deve:

- Instalar FastAPI e Uvicorn no ambiente Python.
- Criar uma aplicação FastAPI com um endpoint `GET /health`.
- Retornar `{"status": "ok"}` ao acessar `GET /health`.
- Iniciar a aplicação com Uvicorn e disponibilizar a documentação em `/docs`.

### 🛠️ Implementar operações para gerenciar itens

#### Descrição
Estenda a aplicação para permitir que clientes criem, consultem, atualizem e removam itens. Armazene os dados em memória; não é necessário configurar um banco de dados.

#### Requisitos
O programa concluído deve:

- Criar um item com `POST /items` e retornar o item criado.
- Listar os itens com `GET /items`.
- Consultar um item por identificador com `GET /items/{item_id}`.
- Atualizar um item com `PUT /items/{item_id}`.
- Remover um item com `DELETE /items/{item_id}`.
- Retornar `404 Not Found` quando o identificador solicitado não existir.

### 🛠️ Validar dados e respostas HTTP

#### Descrição
Defina modelos de entrada e saída com Pydantic para validar os dados dos itens e tornar as respostas da API previsíveis para seus clientes.

#### Requisitos
O programa concluído deve:

- Exigir um nome não vazio e um preço maior que zero para cada item.
- Rejeitar dados inválidos com `422 Unprocessable Entity`.
- Retornar `201 Created` ao criar um item e um código de sucesso apropriado ao atualizar ou remover um item.
- Manter as respostas dos endpoints no formato JSON.

### 🛠️ Testar os endpoints da API

#### Descrição
Escreva testes automatizados para verificar os principais fluxos da API usando o cliente de testes do FastAPI.

#### Requisitos
O programa concluído deve:

- Testar a criação e a consulta de um item.
- Testar a atualização e a remoção de um item existente.
- Verificar as respostas para dados inválidos e identificadores inexistentes.
- Executar os testes com sucesso usando `pytest`.
