# 📘 Atividade: Persistindo dados com arquivos JSON

## 🎯 Objetivo

Crie um programa Python que salve e carregue uma lista de tarefas em um arquivo JSON. Você praticará a conversão entre estruturas Python e JSON e aprenderá a preservar dados entre execuções.

## 📝 Tarefas

### 🛠️ Salvar dados em um arquivo JSON

#### Descrição
Crie uma lista de tarefas em Python e grave seu conteúdo no arquivo `tarefas.json` usando o módulo `json`.

#### Requisitos
O programa concluído deve:

- Criar uma lista com pelo menos duas tarefas.
- Representar cada tarefa como um dicionário com os campos `titulo` e `concluida`.
- Usar `json.dump` para salvar a lista em `tarefas.json`.
- Gerar um arquivo JSON válido e legível, com indentação.

### 🛠️ Carregar e exibir as tarefas

#### Descrição
Leia `tarefas.json` e mostre cada tarefa no terminal, indicando se está concluída ou pendente.

#### Requisitos
O programa concluído deve:

- Usar `json.load` para ler o arquivo.
- Exibir o título de cada tarefa.
- Mostrar claramente o estado de cada tarefa: concluída ou pendente.
- Processar todas as tarefas sem alterar os dados salvos.

### 🛠️ Adicionar uma tarefa e salvar as alterações

#### Descrição
Permita que a pessoa usuária informe o título de uma nova tarefa. Adicione a tarefa à lista carregada e salve a lista atualizada no mesmo arquivo.

#### Requisitos
O programa concluído deve:

- Solicitar o título da nova tarefa pelo terminal.
- Adicionar a tarefa com `concluida` inicialmente definida como `false` no JSON.
- Salvar a lista atualizada em `tarefas.json`.
- Manter as tarefas anteriores ao adicionar uma nova.
- Preservar a nova tarefa quando o programa for executado novamente.

### 🛠️ Iniciar quando o arquivo ainda não existe

#### Descrição
Adapte o programa para que uma primeira execução sem `tarefas.json` comece com uma lista vazia e possa criar o arquivo ao salvar uma tarefa.

#### Requisitos
O programa concluído deve:

- Tratar o caso em que `tarefas.json` ainda não existe, sem encerrar com erro.
- Iniciar com uma lista vazia quando o arquivo estiver ausente.
- Criar `tarefas.json` ao salvar a primeira tarefa.
- Continuar carregando e preservando os dados nas execuções seguintes.
