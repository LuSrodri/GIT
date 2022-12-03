![GIT](https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png)
# Resumo sobre GIT e comandos importantes
Um documento com um resumo sobre o GIT e com o principais comandos presentes nessa tecnologia.
- ### [Principais conceitos](#principais-conceitos-1)
- ### [Comandos importantes](#comandos-importantes-1)
---
# Principais conceitos
Principais conceitos sobre GIT.
- ### [O que é GIT?](#o-que-é-git-1)
- ### [O que é controle de versão?](#o-que-é-controle-de-versão-1)
- ### [Funcionalidades](#funcionalidades-1)
- ### [Tipos de controles de versões](#tipos-de-controles-de-versões-1)
- ### [Características do GIT](#características-do-git-1)
## O que é GIT?
GIT é uma ferramenta de controle de versão.
##### [Voltar aos Principais conceitos](#principais-conceitos-1)
## O que é controle de versão?
Software que tem a função de fazer o gerenciamento de versões de um documento qualquer. Muito usado em empresas e projetos de desenvolvimento de softwares.
##### [Voltar aos Principais conceitos](#principais-conceitos-1)
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
##### [Voltar aos Principais conceitos](#principais-conceitos-1)
## Tipos de controles de versões
Dois principais tipos de controles de versões.

 - #### Centralizada: 
    Servidor que possui todo o histórico. Padrão usado durante muitos anos;
 - #### Distribuído:
    Cada computador possui uma cópia do repositório. **GIT** é distribuído.
##### [Voltar aos Principais conceitos](#principais-conceitos-1)
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
    
##### [Voltar aos Principais conceitos](#principais-conceitos-1)
##### [Voltar ao topo](#resumo-sobre-git-e-comandos-importantes)
---
# Comandos importantes
Principais comandos para se usar no GIT.
- ### [Comandos básicos](#comandos-básicos-1)
- ### [Funcionamento do GIT](#funcionamento-do-git-1)
- ### [Repositórios remotos](#repositórios-remotos-1)
- ### [Branches](#branches-1)
- ### [Tags](#tags-1)
##### [Voltar ao topo](#resumo-sobre-git-e-comandos-importantes)
## Comandos básicos
Comandos de configurações e alguns comandos iniciais.
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
##### [Voltar aos Comandos importantes](#comandos-importantes-1)
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
##### [Voltar aos Comandos importantes](#comandos-importantes-1)

## Repositórios remotos
Trabalhando com repositórios remotos.

- ### `git clone link_do_repositorio_remoto`
   Clona o repositório remoto na máquina local.

- ### `git push`
   Envia as mudanças locais para o servidor.

- ### `git pull`
   Baixa as mudanças do servidor para a máquina local.

**Atenção!** Na maioria dos casos, se o usuário ainda não estiver autenticado, o serviço responsável pelo repositório remoto pode pedir a verificação, para certificar-se que as requisições como **`git clone`**, **`git push`** e **`git pull`** é permitida.
##### [Voltar aos Comandos importantes](#comandos-importantes-1)
## Branches
Branches são ramificações no projeto que permite que funcionalidades sejam desenvolvidas separadamente sem impactar nas funcionalidades estáveis no projeto.
![funcionanmento do git](/branches.png)
 - ### `git branch`
   Lista todas as branches do repositório.

 - ### `git branch nome_da_nova_branch`
   Cria uma nova branch no repositório.

 - ### `git checkout nome_da_branch`
   Muda de branch.

 - ### `git checkout -b nome_da_nova_branch`
   Cria e muda para a nova branch.

 - ### `git push -u origin nome_da_branch_criada_localmente`
   Envia uma branch criada localmente para o repositório remoto.

 - ### `git pull`
   Atualiza as branches locais.

 - ### `git branch -d nome_da_branch` ou `git branch -D nome_da_branch`
   Remove branches locais.

 - ### `git branch --delete origin nome_da_branch`
   Remove branches remotas.

 - ### `git branch -m nome_atual nome_novo`
   Renomeia uma branch local.

**Atenção!** Não existe um comando específico para alterar nome de branches remotas.

 - ### `git merge outra_branch`
   Traz as alterações de outra branch para a branch selecionada.

##### [Voltar aos Comandos importantes](#comandos-importantes-1)

## Tags
Usando tags.
 - ### `git tag -a {nome da tag} -m "Título da tag"`
   Cria uma tag.

 - ### `git tag"`
   Lista todas as tags.

 - ### `git push origin {nome da tag}"`
   Envia Tag para o repositório remoto.

 - ### `git checkout {nome da tag}"`
   Usa uma tag.

 - ### `git tag -d {nome da tag}"`
   Remove uma tag local.

 - ### `git push --delete origin {nome da tag}"`
   Remove uma tag remota.

 - ### `git tag -a {nome da tag} {código de um commit}"`
   Cria uma tag em um commit antigo.
##### [Voltar aos Comandos importantes](#comandos-importantes-1)

## Stashes
Usando stashes.

 - ### `git stash`
   Salva as mudanças para posterior ação.

- ### `git stash list`
   Lista as mudanças salvas.

- ### `git stash "mensagem"`
   Salva as mudanças com uma mensagem personalizada.

- ### `git stash apply`
   Usa a última mudança salva.

- ### `git stash pop`
   Usa e exclui a última mudança salva.

- ### `git stash drop stash@{1}`
   Usa e exclui uma mudança específica.

##### [Voltar aos Comandos importantes](#comandos-importantes-1)
##### [Voltar ao topo](#resumo-sobre-git-e-comandos-importantes)