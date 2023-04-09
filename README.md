# Учебный проект yamdb_final  
 
### Описание проекта 
Yamdb_final это учебный проект, в котором реализована API сервиса,  
на котором можно размещать произведения, каталогизировать их,  
комментировать и подписываться на интересных авторов.  
 
### Как развернуть проект локально 
Проект упакован в Докер, запускается командой 
    docker-compose up -d 
Для того, чтобы команда выполнилась необходимо установить Docker, сделать это можно на официально сайте https://www.docker.com. 
Далее необходимо выполнить миграции командой 
    sudo docker-compose exec web python manage.py migrate 
После этого создать суперпользователя, используя команду 
    sudo docker-compose exec web python manage.py createsuperuser 
И наконец, собрать статику командой 
    sudo docker-compose exec web python manage.py collectstatic --no-input 

 
### Статус workflow 
![yamdb_final](https://github.com/Nasibao/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)


### Проект развернут
http://158.160.51.54/api/v1/
http://158.160.51.54/admin (login - "admin" , password - "admin" )
