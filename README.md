<!-- Título -->
# Utilizando SSH Para Comunicação

***Conteúdo da Aula:***

O processo de comunicação com o Github utilizando o SSH é mais complexo que utilizando HTTPS.

Para isso, precisamos gerar as chaves SSH e adicioná-las ao nosso perfil do Github.

* Sendo assim, vamos ao passo-a-passo:

  * Para gerar uma nova chave SSH, o primeiro passo é, no terminal (ou Git Bash) utilizar o seguinte comando:
    * ssh-keygen -t rsa -b 4096 -C "<your_email@example.com>", onde você deve substituir o email e adicionar o utilizado no github.

  * Após isso, será perguntado onde você deseja salvar a chave SSH.
  * Neste ponto, pode clicar em "enter", o destino padrão já é suficiente.
  * Feito isso, será solicitado uma chave secreta:
    * Esta chave é utilizada em conjunto com o hash para gerar sua chave SSH;
    * Pode adicionar qualquer frase (desde que você se lembre, haha).
  * Com isso, sua chave foi gerada:
    * O próximo passo é adicioná-la ao nosso perfil do github

  * Agora, com as chaves SSH geradas, vamos adicioná-la ao github.

  * Para isso, vamos ao passo-a-passo:

    * Ao realizar o login, vamos até a seguinte rota:
      * [settings/keys](https://github.com/settings/keys "Clique aqui")
      * Na página, clicamos em **“NEW SSH KEY”**.
  * Agora, voltando ao terminal, precisamos copiar nossa chave gerada anteriormente.
  * Caso você utilize o macOS, no terminal (ou git bash), digitamos o seguinte comando:

    ```powershell
    pbcopy < ~/.ssh/id_rsa.pub
    ```

  * Caso você utilize o Windows, no gitbash, digitamos o seguinte comando:

    ```powershell
    clip < ~/.ssh/id_rsa.pub
    ```

  * Caso você utilize o Linux, no terminal, digitamos os seguintes comandos:

    ```powershell
    sudo apt-get install xclip e xclip -sel clip < ~/.ssh/id_rsa.pub
    ```

  * Feito isso, a chave ssh estará em nossa área de transferência.
  * Agora, voltamos à página aberta do Github [settings/keys](https://github.com/settings/keys) e colamos a chave, conforme a imagem abaixo:

    ![Exemplo](https://d2v0x26thbzlwf.cloudfront.net/prod/527/img/rId15uih22wf4.enz.png)

  * Feito isso, já podemos salvar e a chave já está configurada.

  * O último passo é testar a comunicação.

  * Para isso, no terminal (ou gitbash), utilizamos o seguinte comando:

    ```powershell
    ssh -T git@github.com.
    ```

  * Será solicitado que digitemos, então, a chave secreta que utilizamos ao criar a chave ssh no processo anterior.

  * Ao fazer isso, a comunicação será feita com sucesso e nossa chave estará configurada:

    ![Exemplo](https://d2v0x26thbzlwf.cloudfront.net/prod/527/img/rId17jbhg53xl.ocz.png)

<!-- Informações -->
## &#8505; Informações

![Visitors](https://api.visitorbadge.io/api/visitors?path=Devsgeeknerd%2Fcla-uti-ssh-par-com-com-htt-ssh-git-fun-bas&label=Visitantes&labelColor=%23700070&labelStyle=none&countColor=%23000fff&style=plastic&color=%23ffffff "Total de Visitantes")
&nbsp;
![Followers](https://img.shields.io/github/followers/Devsgeeknerd?style=p&label=Seguidores&labelColor=800080&color=000fff "Total de Seguidores")
&nbsp;
![Watchers](https://img.shields.io/github/watchers/Devsgeeknerd/cla-uti-ssh-par-com-com-htt-ssh-git-fun-bas?style=p&label=Observadores&labelColor=800080&color=000fff "Total de Observadores")
&nbsp;
![Stars](https://img.shields.io/github/stars/Devsgeeknerd/cla-uti-ssh-par-com-com-htt-ssh-git-fun-bas?style=p&label=Estrelas&labelColor=800080&color=000fff "Total de Estrelas")
&nbsp;
![Forks](https://img.shields.io/github/forks/Devsgeeknerd/cla-uti-ssh-par-com-com-htt-ssh-git-fun-bas?style=p&label=Bifurcações&labelColor=800080&color=000fff "Total de Bifurcações")
&nbsp;
![Repo Size](https://img.shields.io/github/repo-size/Devsgeeknerd/cla-uti-ssh-par-com-com-htt-ssh-git-fun-bas?style=p&label=Tamanho&labelColor=800080&color=000fff "Tamanho do Repositório")
&nbsp;
![License](https://img.shields.io/github/license/Devsgeeknerd/cla-uti-ssh-par-com-com-htt-ssh-git-fun-bas?style=p&label=Licença&labelColor=800080&color=000fff "Licença do Repositório")
