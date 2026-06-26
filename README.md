# 🔒 App Lista de Tarefas - Backend

Backend da aplicação **App Lista de Tarefas**, desenvolvido em PHP utilizando arquitetura em camadas (Model, Service e Controller) e acesso ao banco de dados com PDO.

> Este repositório contém apenas a lógica de negócio e acesso aos dados da aplicação. A interface do usuário está disponível em outro repositório.

## 🔗 Repositório do Front-end

https://github.com/leobernardo05/App_lista_tarefas

---

# 📚 Tecnologias utilizadas

- PHP 8
- MySQL
- PDO (PHP Data Objects)
- Programação Orientada a Objetos (POO)
- Arquitetura MVC (adaptada)
- XAMPP

---

# 📂 Estrutura do projeto

```
app_lista_tarefas_protegido
│
├── conexao.php
├── tarefa.model.php
├── tarefa.service.php
└── tarefa_controller.php
```

---

# 📄 Descrição dos arquivos

## conexao.php

Responsável pela conexão com o banco de dados utilizando PDO.

---

## tarefa.model.php

Classe que representa a entidade **Tarefa**, contendo seus atributos e métodos mágicos (`__get` e `__set`).

Principais atributos:

- id
- tarefa
- id_status

---

## tarefa.service.php

Camada responsável pelas operações no banco de dados.

### Funcionalidades implementadas

- Inserir tarefa
- Recuperar todas as tarefas
- Recuperar tarefas pendentes
- Atualizar tarefa
- Remover tarefa
- Marcar tarefa como realizada

Todas as consultas utilizam **Prepared Statements**, aumentando a segurança da aplicação contra SQL Injection.

---

## tarefa_controller.php

Responsável por receber as requisições da aplicação e encaminhá-las para a camada de serviço.

### Ações disponíveis

| Ação | Descrição |
|------|-----------|
| inserir | Cadastra uma nova tarefa |
| recuperar | Lista todas as tarefas |
| recuperarTarefasPendentes | Lista apenas tarefas pendentes |
| atualizar | Atualiza uma tarefa |
| remover | Exclui uma tarefa |
| marcarRealizada | Marca uma tarefa como concluída |

---

# 🗄 Banco de Dados

A aplicação utiliza duas tabelas.

## tb_tarefas

| Campo | Tipo |
|--------|------|
| id | INT |
| tarefa | VARCHAR |
| id_status | INT |

---

## tb_status

| id | Status |
|----|---------|
| 1 | Pendente |
| 2 | Realizada |

---

# ⚙ Funcionalidades

✔ Cadastro de tarefas

✔ Atualização de tarefas

✔ Exclusão de tarefas

✔ Marcação de tarefas como realizadas

✔ Listagem completa

✔ Listagem de tarefas pendentes

✔ Separação entre frontend e backend

✔ Conexão segura utilizando PDO

---

# 🔒 Segurança

O backend foi desenvolvido mantendo a lógica da aplicação separada da interface pública.

Principais práticas adotadas:

- Utilização de Prepared Statements
- Separação da camada de acesso ao banco
- Encapsulamento utilizando Programação Orientada a Objetos
- Organização em camadas

---

# 🚀 Como utilizar

Clone o projeto

```bash
git clone https://github.com/leobernardo05/App_lista_tarefas_back-end.git
```

Configure o arquivo

```
conexao.php
```

informando:

- Host
- Banco de dados
- Usuário
- Senha

Após isso, integre este backend ao projeto do frontend.

---

# 📌 Integração

Este backend foi desenvolvido para funcionar juntamente com o projeto:

**App Lista de Tarefas (Frontend)**

https://github.com/leobernardo05/App_lista_tarefas

---

# 👨‍💻 Autor

**Leonardo Bernardo**

GitHub:

https://github.com/leobernardo05

LinkedIn:

*(adicione o link do seu perfil)*

---

# 📄 Licença

Este projeto foi desenvolvido para fins educacionais durante os estudos de Desenvolvimento Web em PHP.
