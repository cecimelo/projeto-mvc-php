# Gerenciador de Tarefas e Filmes (MVC)

Este projeto é uma aplicação web desenvolvida em PHP seguindo a arquitetura MVC (Model-View-Controller). O sistema permite o gerenciamento de tarefas pessoais e uma lista de filmes favoritos, com autenticação de usuários e persistência em banco de dados MySQL.

## Funcionalidades

- Autenticação: Login, cadastro e logout de usuários com segurança.
- Gestão de Tarefas: Listar, criar, editar, excluir e alternar status de conclusão.
- Gestão de Filmes: Listar, criar, editar e excluir filmes (incluindo título, gênero, ano e sinopse).
- Perfil: Edição de dados do usuário logado (Nome e Senha).
- Segurança: Proteção de rotas para garantir que apenas usuários autenticados acessem seus dados.

## Padroes de Projeto (Design Patterns)

- Singleton: Implementado na classe Conexao.php. Este padrão garante que a aplicação utilize uma única instância da conexão PDO durante todo o ciclo de vida da requisição, economizando recursos do servidor.
- Factory: Utilizado nos Models (Usuario, Tarefa, Filme). Centraliza a lógica de criação de objetos, garantindo que as instâncias das entidades sejam criadas de forma padronizada.

## Estrutura do Projeto

### Configuracao

- config/Conexao.php: Gerencia a conexão com o banco de dados utilizando o padrão Singleton.

### Controllers

- AutenticacaoController.php: Responsável pelo controle de sessão e segurança de acesso.
- UsuarioController.php: Gerencia o cadastro de usuários e a atualização do perfil.
- TarefaController.php: Processa todas as operações CRUD da entidade Tarefa.
- FilmeController.php: Processa todas as operações CRUD da entidade Filme.

### Models

- Usuario.php, Tarefa.php e Filme.php: Representam as entidades do sistema e contêm suas respectivas Factories para criação de objetos.

### Views

- index.php / filmes.php: Listagens principais de cada entidade.
- nova-tarefa.php / editar-tarefa.php: Telas de gerenciamento de tarefas.
- novo-filme.php / editar-filme.php: Telas de gerenciamento de filmes.
- editar-perfil.php: Interface para o usuário atualizar seus dados cadastrais.

### Componentes e Estilos

- header.php e footer.php: Fragmentos de interface reutilizáveis.
- styles.css: Centralização dos estilos visuais do sistema.

## Tecnologias Utilizadas

- Linguagem: PHP 8.x
- Banco de Dados: MySQL (PDO)
- Arquitetura: MVC + Design Patterns (Singleton e Factory)
- Interface: HTML5, CSS3 e Material Symbols.

---