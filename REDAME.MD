После клонирование проекта с репозитория необходимо открыть терминал и перейти в 
директорию с проектом

`cd <path_toproject>`

Далее выполнить команду `docker-compose up -d --build`


Для доступа к админке необходимо создать суперпользователя выполнив серию команд в терминале

`docker ps` - покажет списк всех контейнеров нас интересует id контейнера obli_backend-web

`docker exec -ti <id_container> bash`

Так мы попали внутрь контейнера и можем выполнять терминальные команды.

Создадим суперпользователя командой: `python manage.py createsuperuser` следуя инструкции выполните то
о чем просит система. В итоге будет создан пользователь с указанными вами логином и паролем. Теперь можно войти
в админку джанги по адресу http://localhost:8000/admin/

В админке в модели Items можно создать несколько товаров с описанием.

Затем переходя по адрсам /buy/{id},/item/{id} можно протестировать созданый сервис


