![GIT](https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png)
# Resumo sobre GIT e comandos importantes
Um documento com um resumo sobre o GIT e com o principais comandos presentes nessa tecnologia.
- ### [Principais conceitos sobre GIT](#principais-conceitos-sobre-git-1)
- ### [Comandos importantes do GIT](#comandos-importantes-do-git-1)
---
# Principais conceitos sobre GIT
Principais conceitos sobre GIT.
- ### [O que é GIT?](#o-que-é-git-1)
- ### [O que é controle de versão?](#o-que-é-controle-de-versão-1)
- ### [Funcionalidades](#funcionalidades-1)
- ### [Tipos de controles de versões](#tipos-de-controles-de-versões-1)
- ### [Características do GIT](#características-do-git-1)
## O que é GIT?
GIT é uma ferramenta de controle de versão.

## O que é controle de versão?
Software que tem a função de fazer o gerenciamento de versões de um documento qualquer. Muito usado em empresas e projetos de desenvolvimento de softwares.

## Funcionalidades
Algumas das importantes funcionalidades de um software de controle de versão.

 - #### Histórico:
    Alternar entre versões. Como um "backup" para caso ocorra erros nas mudanças;
 - #### Trabalho em equipe:
    Desenvolvimento em paralelo em diferentes ambientes;
 - #### Ramificação:
    Possibilidade de criar várias versões versões a partir de um ponto. E a possiblidade de junção das funcionalidades após finalizadas;
 - #### Rastreabilidade:
    Identificar em que ponto a mudança foi feita e identificar responsável pela mudança.

## Tipos de controles de versões
Dois principais tipos de controles de versões.

 - #### Centralizada: 
    Servidor que possui todo o histórico. Padrão usado durante muitos anos;
 - #### Distribuído:
    Cada computador possui uma cópia do repositório. **GIT** é distribuído.

## Características do GIT
Algumas das características do GIT.

 - #### Operações locais:
    Navegações entre as versões pelo histórico e criação de novas ramificações/versões;
 - #### Somente adição de conteúdo:
    Mesmo a remoção de arquivo, é feita através de uma adição de um versão onde diz que o arquivo foi removido;
 - #### Integridade:
    Uma vez um arquivo adicionado, todo seu histórico é mantido;
 - #### Autonomia:
    Facilidade para diversos colaboradores realizarem alterações sem a dependência de arquivos.

---
# Comandos importantes do GIT
Principais comandos para se usar no GIT.
- ### [Comandos básicos](#comandos-básicos-1)
- ### [Funcionamento do GIT](#funcionamento-do-git-1)

## Comandos básicos

- ### `git config`
  Os comandos **`git config --global user.name "Seu Nome"`** e **`git config --global user.email "seu-email@mail.com"`** são usados para configurar seu usuário e seu e-mail no seu computador. São importantes principalmente quando há comunicação com repositórios remotos.
  O comando **`git config --list`** é usado para ver todas as configurações do seu git local.

 - ### `git init`
   Usado para inicializar um repositório.

 - ### `git status`
   Mostra o estado dos arquivos. Ver mais em [Funcionamento do GIT](#funcionamento-do-git-1).

 - ### `git add nome_do_arquivo`
   Torna-se um arquivo rastreável, ou seja, adiciona as alterações ao **staging area** para serem salvas. Pode ser utilizado o comando **`git add .`** para adicionar todas alterações.

 - ### `git commit -m "uma mensagem"`
   Salva as alterações.

## Funcionamento do GIT
Mostrando como o git funciona.
![funcionanmento do git](/funcionamento_do_git.png)

 - ### `git diff`
   Mostra as alterações ou diferenças da working directory.

 - ### `git diff --cached` ou `git diff --staged`
   Mostra as alterações ou diferenças da staging area.

 - ### `git log`
   Histórico de alterações. São listadas da mais recentes para a mais antigas.

 - ### `git log --oneline` 
   Histórico de alterações. São listadas em linhas únicas da mais recentes para a mais antigas.

 - ### `git checkout {código do commit}` 
   Usa commits anteriores. O código do commit pode ser obtido com o **`git log`**.

 - ### `git checkout main` 
   Usa a branch principal. Usado também para voltar para o último commit. Em alguns caso, em que a branch principal é a master, utiliza-se o comando **`git checkout master`**.

 - ### `git checkout nome_do_arquivo`
   Desfaz as alterações de um arquivo.

 - ### `git reset --hard`
   Defaz todas as alterações. Volta para o estado inicial do último commit.

 - ### `git clean -f`
   Remove arquivos que foram adicionados mas ainda não foram salvos.