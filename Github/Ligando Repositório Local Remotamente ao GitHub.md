# Ligando repositório local remotamente ao GitHub

## Passos iniciais


* Escolha um local em sua máquina para criar uma pasta aonde ficarão seus repositórios associados ao GitHub; 

* Após criar a pasta, clique com o botão direito do mouse e selecione a opção "_**Git Bash Here**_" como na imagem abaixo; 

  


<div align="center">
	<img align="Git-Bash here" alt="Checkboxes" src="https://jcutrer.com/wp-content/uploads/2018/01/git-bash-here-right-click.png.webp"    
</div>



* Configure globalmente adicionando com os seguintes comandos:


> ```
> $ git config --global user.name "Nome"
> $ git config --global user.email "e-mail@exemplo.com"
> ```

* Importante que o nome e email informado seja equivalente à conta do GitHub detentora dos repositórios, para evitar futuros transtornos.

## Git remote

1. Tenha certeza de que foi feito o atalho "_**Git Bash Here**_" na pasta que deseja;

2. Inicie um repositório local com o comando:

> ```
> $ git init
> ```

3. Afim de seguir um padrão, se ao fim do identificador de diretório estiver **(master)** como branch principal, mude para **(main)** com o comando:

> ```
> $ git branch -m master main
> ```

</hr>

4. Caso o repositório do GitHub ainda esteja vazio ou apenas com os arquivos iniciais (**README.md** e **LICENSE**), faça o comando "**git remote**" com o endereço HTTPS do seu repositório: 

> ```
> $ git remote add origin https://github.com/username/repositorio.git
> ```

5. Faça o comando "**git status**" para verificar se ainda há algo para ser adicionado ou "commitado":

> ```
> $ git status
> ```

6. Se existir algum retorno, faça os seguintes comandos ("**git add ***"para adicionar tudo que ainda não está no Github e "**git commit**" para o repositório local entender o que deverá ser empurrado para o repositório remoto):

> ```
> $ git add *
> $ git commit -m "mensagem do commit"
> ```

7. Agora empurre com o comando "**git push**" tudo aquilo que foi "commitado":

> ```
> $ git push -u origin main
> ```

</hr>

4. Caso o repositório do GitHub já contenha alguns arquivos, faça o comando "**git pull**" com o endereço HTTPS do seu repositório depois de ser definido o repositório remoto e siga a partir do passo "**5.**":

> ```
> $ git pull origin main
> ```
