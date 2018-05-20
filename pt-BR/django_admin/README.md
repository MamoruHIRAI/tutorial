# Django Admin

Para adicionar, editar e deletar os posts que acabamos de modelar, nós usaremos o admin do Django.

Vamos abrir o arquivo `blog/admin.py` e substituir seu conteúdo por isso:

{% filename %}blog/admin.py{% endfilename %}

```python
from django.contrib import admin
from .models import Post

admin.site.register(Post)
```

Como você pode ver, nós importamos (incluímos) o modelo Post definido no capítulo anterior. Para tornar nosso modelo visível na página de administração, nós precisamos registrá-lo com `admin.site.register(Post)`.

OK, hora de olhar para o nosso modelo de Post. Lembre-se de executar `python manage.py runserver` no console para iniciar o servidor web. Vá para o seu navegador e digite o endereço http://127.0.0.1:8000/admin/. Veremos uma página de login como essa:

![Página de login](images/login_page2.png)

Para fazer login, você precisa criar um *superusuário (superuser)* - uma conta de usuário que pode controlar tudo no site. Volte à linha de comando, digite `python manage.py createsuperuser` e aperte Enter.

> Lembre-se, para escrever novos comandos enquanto o servidor web está rodando, abra uma nova janela do terminal e ative seu virtualenv. Nós revisamos como escrever novos comandos no capítulo **Seu primeiro projeto Django!**, na seção **Iniciando o servidor web**.

{% filename %}Mac OS X ou Linux:{% endfilename %}

    (myvenv) ~/djangogirls$ python manage.py createsuperuser
    

{% filename %}Windows:{% endfilename %}

    (myvenv) C:\Users\Name\djangogirls> python manage.py createsuperuser
    

When prompted, type your username (lowercase, no spaces), email address, and password. **Não se preocupe se você não consegue ver a senha que está digitando – é assim que tem ser.** Só digitá-la e pressionar `enter` para continuar. The output should look like this (where the username and email should be your own ones):

    Username: admin
    Email address: admin@admin.com
    Password:
    Password (again):
    Superuser created successfully.
    

Volte ao seu navegador. Faça login com as credenciais de superusuário que você escolheu; você deverá ver o painel de controle de administração do Django.

![Django admin](images/django_admin3.png)

Vá para Posts e experimente um pouco por lá. Adicione cinco ou seis posts. Não se preocupe com o conteúdo - você pode simplesmente copiar e colar algum texto desse tutorial para economizar tempo. :)

Certifique-se que pelo menos duas ou três postagens (mas não todas) têm a data de publicação definida. Isso será útil depois.

![Django admin](images/edit_post3.png)

Se você quiser saber mais sobre o Django admin, você precisa conferir a documentação do Django: https://docs.djangoproject.com/en/1.11/ref/contrib/admin/

Esse provavelmente é um bom momento para pegar um café (ou chá) ou algo para comer para recuperar as energias. Você criou seu primeiro modelo em Django - você merece uma pausa!