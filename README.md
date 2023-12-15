# README


Этот проект на Spring Boot, собранный с использованием Gradle, предоставляет RESTful API для управления сущностями, связанными с библиотекой, включая книги, клиентов (пользователей) и выпуски. Следуйте инструкциям ниже, чтобы настроить и запустить проект.

## Предварительные требования

- **Docker**: Убедитесь, что Docker установлен на вашем компьютере.

## Настройка базы данных

1. Откройте терминальное окно.

2. Запустите следующую команду для запуска базы данных PostgreSQL с использованием Docker:

   ```
   docker run --rm --name pg-docker -e POSTGRES_PASSWORD=test -e POSTGRES_USER=test -e POSTGRES_DB=module1 -p 5433:5432 postgres:13
   ```
   Эта команда запускает контейнер PostgreSQL с указанной конфигурацией.

## Настройка проекта
1. Клонируйте репозиторий:
```
git clone https://github.com/kistaubaeff/CRUD.git
```
2. Откройте проект:

Откройте проект в вашей предпочтительной среде разработки на Java.

3. Соберите и запустите:

Соберите и запустите приложение Spring Boot из среды разработки.

4. Доступ к API:

Используйте инструмент, такой как Postman или любой клиент REST, чтобы получить доступ к предоставленным конечным точкам API.

## Настройка базы данных
Проект настроен для подключения к базе данных PostgreSQL с использованием следующих параметров:

URL базы данных:
``` jdbc:postgresql://localhost:5433/module1 ```
Имя пользователя:
 ``` test ```
Пароль:
 ``` test ```
Если вам необходимо изменить конфигурацию базы данных, вы можете найти ее в файле application.properties в проекте.

API
1. Контроллер книг (BookController)
Конечные точки:
GET /books: Возвращает список всех книг.
GET /books/{id}: Возвращает конкретную книгу по ее идентификатору.
POST /books: Сохраняет новую книгу.
PUT /books/{id}: Обновляет информацию о книге по ее идентификатору.
DELETE /books/{id}: Удаляет книгу по ее идентификатору.
2. Контроллер клиентов (ClientController)
Конечные точки:
GET /users: Возвращает список всех пользователей.
GET /users/{id}: Возвращает конкретного пользователя по его идентификатору.
POST /users: Сохраняет нового пользователя.
PUT /users/{id}: Обновляет информацию о пользователе по его идентификатору.
DELETE /users/{id}: Удаляет пользователя по его идентификатору.
3. Контроллер выпусков (IssueController)
Конечные точки:
GET /issues: Возвращает список всех выпусков.
GET /issues/{id}: Возвращает конкретный выпуск по его идентификатору.
POST /issues: Создает новый выпуск.
PUT /issues/{id}: Обновляет информацию о выпуске по его идентификатору.
DELETE /issues/{id}: Удаляет выпуск по его идентификатору.


## Благодарю за использование проекта!
