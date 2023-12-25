# Instalação, Configuração e Autenficação

## Instalando o Git no Windows:
Para instalar o Programa Git em seu computador Acesse < https://git-scm.com/download/win >;

- Em seguida realize o download do instalador e execute;
- Aceite a licença e clique em “Next”, e prosiga configurando como desejar e clicando em “Next”;
- Finalize clicando em “Install”, e “Finish”.

Em "Select Components“, deixe as opções “Git Bash Here” e “Git GUI Here” marcadas.

## Configurando o Git
### configurando o seu nome de usuario e email (globalmente):
```
$ git config --global user.name "Nome Sobrenome"
$ git config --global user.email seuemail@email.com
```
### configurando o nome da Branch padrão:
```
$ git config --global init.defaultBranch main
```
Clonado arquivos de seu repertório remoto (GitHub)
```
$ git clone URL
```

## Autentificando via Token
O Programa Git não depende da plataforma github para fazer o versionamento, porém o Github é uma ferramenta muito util para o armazenamento remoto e compartilhamento de dados.

A autentificação via token serve como uma proteção no compartilhamento de dados dificultando a 
 
Para autentificar via token é necessário ter uma conta no github e seguir esse passos:
1. Criar um token no Github

Home page > Clique em seu icone> settings> Developer Settings> Personal acess token > token (classic)> Generate new token> token (classic)
Agora uma pagina será carregada onde você tem que preencher as seguintes informações:
* Note
* Expiration (este é o periodo de tempo que o token ficará ativo)
* repo (marque um x na caixa)

Finalize a criação do token clicando em "gerate token"

*copie o codigo do token. 

2. Autentificar na sua maquina.

entre novamente no git Bash e insira:
```
$ git clone URL
```
uma caixa de texto irá se abrir pedindo
* Nome de Usuario 
* Email
* Senha (Code token)
Ao inserir todos esses dados os arquivos do repositório remoto serão copiados localmente

## Armanamento de credenciais 
o procedimento acima tem quer ser realizado toda vez, para automatizar esse processo insira este codigo:

```
$ git config --global credential.helper store
```
uma caixa de texto irá se abrir pedindo
* Nome de Usuario 
* Email
* Senha (Code token)

Agora todas suas credencias ficaram salvas na sua maquina, a quando for realizado alguma tarefa que necessita de autentificação será realizado de forma automatica.