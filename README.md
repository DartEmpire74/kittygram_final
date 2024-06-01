# Описание проекта 

Проект `Kittygram` представляет из себя социальную сеть, в которой владельцы котиков могут делиться информацией о своих питомцах.
При добавлении котика на портал, вы можете указать его достижения, прикрепить фото, указать цвет, имя и год рождения.

# Стек технологий 

## Backend
- Django
- PostgreSQL
- Django REST Framework

## Frontend
- React
- Redux
- Axios
- Material-UI

## Gateway
- Nginx
- Certbot

# Развертывание проекта

Для развертывания проекта вам потребуется установить Docker и Docker Compose, 
если они еще не установлены на вашем сервере.

## Шаги развертывания
1. Скопируйте файл `docker-compose.production.yml` в корневую директорию вашего проекта.
2. Создайте файл .env и укажите в нем следующую информацию: 
`ALLOWED_HOSTS, DEBUG, USE_SQLITE, POSTGRES_DB, POSTGRES_USER, POSTGRES_PASSWORD, DB_NAME, DB_HOST, DB_PORT`.

### Пример файла .env: 
```
ALLOWED_HOSTS= 127.0.0.1,localhost
DEBUG=true
USE_SQLITE=false

POSTGRES_DB=your_database
POSTGRES_USER=your_username
POSTGRES_PASSWORD=your_password
DB_NAME=your_database

DB_HOST = db
DB_PORT = 5432
```

3. В командной строке перейдите в директорию с вашим проектом.
4. Запустите контейнеры с помощью команды:
```
docker-compose -f docker-compose.production.yml up -d
```
5. После успешного запуска всех контейнеров ваше приложение будет доступно по адресу 
`http://ваш_домен` или `http://IP_адрес:9000`, в зависимости от конфигурации.


## Автор проекта
__Артем Бахарев__ - `https://github.com/DartEmpire74`
