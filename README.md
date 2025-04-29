# 📚 Fundamentos de Git e Git Flow

## 📁 Índice

- [Introdução](#introducao)
- [Pré-requisitos](#pre-requisitos)
- [Comandos Git](#comandos-git)
- [Git Flow](#git-flow)
    - [Estrutura de branches](#estrutura-de-branches)
    - [Diagrama do fluxo](#diagrama-do-fluxo)
    - [Criação das branches](#criacao-das-branches)
- [Boas práticas](#boas-praticas)
- [Materiais Complementares](#materiais-complementares)
- [Licença](#licenca)

## Introducao

Repositório criado para ensinar e contruibuir no aprendizado de versionamento de código e fluxo de trabalho utilizando o Git. Sendo assim, possibilitando a aplicabilidade do conhecimento adquirido em projetos pessoais ou processos seletivos.

## Pre-requisitos

1. Possuir o [Git](https://git-scm.com/downloads) instalado na máquina.
2. Ter uma conta no [GitHub](https://github.com).
3. [VsCode](https://code.visualstudio.com) ou qualquer outro editor de código.

## Comandos Git

### Principais

- Inicializar repositório

    ```sh
    git init nome-da-pasta
    ```
- Verificar status dos arquivos
    ```sh
    git status
    ```
- Adicionar alterações

    ```sh
    git add "Nome do arquivo"
    ```
- Realizar um *commit*
    ```sh
    git commit -m "Mensagem do commit"
    ```
- Verificar histórico de *commits*
    ```sh
    git log
    ```
- Criar e verifcar *branch*
    ```sh
    git branch nome-da-branch
    ```
- Unir alterações de *branches*
     ```sh
    git merge nome-da-branch
    ```
## Git Flow

Modelo de trabalho baseado na criação de *branches* para organizar e gerenciar de forma mais eficaz o desenvolvimento do projeto.

### Estrutura de branches

- `main` : manter código estável.
- `develop` : desenvolvimento geral do projeto.
- `feature/` : destinada a cada funcionalidade.
- `release/` : criação de versões do projeto.
- `hotfix/` : correção de *bugs* e criada a partir da `main`

### Diagrama do fluxo

```plaintext
main
|
|___develop
|   |
|   |__feature/nome-da-funcionalidade
|   |
|   |____release/1.0.0
|
|__hotfix/nome-do-bug
```

### Criacao das branches

- Criar *branch* `develop`

    ```sh
    git checkout -b develop
    ```
- Criar *branch* `feature/`

    ```sh
    git checkout -b feature/nome-da-funcionalidade
    ```
- Criar *branch* `hotfix/`
    ```sh
    git checkout -b hotfix/nome-do-bug
    ```
- Criar *branch* `release/`
    ```sh
    git checkout -b release/numero-da-release
    ```

## Boas praticas

- Mantenha o `main` estável.
- Faça *commits* claros e constantes.
- Busque trabalhar em *branches* separadas.