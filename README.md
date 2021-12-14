# Blog
S.O de desenvolvimento: **Ubuntu 20.04.3 LTS** 

Blog desenvolvido com Django, esta online no link:

```
https://giodevelopment.pythonanywhere.com/
```

Para testar o site, baixe o repositorio, abra no Visual Studio Code

![vscode](https://drive.google.com/file/d/1hPRs2rJMlFmk8x5u9m-BOJ7WNQ7sz4b3/view?usp=sharing)

Caso não tenha o python instalado, instale executado no terminal: 

```
$ sudo apt install python3
```

Instale o ambiente virutual, no qual iremos executar o projeto:

```
$  sudo apt install python3-venv
```

**Observação:** Em algumas versões do Debian/Ubuntu, iniciar o ambiente virtual com este comando gera o seguinte 	erro:

```
Error: Command '['/home/eddie/Slask/tmp/venv/bin/python3', '-Im', 'ensurepip', '--upgrade', '--default-pip']' returned non-zero exit status 1
```

Para contornar esse problema, use o comando `virtualenv`.

```
$ sudo apt install python-virtualenv
$ virtualenv --python=python3.6 myvenv
```

**Oservação:** Se você obtiver um erro como

```
E: Unable to locate package python3-venv
```

no lugar do comando mostrado acima, execute esse:

```
$ sudo apt install python3.6-venv
```

Crie um ambiente virtual atraves do comando:

```
$ python3 -m venv blogDjango
```

Ative o ambiente virtual atraves do comando:

```
$ source blogDjango/bin/activate
```

Caso não possua o DJango instalado, entre no seu ambiente virtual criado e inicie a instalação:

```
$ source blogDjango/bin/activate
$ python -m pip install --upgrade pip
```

Agora, execute `pip install -r requirements.txt` para instalar o Django.

```
$ pip install -r requirements.txt
```

Teremos que executar as migrates na raiz do projeto, para inicializarmos o banco de dados

```
$ python manage.py migrate
```

Agora execute o servidor local:

```
$ python manage.py runserver
```

O Blog estara acessível em seu Browser padrão na URL:

```
http://127.0.0.1:8000/
```

Agora, você verá algo  do tipo:
![0](/home/gio/Imagens/0.png)

Precisamos agora configurar um administrador que possa publicar e gerenciar o blog, execute: 

```
$ python manage.py createsuperuser
```

Configure nome, email senha:

![5](/home/gio/Imagens/5.png)

Agora faça login no sistema com usuario que você criou:
![6](/home/gio/Imagens/6.png)

Agora acesse a url para a home do site:

```
http://127.0.0.1:8000/
```

![](/home/gio/Imagens/7.png)

Ao clicar no sinal  ' + ' , você pode adicionar um novo post

![2](/home/gio/Imagens/8.png)

Após adicionar um post, você pode altera-lo

![2](/home/gio/Imagens/9.png)

A Home ficará assim:

![10](/home/gio/Imagens/10.png)

Agora é só utilizar o Blog : ) 

